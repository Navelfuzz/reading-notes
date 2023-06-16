# CF301 Reading Notes Class 10: Functional Programming

## Reading

[Understanding the JavaScript Call Stack](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)

### Questions

1. What is a ‘call’?
2. How many ‘calls’ can happen at once?
3. What does LIFO mean?
4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
5. What causes a Stack Overflow?

### Answers

1. A 'call' refers to the invocation of a function. When a function is called in JS, it is added to the call stack. The execution of the program moves to that function. Once the function completes its executions, it is removed from the call stack, and returns to the calling function.
2. Many function calls can happen at once. 
3. LIFO: Last In First Out, meaning if I call multiple functions the last function to be called and added onto the stack is the first to execute.
4. 
        Program Call Order:
        
        main()
        └── functionA()
            └── functionB()
                └── functionC()


        Stack Execution Order: 
        
        functionC()
        functionB()
        functionA()
        main()

5. 'Stack Overflow' occurs when there is a recursive function or a chain of function calls that consumes all the available stack space. "stack space" meaning available memory.

[JavaScript Error Messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

### Questions

1. What is a ‘reference error’?
2. What is a ‘syntax error’?
3. What is a ‘range error’?
4. What is a ‘type error’?
5. What is a breakpoint?
6. What does the word ‘debugger’ do in your code?

### Answers

1. When you try to access a variable or function that does not exist or is not currently in scope. It indicates the interpreter cannot find the referenced identifier, and typically causes a runtime error.
2. When you write code that violates the language's syntax rules. Indicates the code is not valid and cannot be parsed correctly by the JavaScript interpreter. Syntax errors are usually detected during the compilation or parsing phases befor the code is executed.
3. Occurs when you use a number outside of the valid range for a particular operation or function. For example, attempting to create an array with a negative length or using an invalid index for an array would result in a range error. 
4. When an operation or function is performed on a value of an unexpected type. It indicates a violation of the expected data taype or an incompatible operation. For instance, trying to call a non-funciton object or performing arithmetic on non-numeric values.
5. A specific point in the code where program execution pauses. This is used by developers to identify where problems are occuring in the code.
6. The word 'debugger' is a keyword in JavaScript that is used to trigger a breakpoint programmatically. When the 'debugger' statement is encountered in the code, it halts the execution and allows the developer to interactively debug and inspect the code using a debugger tool. It is commonly used to pause execution at a specific point to analyze variables, check control flow, and troubleshoot issues during development.
