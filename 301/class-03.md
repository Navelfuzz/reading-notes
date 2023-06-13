# CF301 Reading Notes Class 03: Passing Functions as Props

## Reading

[React Docs - lists and keys](https://legacy.reactjs.org/docs/lists-and-keys.html)

### Questions

1. What does .map() return?
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
3. Each list item needs a unique ____.
4. What is the purpose of a key?

### Answers

1. Returns a new array with transformed values.
2. `items.map(item, index) => (<li key={index}>{item}</li>)`
3. key
4. It gives each item in a list a uniqe id.

[The Spread Operator](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

### Questions

1. What is the spread operator?
2. List 4 things that the spread operator can do.
3. Give an example of using the spread operator to combine two arrays.
4. Give an example of using the spread operator to add a new item to an array.
5. Give an example of using the spread operator to combine two objects into one.

### Answers

1. `...` used in various contexts to expand or spread elements, arrays, or objects.
2. "spread" elements of an array into individual elements, concatenate arrays, copy objects, merge objects.
3. 
        const arr1 = [1, 2, 3];
        const arr2 = [4, 5, 6];
        const combinedArray = [...arr1, ...arr2];
        console.log(combinedArray); // Output: [1, 2, 3, 4, 5, 6]

4. 
        const originalArray = [1, 2, 3];
        const newItem = 4;
        const newArray = [...originalArray, newItem];
        console.log(newArray); // Output: [1, 2, 3, 4]
5. 
        const obj1 = { name: 'John', age: 30 };
        const obj2 = { city: 'London', occupation: 'Engineer' };
        const mergedObject = { ...obj1, ...obj2 };
        console.log(mergedObject);
        // Output: { name: 'John', age: 30, city: 'London', occupation: 'Engineer' }


## Videos

[How to Pass Functions Between Components](https://www.youtube.com/watch?v=c05OL7XbwXU)

### Questions

1. In the video, what is the first step that the developer does to pass functions between components?
2. In your own words, what does the increment function do?
3. How can you pass a method from a parent component into a child component?
4. How does the child component invoke a method that was passed to it from a parent component?

### Answers

1. Define the function in the parent component.
2. Adds to a count in order to often keep track of usage.
3. Pass it as a prop.
4. Child calls the method using the prop it received.
