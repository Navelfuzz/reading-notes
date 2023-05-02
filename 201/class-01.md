# Read: Class 01

In this section we cover the basics of getting started with web-development. It covers how the web works, web design and process, and javascript, html, css...

## Getting Started

### Questions

1. Compose a short poem describing how HTTP sends data between computers.
2. Describe how HTML, CSS, and JS files are “parsed” in the browser.
3. How can you find images to add to a Website?
4. How do you create a String vs a Number in JavaScript?
5. What is a Variable and why are they important in JavaScript?

### Answers

- Poem about data transfer:

        HTTP, the protocol of the web
        Sends data between computers, no sweat
        A request from one, a response from the other
        They communicate, like sister and brother

        First comes the client, who makes the call
        Asks for a file, big or small
        The server responds, with a code of its own
        200 means success, 404, unknown

        The data travels, in packets so neat
        From one computer to another, a feat
        It travels through wires, or through the air
        Until it reaches its destination, without a care

        And so HTTP, the language of the web
        Enables us to browse, without any dread
        It's a protocol we all rely on, day to day
        Sending data between computers, in its own special way.

- Additional poem about packet loss.

        I am a packet, lost in the fray
        A lost little piece, on its way
        I set out on a journey, with a purpose so clear
        To reach my destination, without any fear

        But alas, something went wrong on the way
        A hiccup, a glitch, or a delay
        I got lost in the transfer, in the vast digital space
        An outcast, a failure, without a place

        I was meant to be part of a bigger whole
        To deliver a message, to play my role
        But now I'm just a lost packet, with no way back
        A victim of the digital highway's attack

        I long to be found, to complete my task
        To be reunited with my digital mask
        But until then, I'll wander aimlessly in this void
        A lost packet, without a voice.

        Oh, how I wish I could find my way
        To reach my destination, without delay
        But until then, I'll just keep on searching
        A lost packet, still determined and perching.

- The browser parses HTML first and then recognizes any `<link>` to external CSS stylesheets and internal stylesheets via `<style>` it implements css data. It finds any JavaScript files with `<script>`

- Images can be drawn from any source you can link from an HTML address or upload a file.

- Strings are denoted by double or single quotations around characters after the assignment operator as such: `let myVariable = "bippity boppity";`. Numbers follows the same convention but no quotations go around the number assigned to the variable.

- A variable are conatiners that store values. At location A I have stored value X.

## Introduction to HTML

### Questions

1. What is an HTML attribute?
2. Describe the Anatomy of an HTMl element.
3. What is the Difference between `<article>` and `<section>` element tags?
4. What Elements does a “typical” website include?
5. How does metadata influence Search Engine Optimization?
6. How is the `<meta>` HTML tag used when specifying metadata?

### Answers

## How to start to design a wesite

### Questions

1. What is the first step to designing a Website?
2. What is the most important question to answer when designing a Website?

### Answers

1. Determine what it is you want to accomplish and how a website will help you do that. Then plan out what needs to be done and develop an ordered task list. *Project Ideation*
2. What is your goal?

## Semantics

### Questions

1. Why should you use an `<h1>` element over a `<span>` element to display a top level heading?
2. What are the benefits of using semantic tags in our HTML?

### Answers

1. Being a semantic element it identifies the imbedded text as something, in this case, a top level header.
2. Semantic tags tie into SEO, accessibility functions, keeps code organized and labeled, readable/understandable, follows naming conventions.

## What is JavaScript?

### Questions

1. Describe 2 things that require JavaScript in the Browser?
2. How can you add JavaScript to an HTML document?

### Answers

1. JavaScript allows your website to have dynamic features, like modifications to HTML and CSS to update UI. Also allows you to access APIs.
2. `<script>` element.