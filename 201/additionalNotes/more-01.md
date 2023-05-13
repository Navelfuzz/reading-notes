# CF 201 Class 01 Additional Notes

## Links Included in the Reading Assignment

### [Getting Started with the Web](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)

#### *Guides*

- Installing basic software
- What will your website look like?
- Dealing with files
- HTML Basics
- CSS Basics
- JavaScript Basics
- Publishing your website
- How the Web Works

___

### [How the Web Works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works)

#### *Covered Materials*

- Clients and Servers: The web works on a basic principle of Clients making requests to Servers and Servers sending responses to Cients.
- TCP/IP: Transmission Control Protocol and Internet Protocol.
- DNS: Domain Name System.
- HTTP: Hypertext Transfer Protocol.
- Code Files: HTML, CSS, JavaScript
- Assets: images, music, video, documents

#### *Order of Operations*

1. The browser goes to the DNS server, and finds the real address of the server that the website lives on.
2. The browser sends an HTTP request message to the server, asking it to send a copy of the website to the client. This message, and all other data sent between the client and the server, is sent across your internet connection using TCP/IP.
3. If the server approves the client's request, the server sends the client a "200 Ok" message, and then starts sending the website's files to the browser as a series of data packets.
4. The browser assembles the packets to complete the web page.

#### *Order which component files are parsed*

1. The browser parses the HTML file first, and that leads the browser recognizing any `<link>` element references to external CSS stylesheets and any `<script>` element references to scripts.
2. These links trigger additional requests to the server.
3. The browser generates an in-memory DOM tree from the parsed HTML, generates an in-memory CSSOM structure from the parsed CSS, and compiles and executes the parsed JavaScript.
4. As the browser builds the DOM tree and applies the styles from the CSSOM tree and executes the JS, a visual representation is painted to the screen.

___

### [What will your website look like?](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/What_will_your_website_look_like)

#### *Steps to Building A Website*

1. Planning
    - What is the purpose? What is it about?
2. Sketching out a design
    - Create a general outline and map your website.
