# CF 401: Java // Reading Notes

## Class 03: Jave Data Types, Exceptions, and Files

## Readings

[Primitives vs. Objects](https://www.baeldung.com/java-primitives-vs-objects)

### Questions

1. Explain the difference between an “int” and an “Integer” in Java.
2. What is the default value for ints? Integers?
3. What is autoboxing? Unboxing?

### Answers

1. `int` is a primitive data type that is a 32 bit signed integer. `Integer` is a class defined in the Java API and belongs to the java.lang package. It wraps the primitive `int` type into an object. It provides various methods and utility functions for working with integer values.
2. `int` default value is 0. `Integer` is null. This is a difference in memory usage. `int` when declared has to assign memory space for the integer whereas `Integer` doesn't allocate a memory space until the object is created. 
3. Autoboxing is the automatic conversion of a primitive type into its corresponding wrapper class. Unboxing is the opposite.

[Exceptions in Java](https://docs.oracle.com/javase/tutorial/essential/exceptions/index.html)

### Questions

1. List the three basic categories of exceptions.
2. What type of statement can you use to handle an exception?

### Answers

1. Checked, Unchecked, and Errors
2. `try-catch` & `finally` (where applicable)
[Using Scanner to read in a file in Java](https://docs.oracle.com/javase/tutorial/essential/io/scanning.html)

### Questions

1. Describe a situation where you think it would be useful to have a program that scans text.
2. What is input from a Scanner broken down into?

### Answers

1. Say your job is one where you take a preformatted memo and convert it to some form of spreadsheet or vice versa and want to automate.
2. By default it is broken into tokens, which are the individual units of data. However you can configure what delimiters or expressions to define how the input should be tokenized.
