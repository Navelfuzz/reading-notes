# CF 401: Java // Reading Notes

## Class 14: Salt and Passwords

## Readings

[Intro to Password Hashing](https://auth0.com/blog/hashing-passwords-one-way-road-to-security/)

### Questions

1. Define the term “hashing”.
2. Explain to a non-technical friend what a hash function does to a password.

### Answers

1. Hashing is a process in computer science and cryptography where data, such as text or files, is transformed into a fixed-size string of characters, which is typically a sequence of numbers and letters. This fixed-size string is known as a "hash value" or simply a "hash." The purpose of hashing is to create a unique representation of the original data, so even a small change in the input will produce a completely different hash value. In the context of passwords, hashing is used to store password information securely. When you create an account on a website or service, your password is not stored in its original form. Instead, it goes through a one-way hash function, and only the resulting hash value is saved in the database. This way, even if someone gains access to the database, they cannot see the actual passwords, as they are irreversibly transformed into hashes.
2. Imagine you have a secret message (the password) that you want to keep safe. However, instead of locking it away in a box, you decide to use a special box with a magical lock (the hash function). Here's how the magical lock works: You put your secret message (password) into the magical lock, and it automatically turns it into a unique and scrambled puzzle (the hash). The magic part is that this puzzle can't be turned back into the original message! It's like transforming your password into a secret code that only the lock knows how to create. Now, whenever you need to use your secret message (for logging into a website, for example), you don't give out the original message. Instead, you give out the scrambled puzzle (the hash). When the website wants to check if you typed the correct password, it takes what you entered, scrambles it using the same magical lock (hash function), and then compares the scrambled puzzle (hash) you provided with the one they have stored. If the two puzzles match, they know you entered the right password without ever seeing your actual secret message (password). This way, even if someone sneaks into the website and looks at the puzzles in the database, they won't be able to figure out what your original secret message (password) is because the magical lock (hash function) works only one way, turning your secret message into an unbreakable puzzle!

[bcrypt Overview](https://danboterhoven.medium.com/why-you-should-use-bcrypt-to-hash-passwords-af330100b861)

### Questions

1. What does it mean to ‘salt’ a password?
2. What piece of information would a hacker need to access in order to find the ‘salt’ string for your passwords?

### Answers

1. Salting a password is a technique used to enhance the security of password storage in computer systems, particularly in the context of hashing passwords. A "salt" is a random string of characters that is generated uniquely for each user's password. When a user creates or updates their password, the salt is combined with the password before hashing it using a cryptographic hash function. The resulting hashed value, which includes the salt, is then stored in the database. The purpose of salting is to prevent attackers from using precomputed tables (rainbow tables) or other common techniques to quickly look up the hashed value of commonly used passwords. With a unique salt for each user, even if multiple users have the same password, their hashed values will be different due to the different salts.
2. The 'salt' is intended to be a random and unique value for each user, and its purpose is to add unpredictability to the hashing process. Therefore, the 'salt' is generally stored alongside the hashed password in the database. It is not meant to be secret or confidential. As a result, a hacker who gains access to the hashed passwords in the database will also have access to the corresponding 'salt' values. However, the presence of the 'salt' significantly complicates the hacker's attempts to crack the passwords using precomputed tables or common attacks. To successfully find the original passwords, the hacker would need to perform a brute-force attack or use other complex methods, which are much more time-consuming and less practical compared to traditional attacks when salts are not used. In summary, the 'salt' is stored alongside the hashed password in the database and is not kept secret. Its presence increases the complexity of password cracking for attackers and enhances the security of password storage.

[jBCrypt (top of page)](https://www.mindrot.org/projects/jBCrypt/)

### Questions

1. How does the Blowfish block cipher handle the increased computation speed of new computers?
2. What are the issue with the two most commong password hashes for Java (“Java password hash” and “Java password encryption”)?

### Answers

1. Blowfish is a symmetric block cipher designed by Bruce Schneier in 1993. It uses a variable-length key and processes data in blocks of 64 bits. One of the key features of Blowfish is its ability to adjust its encryption/decryption speed based on the processor's capabilities.

As computers have evolved and become more powerful over time, the processing speed has increased significantly. Blowfish takes advantage of this by employing a key setup phase that involves multiple rounds of processing the key data. The number of rounds, known as the "iteration count," can be adjusted to make the cipher more computationally intensive. This iteration count can be set dynamically based on the capabilities of the computer.

In modern implementations of Blowfish, the iteration count can be chosen based on the computer's processing power. This means that the cipher can be made to run slower on more powerful computers, increasing the time it takes to encrypt or decrypt data. This technique, known as key stretching or key strengthening, helps counteract the increased computational speed of modern hardware, making the cipher more resistant to brute-force attacks.
2. See Below: 
* "Java password hash":
    The term "Java password hash" is not specific to any particular algorithm, but it generally refers to storing passwords in a hashed form using standard hashing algorithms like MD5 or SHA-1. The main issue with using MD5 or SHA-1 for password hashing is that they are fast, one-way hash functions, which makes them vulnerable to brute-force attacks and rainbow table attacks. These attacks are possible because these algorithms are designed for speed and efficiency, and with the computational power available today, attackers can quickly generate hashes for a large number of possible passwords and compare them to the stored hashes. Moreover, since MD5 and SHA-1 are widely used, attackers can precompute tables (rainbow tables) of hashes for common passwords, allowing them to quickly look up the original passwords.

* "Java password encryption":
    Similarly, "Java password encryption" could refer to various encryption algorithms used to store passwords, but common encryption methods like AES or DES are not suitable for password storage. Encryption is a two-way process, and the original password can be retrieved if the encryption key is known. The problem with using encryption for password storage is that the encryption key must be stored somewhere, and if an attacker gains access to both the encrypted passwords and the key, they can easily decrypt the passwords. Additionally, encryption algorithms are designed for data confidentiality, not password storage, so they lack the necessary properties for securely protecting passwords, such as key stretching and salting. To securely hash passwords in Java, it's recommended to use strong password hashing functions specifically designed for this purpose, such as bcrypt, PBKDF2, or Argon2. These algorithms incorporate salting, key stretching, and other security measures to protect passwords effectively against various attacks.
