# CF301 Reading Notes Class 04: React and Forms

## Reading

[React Docs - Forms](https://legacy.reactjs.org/docs/forms.html)

### Questions

1. What is a ‘Controlled Component’?
2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.
3. How do we target what the user is entering if we have an event handler on an input field?

### Answers

1. An input form element whose value is controlled by React
2. If we update on submit then we have a complete and consistent state, we aren't handling incomplete submissions. If we do it upon change then although we see their incremental real-time info we then deal with several different instances of submission essentially.
3. `event.target.value` in an event handler saved to a variable. Then `input type="text" onChange={handleChange} />`

[The Conditional (Ternary) Operator Explained](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)

### Questions

1. Why would we use a ternary operator?
2. Rewrite the following statement using a ternary statement:

        if(x===y){             
          console.log(true);    
        } else {
          console.log(false);      
        }

### Answers

1. When expressing conditional statements. `condition ? expressionIfTrue : expressionIfFalse`
2. `console.log(x === y ? true : false);
