# CF301 Reading Notes Class 09: Functional Programming

## Reading

[Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

### Questions

1. What is functional programming?
2. What is a pure function and how do we know if something is a pure function?
3. What are the benefits of a pure function?
4. What is immutability?
5. What is Referential transparency?

### Answers

1. A programming paradigm that emphasizes the use of pure functions, immutability, and declarative programming style. It treats computation as the evaluation of mathematical functions and avoids changing state and mutable data. Promotes the use of higher-order functions, recursion, and immutable data structures.
2. A pure function is a function that, given the same input, will always produce the same exact output and has no side effects. It does not modify any external state or data outside of its own scope. Determined by: Only dependent on its input parameters, does not modify any external state or mutable data, does not have any side effects such as I/O operations or network requests.
3. Predictability, Testability, Modularity, Concurrency and Parallelism.
4. Immutability refers to the property of an object or data structure that connot be modified after it is created. So instead of modifying existing objects, new ones are created with updated values.
5. Referential transparency is a property of an expression in a programming language. An expression is referentially transparent if it can be replaced with its corresponding value without affecting the behavior of the program. In other words, if an expression always evaluates to the same result in the same context, it is referentially transparent.

___

## Videos

[Node JS Tutorial for Beginners #6 - Modules and require()](https://www.youtube.com/watch?v=xHLd36QoS4k)

### Questions

1. What is a module?
2. What does the word ‘require’ do?
3. How do we bring another module into the file the we are working in?
4. What do we have to do to make a module available?

### Answers

1. A reusable block of code that encapsulates related functionality. It includes variables, functions, classes, or objects that are organized and packaged together to provide a specific set of features or services. 
2. The `require` function is used to load and import modules. It is the primary way to include the functionality of other modules into the current module. By using `require`, you can access the exports or the public interface of another module and use its functionality within your current module.
3. To bring in another module you need to use the `require` function and provide the path or name of the module you want to import. The path can be a relative path to a local module or the name of a globally installed module. `const myModule = require('./myModule');`
4. To make a module available you have to export the functionality. 

        const myFunction = () => {
            //function implementation
        };

        module.exports = myFunction;
