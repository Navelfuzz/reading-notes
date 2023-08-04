# CF 401: Java // Reading Notes

## Class 19: but is it Functional?

## Readings

[Purely functional programming, from Wikipedia](https://en.wikipedia.org/wiki/Purely_functional_programming)

### Questions

1. Can you change the state of a data structure using functional programming?
2. Define purely functional programming.
3. How do you think purely functional programming will differ from the programs you’ve written so far in this course?

### Answers

1. One of the main points of Functional Programming is to minimize and avoid changing or mutating data structures, you just make new ones as necessary. 
2. Purely functional programming is an approach to writing programs that emphasizes immutability, referential transparency, and the use of functions to create and transform data. In a purely functional programming paradigm, functions do not have side effects (they do not modify external state or variables), and the output of a function depends solely on its input parameters. This predictability and lack of side effects make programs more robust, easier to reason about, and often more parallelizable.
3. I imagine (as I'm not super experienced or well versed in the concepts) that functional programming requires a lot of thought as to how you set up "trigger functions" that detect a state that requires a new data structure. I think also that I could perhaps monopolize the call stack to linear purposes rather than a more malleable abstraction. If data structures can mutate then they can be used for more than one production line at a time. 
