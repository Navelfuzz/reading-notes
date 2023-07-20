# CF 401: Java // Reading Notes

## Class 06: OO Java, Static, Singleton

## Readings

[Java OO Tutorial (review Object and Class, read the rest)](https://docs.oracle.com/javase/tutorial/java/concepts/)

### Questions

1. What is the difference between an Object and a Class in Java?
2. Explain to a non-technical friend the concept of inheritance in Java.

### Answers

1. Classes are like a recipe or blueprint, while an object is the actual food/item created following the recipe.
    * Class: A class is a blueprint or template that defines the properties and behaviors of an object. It serves as a template for creating objects of a particular type. It encapsulates the data (attributes) and methods (functions) that define the behavior of objects.
    * Object: An object is an instance of a class. It represents a specific entity or occurrence that was created based on the class blueprint. An object has its own unique state (attribute values) and behavior (methods).
2. Think of it as a parent-child relationship. The child class inherits the characteristics of the parent class, such as its attributes (data) and methods (functions). This means that the child class can reuse the code from the parent class without having to redefine it. Inheritance promotes code reusability and allows you to create specialized classes that inherit the common features from a more general class. It helps in organizing and structuring code by creating a hierarchy of classes. For example, let's say we have a class called "Animal" that has attributes and methods common to all animals. We can create specific classes like "Dog" and "Cat" that inherit from the "Animal" class. The "Dog" and "Cat" classes will have their unique features but also inherit the common attributes and behaviors from the "Animal" class. Inheritance is like a family tree, where the parent class is at the top and the child classes branch out from it, inheriting its characteristics while adding their own specific traits.

[Java Static Keyword](https://www.programiz.com/java-programming/static-keyword)

### Questions

1. Static methods are also called what? Why?
2. How can you access a variable of a class without instantiating an object from that class?

### Answers

1. Static methods are also called 'class methods' because they belong to the class rather than to any specific instance (object) of the the class. They can be accessed directly through the class name, without needing to create an instance of the class. 
2. To access a variable of a class without instantiating an object, the variable must be declared as static. Static variables are of the class itself and not of the object. You can access them using the class name followed by the dot operatore, without needing to create an instance of the class. 

[Java Singleton Class](https://www.programiz.com/java-programming/singleton)

### Questions

1. What is a Design Pattern? Describe one or two with analogies from your previous work experience.
2. What is a Singleton?

### Answers

1. A reusable and proven solution to common software design problems. If I were to go as far back as boot camp... I imagine this is why they gave us sharpies and stencils to label our underwear.
2. A singleton is a creational design pattern that ensures a class has only one instance and provides a global access point to that instance throughout the application's lifetime. It is often used when you want to restrict the instantiation of a class to a single object.

        public class SingletonExample{
            private static SingletonExample instance;

            private SingletonExample(){
                //private constructor to prevent direct instantiation
            }

            public static SingletonExample getInstance(){
                if (instance == null){
                    instance = new SingletonExample();
                }
                return instance;
            }
        }
