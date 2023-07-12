# CF 401: Java // Reading Notes

## Class 02: Imports, Loops, & Arrays in Java

## Readings

[Java Imports](https://www.programiz.com/java-programming/packages-import)

### Questions

1. Use an analogy to explain Built-In packages. Give examples.
2. Explain the steps for creating a new package in IntelliJ.

### Answers

1. Built-In packages are java packages that came along with the JDK. This is the Java version of the C++ standard library essentially as packages are pre-built collections of classes, interfaces, enumerations, and annotations. java.util.Date is an example, using this package saves a lot of time programming your own methods to derive the date in a program independently.
2. You define a .java file in a given directory as a package: `package <package name>`

[Different types of loops in Java](https://www.baeldung.com/java-loops)

### Questions

1. Which loop types use a loop counter?
2. Explain the difference between While and Do-While loops.

### Answers

1. `for` & `do-while` loops. However, you can craft a `while` loop to use a counter if you choose to, but it is not strictly necessary.
2. Both are based on a specified condition being true or fales. `while` checks the condition prior to iteration. `do-while` checks the condition after its iteration.

[Java Arrays](https://www.tutorialspoint.com/java/java_arrays.htm)

### Questions

1. Describe 3 built-in methods for Arrays.
2. How is the size of an array determined in Java?

### Answers

1. There are many
- asList(): Returns a fixed-size list backed by the specified Arrays
- binarySearch(): Searches for the specified element in the array wiht the help of the Binary Search Algorithm
- compare(array 1, array 2): Compares two arrays passed as parameters lexicographically
2. Based on its declaration at the time of its creation
