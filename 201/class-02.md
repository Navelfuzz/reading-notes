# Read: Class 02 Basics of HTML, CSS & JS

## Introduction to HTML

1. Why is it important to use semantic elements in our HTML?
2. How many levels of headings are there in HTML?
3. What are some uses for the `<sup>` and `<sub>` elements?
4. When using the `<abbr>` element, what attribute must be added to provide the full expansion of the term?

### *Answers:*

1. Semantic elements provide information that identifies what the content is, this integrates into several background browser services as well as organizes our page for ideal Search Engine Optimization
2. There are 6 heading elements `<h1>` through `<h6>`
3. 'sup' and 'sub' are shorthand for superscript and subscript. Superscripts are used for things such as exponents:

        a<sup>2</sup> + b<sup>2</sup> = c<sup>2</sup>

    Would appear as: a<sup>2</sup> + b<sup>2</sup> = c<sup>2</sup>

4. `<title>`

___

## Learn CSS

1. What are ways we can apply CSS to our HTML?
2. Why should we avoid using inline styles?

* Review the block of code below and answer the following questions:<br>

        h2 { 
        color: black;
        padding: 5px;
        }

    a. What is representing the selector?<br>
    b. Which components are the CSS declarations?<br>
    c. Which components are considered properties?<br>

### *Answers:*

1. External Stylesheets are separate text files with a `.css` extension which is `<link>` imbedded into our HTML document. But it can also all be annotated in the same document within the `<head>` using a `<style>` element.
2. The most notable reason to have an external stylesheet is because it allows you to refer to one body of `<style>` parameters and `<link>` it to multiple HTML pages.

a. `h2` <br>
b. The curly braces: `{}` and everything within them are the declaration. <br>
c. the properties in this code are `color` and `padding`

___

## Learn JS

1. What data type is a sequence of text enclosed in single quote marks?
2. List 4 types of JavaScript operators.
3. Describe a real world Problem you could solve with a Function.

### *Answers:*

1. string
2. Arithmetic, Comparison, Logical, Assignment
3. A function could be written to animate text in a way that every 7 seconds a letter within a designated number of characters will slowly turn into a different color and then slowly fade back to its original and the letter is randomly selected within the designated grouping. 

___

### <u> *Making Decisions In Your Code - Conditionals.* </u>

1. An if statement checks a __ and if it evaluates to ___, then the code block will execute.
2. What is the use of an `else if`?
3. List 3 different types of comparison operators.
4. What is the difference between the logical operator `&&` and `||`?g

### *Answers:*

1. Condition
2. It allows you to test another condition should the first not be true.
3. `==` is the equal to operator, `===` means equal value and equal type, `!=` means not equal.
4. `&&` (logical and) ties two separate variables/conditions/objects together. This means you can write a function to sort of glue two separate variables together, or you can write a discrimination function that returns true only if both variables are present. Whereas `||` designates 'or' and only one of the variables/conditions/objects has to be 'true' or meet criteria. This is not an exclusive logical operator it can still find both as meeting criteria.g

___