3. Choosing your assets
    - Text: write out paragraphs and articles that will be on your page.
    - Colors: [Color Picker Tool](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Colors/Color_picker_tool)
    - Images: [Google Images](https://www.google.com/imghp?gws_rd=ssl)
    - Fonts: [Google Fonts](https://fonts.google.com/)

___

### [JavaScript Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics)

JavaScript is a programming language that can add interactivity to a website.

#### *Important features*

1. Browser **A**pplication **P**rogramming **I**nterfaces (**API**s) built into browsers, providing functionality such as dynamically creating HTML and setting CSS styles; collecting and manipulating video from user's webcams, or generating 3D graphics and audio samples.
2. Third-Party APIs that allow developers to incorporate functionality in sites from other content providers. (i.e. Twitter and Facebook).
3. Third-Party frameworks and libraries that you an apply to HTML to accelerate the work of building sites and applications.

#### *Code examples*

How to link your .js files to your HTML document:

- `<script src="scripts/main.js"></script>`

Creates a "Hello world!" h1 heading:

- `const myHeading = document.querySelector("h1");`
- `myHeading.textContent = "Hello world!";`
  - Explainer: the function `querySelector()` grabs a reference to the heading, and then stores it in a variable called `myHeading`. This is similar to how CSS selectors work. Meaning, when you want to do something to an element, you need to select it first.
  - Following that, the code set the value of the `myHeading` variable's `textContent` property (which represents the content of the heading) to "Hello world!".

Variables can be created in this manner:

- `let myVariable;`
  - This creates the variabel "myVariable"
- `myVariable = "Bob";`
  - This sets the value of `myVariable` as `"Bob"` which is a string.
- `let myVariable = "Bob";`
  - You can create and assign a value to your variable on the same line.
- `myVariable;`
  - This would retrieve the value by calling the variable name.

#### **Data Types**

- String
  - `let myVariable = 'Bob';`
  - `let myVariable = "Bob";`
- Number
  - `let myVariable = 10;`
- Boolean
  - `let myVariable = true;`
- Array
  - `let myVariable = [1, 'Bob', 'Steve', 10];`
  - Refere to each member of the array like this: `myVariable[0]`, `myVariable[1]`
- Object
  - `let myVariable = document.querySelector('h1');`

#### **Operators**

- Assignment
  - `=` , assigns a value to a variable.
- Strict equality
  - `===` , tests whether the two values are equal and of the same data type.
- Not, Does-not-equal
  - `!` , `!==` , this returns the logically opposite value of what it preceds.
  - For "Not" the basic expression is `true` but the comparison returns `false`:
    - `let myVariable = 3;`
    - `!(myVariable === 3);`
  - "Does-not-equal" gives basically the same result with different syntax. Here we are testing "is `myVariable` NOT equal to 3". This returns `false` because `myVariable` IS equal to 3:
    - `let myVariable = 3;`
    - `myVariable !== 3;`

#### **Conditionals**

Conditionals are code structures used to test if an expression returns true or not. A very common form of conditionals is the if...else statement. For example:

    let iceCream = "chocolate";
    if (iceCream === "chocolate") {
      alert("Yay, I love chocolate ice cream!");
    } else {
      alert("Awwww, but chocolate is my favorite…");
    }

#### **Functions**

Functions are a way of packaging functionality that you wish to reuse. It's possible to define a body of code as a function that executes when you call the function name in your code. This is a good alternative to repeatedly writing the same code. You have already seen some uses of functions. For example:

    let myVariable = document.querySelector("h1");
    alert("hello!");

#### **Events**

Real interactivity on a website requires event handlers. These are code structures that listen for activity in the browser, and run code in response. The most obvious example is handling the click event, which is fired by the browser when you click on something with your mouse. To demonstrate this, enter the following into your console, then click on the current webpage:

    document.querySelector("html").addEventListener("click", function () {
      alert("Ouch! Stop poking me!");
    });

#### **Adding an image changer**

In this section, you will learn how to use JavaScript and DOM API features to alternate the display of one of two images. This change will happen as a user clicks the displayed image.

1. Choose an image you want to feature on your example site. Ideally, the image will be the same size as the image you added previously, or as close as possible.
2. Save this image in your images folder.
3. Rename the image firefox2.png.
4. Add the following JavaScript code to your main.js file.

*Code Examples:*

    const myImage = document.querySelector("img");

    yImage.onclick = () => {
      const mySrc = myImage.getAttribute("src");
      if (mySrc === "images/firefox-icon.png") {
        myImage.setAttribute("src", "images/firefox2.png");
      } else {
        myImage.setAttribute("src", "images/firefox-icon.png");
      }
    };

#### **Adding a personalized welcome message**

Heres how this can be done via `querySelector` and `eventListener`

- In index.html, add the following line just before the `<script>` element:

      <button>Change user</button>

- In `main.js`, place the following code at the bottom of the file, exactly as it is written. This takes references to the new button and the heading, storing each inside variables:

      let myButton = document.querySelector("button");
      let myHeading = document.querySelector("h1");

- Add the following function to set the personalized greeting. This won't do anything yet, but this will change soon.

      function setUserName() {
        const myName = prompt("Please enter your name.");
        localStorage.setItem("name", myName);
        myHeading.textContent = `Mozilla is cool, ${myName}`;
      }

- The `setUserName()` function contains a `prompt()` function, which displays a dialog box, similar to `alert()`. This `prompt()` function does more than `alert()`, asking the user to enter data, and storing it in a variable after the user clicks OK. In this case, we are asking the user to enter a name. Next, the code calls on an API `localStorage`, which allows us to store data in the browser and retrieve it later. We use localStorage's `setItem()` function to create and store a data item called `'name'`, setting its value to the `myName` variable which contains the user's entry for the name. Finally, we set the `textContent` of the heading to a string, plus the user's newly stored name.
- Add the following condition block. We could call this initialization code, as it structures the app when it first loads.

      if (!localStorage.getItem("name")) {
        setUserName();
      } else {
        const storedName = localStorage.getItem("name");
        myHeading.textContent = `Mozilla is cool, ${storedName}`;
      }

  - This first line of this block uses the negation operator (logical NOT, represented by the `!`) to check whether the `name` data exists. If not, the `setUserName()` function runs to create it. If it exists (that is, the user set a user name during a previous visit), we retrieve the stored name using `getItem()` and set the `textContent` of the heading to a string, plus the user's name, as we did inside `setUserName()`.
- Put this `onclick` event handler (below) on the button. When clicked, `setUserName()` runs. This allows the user to enter a different name by pressing the button.

      myButton.onclick = () => {
        setUserName();
      };

___

### [Introduction to HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML)


___

### [Getting started with HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started)


___

### [Document and website structure](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)


___

### [What's in the head? Metadata in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)


___

### [How do I start to design my website?](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Design_and_accessibility/Thinking_before_coding)


___

### [Semantics](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)


___

### [What is JavaScript?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript)


___
