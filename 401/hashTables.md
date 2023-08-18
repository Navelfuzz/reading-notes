# CF 401: Java // Reading Notes

## Class 30: Hash Tables

## Readings

[Intro to Hash Tables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

[Basics of Hast Tables](https://www.hackerearth.com/practice/data-structures/hash-tables/basics-of-hash-tables/tutorial/)


___

## Watch

[What is a Hash Table?](https://www.youtube.com/watch?v=MfhjkfocRR0)


___

## Skim

[Hash Table Wiki](https://en.wikipedia.org/wiki/Hash_table)


___

## Assignment:

To turn in your reading "Reply" to the discussion by teaching something that you learned from the readings listed.

Some ideas for how you might want to teach:

* Use an analogy
* Explain a detail in depth
* Use WHY, WHAT, HOW structure
* Tutorial/walk through an example
* Write a quiz
* Create a vocabulary/definition list
* Write a cheat sheet
* Create a diagram / visualization / cartoon of a topic
* Anthropomorphize the concepts, and write a conversation between them
* Build a map of the information
* Construct a fill-in-the-blank worksheet for the topic


___

# Hash Tables

## Interesting Facts:

* Hash Tables are also known as Hash Maps or Dictionaries in other programming languages.
* Hash Tables are a data structure that allows for efficient lookup, insertion, and deletion of key-value pairs.
* The time complexity for these operations is typically O(1), making Hash Tables one of the fastest data structures for these operations.
* Hash Tables use a hash function to map keys to indices in an array. This allows for constant-time access to values based on their keys.
* Hash Tables can handle collisions, which occur when two keys map to the same index in the array. There are several techniques for handling collisions, such as chaining and open addressing.
* Hash Tables are widely used in computer science and are the basis for many other data structures, such as Sets and Maps.
* The size of the array used by a Hash Table can affect its performance. A larger array can reduce the likelihood of collisions, but can also increase memory usage.
* Hash Tables can be used for a variety of applications, such as caching, indexing, and symbol tables.

## Cheat Sheet:

### Creating a Hash Table

```java
HashMap<KeyType, ValueType> map = new HashMap<>();
```

### Adding an Element

```java
map.put(key, value);
```

### Removing an Element

```java
map.remove(key);
```

### Checking if an Element Exists

```java
if (map.containsKey(key)) {
    // do something
}
```

### Accessing an Element

```java
ValueType value = map.get(key);
```

### Iterating Over Elements

```java
for (Map.Entry<KeyType, ValueType> entry : map.entrySet()) {
    KeyType key = entry.getKey();
    ValueType value = entry.getValue();
    // do something
}
```

### Getting the Size of the Hash Table

```java
int size = map.size();
```

### Clearing the Hash Table

```java
map.clear();
```

### Checking if the Hash Table is Empty

```java
if (map.isEmpty()) {
    // do something
}
```

### Hash Table with Custom Objects

If you want to use a custom object as a key in a Hash Table, you need to override the `hashCode()` and `equals()` methods in the object's class.

```java
public class MyClass {
    private int id;
    private String name;

    // constructor, getters, setters

    @Override
    public int hashCode() {
        return Objects.hash(id, name);
    }

    @Override
    public boolean equals(Object obj) {
        if (this == obj) {
            return true;
        }
        if (obj == null || getClass() != obj.getClass()) {
            return false;
        }
        MyClass other = (MyClass) obj;
        return id == other.id && Objects.equals(name, other.name);
    }
}
```

This will ensure that the object's hash code is based on its contents, rather than its memory address.
