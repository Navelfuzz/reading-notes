# Reading Class 09: Forms and JS Events

## [HTML Forms](https://developer.mozilla.org/en-US/docs/Learn/Forms)

[Your first Web Form](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form)

[How to structure a Web Form](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form)

*Questions*

1. Why are forms so important in web development?
2. When designing a form, what are some key things to keep in mind when it comes to user experience?
3. List 5 form elements and explain their importance.

*Answers*

1. Allows the collection of data from a user.
2. "K.I.S.S." don't overload the user with a form that asks too much. Keep it readable and understandable.
3. `<form>` formally defines the form, it's a container element, `<label>` defines the following input section purpose, `<input>` defines the following input by type/id/name, `<textarea>` textbox that is fillable, `<button>` allows creation of something such as a submission button.

## [Learn JS](https://developer.mozilla.org/en-US/docs/Learn/JavaScript)

[Introduction to Events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)

*Questions*

1. How would you describe events to a non-technical friend?
2. When using the addEventListener() method, what 2 arguments will you need to provide?
3. Describe the event object. Why is the target within the event object useful?
4. What is the difference between event bubbling and event capturing?

*Answers*

1. Events are the activities that occur and are logged such as mouse clicks, keyboard entries, form submissions. Every action that occurs from the loading of the page to the closing of it and everything inbetween.
2. The type of event being listened for such as click, keydown, or submit. And also the event handler function which is the code to be executed when the specified event occurs.
3. It represents an event that occurs such as a mouse click, it contains the info about the event and its properties that can be accessed within the event handler function. The target property allows us to access the specific element that triggered an event.
4. Bubbling moves from inside out, Capture moves from outside in, in terms of how the event is located and identified.

### Bookmark and Review

[HTML5 Input Types](https://developer.mozilla.org/en-US/docs/Learn/Forms/HTML5_input_types)
[Event Reference and Listings](https://developer.mozilla.org/en-US/docs/Web/Events)