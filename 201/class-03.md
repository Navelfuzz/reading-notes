# HTML Lists, Control Flow with JS and the CSS Box Model

## Learn HTML

___

### Questions

1. When should you use an `unordered list` in your HTML document?
2. How do you change the `bullet style` of unordered list items?
3. When should you use an `ordered list` vs an `unorder list` in your HTML document?
4. Describe two ways you can change the numbers on `list items` provided by an `ordered list`?

### *Answers*

1. When the order of the items isn't meaningful.
2. Style attribute `list-style-type:format`
3. Use an ordered list when the order of the items is relevant.
4. `ol type="i"` swould make roman numerals. `ol start="4"` makes the starting number 4 in your list.

___

## Learn CSS

___

### Questions

1. Describe the CSS properties of `margin` and `padding` as characters in a story. What is their role in a story titled: “The Box Model”?
2. List and describe the four parts of an HTML elements box as referred to by the `box model`.

### *Answers*

1. Margin has this problem where he doesn't like being around other people so as he increases his powers he pushes them away. Padding is obsessively rearranging the furniture in their home thinking that with the appropriate fung shui all of lifes problems will be solved.
2. Margin, Padding, Content, Border. Margin is space between the border and other 'boxes'. Padding is the space between content and the encapsulating border. Border is the box the content is in. Content is the relevant information you have framed in your box.

___

## Learn JS

___

### Questions

1. What `data types` can you store inside of an `Array`?
2. Is the `people` array a valid JavaScript array? If so, how can I access the values stored? If not, why?

         const people = [['pete', 32, 'librarian', null], ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'], ['bill', null, 'artist', null]];

3. List five shorthand operators for assignment in javascript and describe what they do.
4. Read the code below and evaluate the last `expression` and explain what the result would be and why.

         let a = 10;
         let b = 'dog';
         let c = false;

        // evaluate this
         (a + c) + b;

5. Describe a real world example of when a conditional statement should be used in a JavaScript program.
6. Give an example of when a Loop is useful in JavaScript.

### *Answers*

1. Primitives: boolean, numbers, strings, null, undefined. Also object which is a reference type.
2. No. An array is not dynamic in that you can have different organization patterns.
3. `=` assigns the right hand value to the left hand name. `+=` would add the left hand value to the right hand value as the final sum. `-=` would subtract the right hand value from the left hand value as the final sum. `*=` would multiply both values as the final value. `/=` would divide the left hand value by the right hand value as the final value.
4. The output is erreneous because you would need to concatenate the values as an output. You cannot do math between numbers and words.
5. Age resrictions for website content.
6. Writh an output once. Creat a loop that displays it 5 times.

___

Author: Jonathon Stillson
