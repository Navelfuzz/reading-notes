# CF301 Reading Notes Class 05: Putting it all together

## Reading

[React Docs - Thinking in React](https://react.dev/learn/thinking-in-react)

### Questions

1. What is the single responsibility principle and how does it apply to components?
2. What does it mean to build a ‘static’ version of your application?
3. Once you have a static application, what do you need to add?
4. What are the three questions you can ask to determine if something is state?
5. How can you identify where state needs to live?

### Answers

1. SRP is a principle in Software Engineering that states a component or class should have only one reason to change. It means that a component should have a single responsibility or purpose and should focus on doing that one thing well.
2. Meaning that the version has no interactive or dynamic behavior. Simplifies everything and acts as a skeleton to add functionality to.
3. You have to add dynamic behaviors such as input handling, data fetching, updating the app state based on user/external events, rendering the updated content.
4. Does it change over time? Can it be derived or calculated from other state or props? Does it need to be preserved and restored across component renders or application sessions?
5. From article:

        1. Identify every component that renders something based on that state.
        2. Find their closest common parent component—a component above them all in the hierarchy.
        3. Decide where the state should live:
          1. Often, you can put the state directly into their common parent.
          2. You can also put the state into some component above their common parent.
          3. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common parent component.

[Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)

### Questions

1. What is a “higher-order function”?
2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
3. Explain how either map or reduce operates, with regards to higher-order functions.

### Answers

1. A function that can accept other functions as arguments and/or return functions as results.
2. Line 2 takes the 'n' parameter and returns the t/f value of `m > n` to the `m` variable which is then used with console.log
3. The "map" function takes an array and a transformation function as arguments. It applies the transformation function to each element of the array and returns a new array with the transformed values. Essentially, it maps each element of the original array to a corresponding element in the resulting array based on the transformation logic provided by the function.
