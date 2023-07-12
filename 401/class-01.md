# CF 401: Java // Reading Notes

## Class 01: Introduction to Java

## Readings

[Java Basics](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/index.html)

### Questions

1. What does “strong typed” mean?
2. What are the primitive data types?

### Answers

1. In Java, "strongly typed" refers to a type system in which variables and expressions have a specific type that is enforced by the compiler. In a strongly typed language like Java, every variable must be declared with its type explicitly, and once the type is assigned to a variable, it cannot be changed to a different type without explicit casting. Strong typing helps to catch errors at compile-time and promotes code reliability and clarity.

2. Java provides several primitive data types, which are the most basic data types built into the language. These primitive types are not objects and do not have methods or properties like objects do. The primitive data types in Java are:

- boolean: Represents a boolean value, which can be either true or false.
- byte: Represents an 8-bit signed integer value, ranging from -128 to 127.
- short: Represents a 16-bit signed integer value, ranging from -32,768 to 32,767.
- int: Represents a 32-bit signed integer value, ranging from -2,147,483,648 to 2,147,483,647.
- long: Represents a 64-bit signed integer value, ranging from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807.
- float: Represents a 32-bit floating-point value, which can store decimal numbers with limited precision.
- double: Represents a 64-bit floating-point value, which can store decimal numbers with higher precision than float.
- char: Represents a single 16-bit Unicode character.

[XKCD: Compiling](https://xkcd.com/303/)

### Questions

1. Explain to a non-technical friend the difference in how compilation works in Java and JavaScript.
2. Does code complining mean that it works correctly?

### Answers

1. Compilation is a means to take 'raw' Java code and essentially run it through a 'spell-checker' to find errors and ensure it is packaged properly so it can be run on a machine. In the case of Java it is converted to a language run by a virtual machine which allows it to work on any operating system without conflict. Javascript however is interpreted so it is run within an existing program.
2. No, it does make a general statement that the compiled files have 'integrity' of syntax and form but can't predict if the code doesn't account for inputs that break it's operation.

[Reading Java Documentation](https://www.dummies.com/category/articles/java-33602/)

### Questions

1. How many keywords does Java have?
2. How do you print words to the console in Java?

### Answers

1. 51
2. `System.out.println()`
