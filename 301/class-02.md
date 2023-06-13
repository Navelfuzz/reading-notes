# CF301 Reading Notes Class 02: State and Props

## Reading

[React Lifecycle](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

### Questions

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?
2. What is the very first thing to happen in the lifecycle of React?
3. Put the following things in the order that they happen: `componentDidMount`, `render`, `constructor`, `componentWillUnmount`, `React Updates`
4. What does `componentDidMount` do?

### Answers

1. render
2. Mounting, our instance of our component is being created and inserted into the DOM starting with `constructor`
3. `constructor`, `render`, `react updates`, `componentDidMount`, `componentWillUnmount`
4. THis method is invoked immediately after a component is mounted. It then loads anything using a network request.

[React State vs Props](https://www.youtube.com/watch?v=IYvD9oBCuJI)

### Questions

1. What types of things can you pass in the props?
2. What is the big difference between props and state?
3. When do we re-render our application?
4. What are some examples of things that we could store in state?

### Answers

1. Primitive values, Objects, React Elements
2. Props pass data from parent components to child components. State, is used to manage and store data within a component.
3. The application re-renders when there are changes to the component's state or props.
4. User input, Component configuration, loading or error states, component-specific data, UI-related data.
