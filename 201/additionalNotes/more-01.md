# CF 201 Class 01 Additional Notes

## [Getting Started with the Web](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)

### *Guides*

- Installing basic software
- What will your website look like?
- Dealing with files
- HTML Basics
- CSS Basics
- JavaScript Basics
- Publishing your website
- How the Web Works

___

## [How the Web Works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works)

### *Covered Materials*

- Clients and Servers: The web works on a basic principle of Clients making requests to Servers and Servers sending responses to Cients.
- TCP/IP: Transmission Control Protocol and Internet Protocol.
- DNS: Domain Name System.
- HTTP: Hypertext Transfer Protocol.
- Code Files: HTML, CSS, JavaScript
- Assets: images, music, video, documents

### *Order of Operations*

1. The browser goes to the DNS server, and finds the real address of the server that the website lives on.
2. The browser sends an HTTP request message to the server, asking it to send a copy of the website to the client. This message, and all other data sent between the client and the server, is sent across your internet connection using TCP/IP.
3. If the server approves the client's request, the server sends the client a "200 Ok" message, and then starts sending the website's files to the browser as a series of data packets.
4. The browser assembles the packets to complete the web page.

### *Order which component files are parsed*

1. The browser parses the HTML file first, and that leads the browser recognizing any `<link>` element references to external CSS stylesheets and any `<script>` element references to scripts.
2. These links trigger additional requests to the server.
3. The browser generates an in-memory DOM tree from the parsed HTML, generates an in-memory CSSOM structure from the parsed CSS, and compiles and executes the parsed JavaScript.
4. As the browser builds the DOM tree and applies the styles from the CSSOM tree and executes the JS, a visual representation is painted to the screen.

___

## [What will your website look like?](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/What_will_your_website_look_like)

### *Steps to Building A Website*

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

## [JavaScript Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics)

JavaScript is a programming language that can add interactivity to a website.

### *Important features*

1. Browser **A**pplication **P**rogramming **I**nterfaces (**API**s) built into browsers, providing functionality such as dynamically creating HTML and setting CSS styles; collecting and manipulating video from user's webcams, or generating 3D graphics and audio samples.
2. Third-Party APIs that allow developers to incorporate functionality in sites from other content providers. (i.e. Twitter and Facebook).
3. Third-Party frameworks and libraries that you an apply to HTML to accelerate the work of building sites and applications.

### *Code examples*

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

### **Data Types**

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

### **Operators**

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

### **Conditionals**

Conditionals are code structures used to test if an expression returns true or not. A very common form of conditionals is the if...else statement. For example:

    let iceCream = "chocolate";
    if (iceCream === "chocolate") {
      alert("Yay, I love chocolate ice cream!");
    } else {
      alert("Awwww, but chocolate is my favorite…");
    }

### **Functions**

Functions are a way of packaging functionality that you wish to reuse. It's possible to define a body of code as a function that executes when you call the function name in your code. This is a good alternative to repeatedly writing the same code. You have already seen some uses of functions. For example:

    let myVariable = document.querySelector("h1");
    alert("hello!");

### **Events**

Real interactivity on a website requires event handlers. These are code structures that listen for activity in the browser, and run code in response. The most obvious example is handling the click event, which is fired by the browser when you click on something with your mouse. To demonstrate this, enter the following into your console, then click on the current webpage:

    document.querySelector("html").addEventListener("click", function () {
      alert("Ouch! Stop poking me!");
    });

### **Adding an image changer**

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

### **Adding a personalized welcome message**

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

## [Introduction to HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML)

___

## [Getting started with HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started)

### *Elements*

`<p>This is a paragraph Element</p>`

#### *Anatomy of an HTML Element*

![Anatomy of an HTML Element](elementAnatomy.png)

`<em></em>` : Emphasis Tag

- <em>Emphasis Tag</em> :: Produces Italics

`<p></p>` : Paragraph Tag , separates a section as its own paragraph and forces a line break at the end.

- <p>Paragraph Tag</p> 

*<u>Nested Elements</u>*

`<p>Within this paragraph is a <strong>nested</strong> element</p>` : an element within an element. also `<strong>` creates a bold section.

- <p>Within this paragraph is a <strong>nested</strong> element</p>

*<u>Void Elements</u>*

Not all elements follow the pattern of an opening tag, content, and closing tag. Some cosist of a single tag, which is typically used to insert/embed something in the document. Such elements are called *<u>Void Elements</u>*. For example, the `<img>` element embeds an image file onto the page:

    <img
      src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png"
      alt="Firefox icon" />

*Attributes*

![HTML Attributes](attributesHTML.png)

Attributes contain extra information about the element that won't appear in the content. In this example, the `class` attribute is an identifying name used to target the element with style information.

Attributes should have:

- A space between it and the element name. Elements with more than one attribute have spaces separating the attributes.
- The attribute name, followed by an equal sign.
- An attribute value, wrapped with opening and closing quote marks.

### ***Common Attribues***

`href` : this attribute's value specifies the web address for the link.

    href="https://www.mozilla.org/"

`title` : The `title` attribute specifies extra information about the link, such as a description of the page that is being linked to. For example `title="The Mozilla homepage"`. This appears as a tooltip when a cursor hovers over the element.

`target` : The `target` attribute specifies the browsing context to display the link. For example, `target="_blank"` will display the link in a new tab. If you want to display the linked content in the current tab, just omit this attribute.

#### <u>*Boolean Attributes*</u>

`disabled` attribute: `<input type="text" disabled="disabled" />`

    <!-- using the disabled attribute prevents user from entering text into input box -->
    <input type="text" disabled />
    
    <!-- text input is allowed, as it doesn't contain the disabled attribute -->
    <input type="text" />

#### *Ommiting Quotes*

`<a href=https://www.mozilla.org/>`favorite website`</a>`

*Adding quotes and other attributes properly:*

    <a href="https://www.example.com" title="Isn't this fun?">
    A link to my example.
    </a>

- This format would produce the following: <a href="https://www.google.com" title="Isn't this fun?">A link to Google.</a>

## <u>HTML Anatomy</u>

    <!DOCTYPE html>
    <html lang="en-US">
      <head>
        <meta charset="utf-8" />
        <title>My test page</title>
      </head>
      <body>
        <p>This is my page</p>
      </body>
    </html>

1. `<!DOCTYPE html>` : The doctype. When HTML was young (1991-1992), doctypes were meant to act as links to a set of rules that the HTML page had to follow to be considered good HTML. Doctypes used to look something like this:

        <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

    More recently, the doctype is a historical artifact that needs to be included for everything else to work right. `<!DOCTYPE html>` is the shortest string of characters that counts as a valid doctype. That is all you need to know!

2. `<html></html>`: The `<html>` element. This element wraps all the content on the page. It is sometimes known as the root element.
3. `<head></head>`: The `<head>` element. This element acts as a container for everything you want to include on the HTML page, that isn't the content the page will show to viewers. This includes keywords and a page description that would appear in search results, CSS to style content, character set declarations, and more. You will learn more about this in the next article of the series.
4. `<meta charset="utf-8">`: The `<meta>` element. This element represents metadata that cannot be represented by other HTML meta-related elements, like `<base>`, `<link>`, `<script>`, `<style>` or `<title>`. The charset attributes sets the character set for your document to UTF-8, which includes most characters from the vast majority of human written languages. With this setting, the page can now handle any textual content it might contain. There is no reason not to set this, and it can help avoid some problems later.
5. `<title></title>`: The `<title>` element. This sets the title of the page, which is the title that appears in the browser tab the page is loaded in. The page title is also used to describe the page when it is bookmarked.
6. `<body></body>`: The `<body>` element. This contains all the content that displays on the page, including text, images, videos, games, playable audio tracks, or whatever else.

|Literal Character|Character reference equivalent|
|:---------------:|:----------------------------:|
|       <         |              &lt;            |
|       >         |              &gt;            |
|       "         |             &quot;           |
|       '         |             &apos;           |
|       &         |              &amp;           |

___

### [Document and website structure](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)

## Basic sections of a document

Header: Usually a big strip across the top with a big heading, logo, and perhaps a tagline. This usually stays the same from one webpage to another.

Navigation Bar: Links to the site's main sections; usually represented by menu buttons, links, or tabs. Like the header, this content usually remains consistent from one webpage to another — having inconsistent navigation on your website will just lead to confused, frustrated users. Many web designers consider the navigation bar to be part of the header rather than an individual component, but that's not a requirement; in fact, some also argue that having the two separate is better for accessibility, as screen readers can read the two features better if they are separate.

Main Content: A big area in the center that contains most of the unique content of a given webpage, for example, the video you want to watch, or the main story you're reading, or the map you want to view, or the news headlines, etc. This is the one part of the website that definitely will vary from page to page!

Sidebar: Some peripheral info, links, quotes, ads, etc. Usually, this is contextual to what is contained in the main content (for example on a news article page, the sidebar might contain the author's bio, or links to related articles) but there are also cases where you'll find some recurring elements like a secondary navigation system.

Footer: A strip across the bottom of the page that generally contains fine print, copyright notices, or contact info. It's a place to put common information (like the header) but usually, that information is not critical or secondary to the website itself. The footer is also sometimes used for SEO purposes, by providing links for quick access to popular content.

## [HTML Elements Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

***Important tags for the structure.***

- header: `<header>`.
- navigation bar: `<nav>`.
- main content: `<main>`, with various content subsections represented by `<article>`, `<section>`, and `<div>` elements.
- sidebar: `<aside>`; often placed inside `<main>`.
- footer: `<footer>`.

## HTML layout elements in more detail (Semantic Tags)

- `<main>` is for content unique to this page. Use `<main>` only once per page, and put it directly inside `<body>`. Ideally this shouldn't be nested within other elements.
- `<article>` encloses a block of related content that makes sense on its own without the rest of the page (e.g., a single blog post).
- `<section>` is similar to `<article>`, but it is more for grouping together a single part of the page that constitutes one single piece of functionality (e.g., a mini map, or a set of article headlines and summaries), or a theme. It's considered best practice to begin each section with a heading; also note that you can break `<article>`s up into different `<section>`s, or `<section>`s up into different `<article>`s, depending on the context.
- `<aside>` contains content that is not directly related to the main content but can provide additional information indirectly related to it (glossary entries, author biography, related links, etc.).
- `<header>` represents a group of introductory content. If it is a child of `<body>` it defines the global header of a webpage, but if it's a child of an `<article>` or `<section>` it defines a specific header for that section (try not to confuse this with titles and headings).
- `<nav>` contains the main navigation functionality for the page. Secondary links, etc., would not go in the navigation.
- `<footer>` represents a group of end content for a page.

### **Non-Semantic wrappers**

When either you can't find an ideal semantic element for a group or you just need to wrap some content together without that group having a semantic description.

`<div>` and `<span>` elements allow splitting a section and modifying with the `<class>` attribute to provide a label so they can be targeted by CSS and JS.

`<span>` is an inline non-semantic element, which you should use if a better semantic tag cannot be found, or don't want to add any specific meaning. Example:

    <p>
      The King walked drunkenly back to his room at 01:00, the beer doing nothing to
      aid him as he staggered through the door.
      <span class="editor-note">
        [Editor's note: At this point in the play, the lights should be down low].
      </span>
    </p>

`<div>` is a block level non-semantic element, which you should only use if you can't think of a better semantic block element to use, or donn't want to add any specific meaning. For example, imagine a shopping cart widget that you could choose to pull up at any point during your time on an e-commerce site:

    <div class="shopping-cart">
      <h2>Shopping cart</h2>
      <ul>
        <li>
          <p>
            <a href=""><strong>Silver earrings</strong></a>: $99.95.
          </p>
          <img src="../products/3333-0985/thumb.png" alt="Silver earrings" />
        </li>
        <li>…</li>
      </ul>
      <p>Total cost: $237.89</p>
    </div>

### Line breaks and Horizontal Rules

`<br>` : The line break element

    <p>
      There once was a man named O'Dell<br />
      Who loved to write HTML<br />
      But his structure was bad, his semantics were sad<br />
      and his markup didn't read very well.
    </p>

Output:

    There once was a man named O'Dell
    Who loved to write HTML
    But his structure was bad, his semantics were sad
    and his markup didn't read very well.

`<hr>` : the thematic break element. `<hr>` elements create a horizontal rule in the document that denotes a thematic change in the text (such as a change in topic or scene). Visually it looks lioke a horizontal line. Example:

    <p>
      Ron was backed into a corner by the marauding netherbeasts. Scared, but
      determined to protect his friends, he raised his wand and prepared to do
      battle, hoping that his distress call had made it through.
    </p>
    <hr />
    <p>
      Meanwhile, Harry was sitting at home, staring at his royalty statement and
      pondering when the next spin off series would come out, when an enchanted
      distress letter flew through his window and landed in his lap. He read it
      hazily and sighed; "better get back to work then", he mused.
    </p>

Renders as:

    Ron was backed into a corner by the marauding netherbeasts. Scared, but determined to protect his friends, he raised his wand and prepared to do battle, hoping that his distress call had made it through.
    __________________________________________________________________________________________________
    Meanwhile, Harry was sitting at home, staring at his royalty statement and pondering when the next spin off series would come out, when an enchanted distress letter flew through his window and landed in his lap. He read it hazily and sighed; "better get back to work then", he mused.

___

### [What's in the head? Metadata in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)

The head of an HTML document is the part that is not displayed in the web browser when the page is loaded. It contains information such as the page `<title>`, links to CSS (if you choose to style your HTML content with CSS), links to custom favicons, and other metadata (data about the HTML, such as the author, and important keywords that describe the document). Web browsers use information contained in the head to render the HTML document correctly. In this article we'll cover all of the above and more, in order to give you a good basis for working with markup.

### A few examples of `<head>` items

    <head>
      <meta charset="utf-8" />       //document's character encoding (language/typecase)
      <title>My test page</title>    //this title displays on the browser tab
    </head>

*Author and Description*

    <meta name="author" content="Chris Mills" />
    <meta
      name="description"
      content="The MDN Web Docs Learning Area aims to provide
    complete beginners to the Web with all they need to know to get
    started with developing websites and applications." />

*Discription in Search Engine Results*

    <meta
      name="description"
      content="The MDN Web Docs site
      provides information about Open Web technologies
      including HTML, CSS, and APIs for both websites and
      progressive web apps." />

![Meta: Description in SE](metaDataSE.png)

*Other types of Meta-data*

    <meta
      property="og:image"
      content="https://developer.mozilla.org/static/img/opengraph-logo.png" />
    <meta
      property="og:description"
      content="The Mozilla Developer Network (MDN) provides
    information about Open Web technologies including HTML, CSS, and APIs for both websites
    and HTML Apps." />
    <meta property="og:title" content="Mozilla Developer Network" />

![Other Meta-data](facebook-output.png)

## Adding custom icons to your site

To further enrich your site design, you can add references to custom icons in your metadata, and these will be displayed in certain contexts. The most commonly used of these is the favicon (short for "favorites icon", referring to its use in the "favorites" or "bookmarks" lists in browsers).

The humble favicon has been around for many years. It is the first icon of this type: a 16-pixel square icon used in multiple places. You may see (depending on the browser) favicons displayed in the browser tab containing each open page, and next to bookmarked pages in the bookmarks panel.

A favicon can be added to your page by:

1. Saving it in the same directory as the site's index page, saved in `.ico` format (most also support favicons in more common formats like `.gif` or `.png`)
2. Adding the following line into your HTML's `<head>` block to reference it:

        <link rel="icon" href="favicon.ico" type="image/x-icon" />

## Applying CSS nad JavaScript to HTML

- The `<link>` element should always go inside the head of your document. This takes two attributes, `rel="stylesheet"`, which indicates that it is the document's stylesheet, and `href`, which contains the path to the stylesheet file:

      <link rel="stylesheet" href="my-css-file.css" />

- The `<script>` element should also go into the head, and should include a `src` attribute containing the path to the JavaScript you want to load, and `defer`, which basically instructs the browser to load the JavaScript after the page has finished parsing the HTML. This is useful as it makes sure that the HTML is all loaded before the JavaScript runs, so that you don't get errors resulting from JavaScript trying to access an HTML element that doesn't exist on the page yet. There are actually a number of ways to handle loading JavaScript on your page, but this is the most reliable one to use for modern browsers (for others, read Script loading strategies).

      <script src="my-js-file.js" defer></script>

___

### [How do I start to design my website?](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Design_and_accessibility/Thinking_before_coding)

Find the Why & the What, the develp the How.
___

### [Semantics](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)

Semantics in programming: Semantics refers to the meaning of a piece of code — for example "what effect does running that line of JavaScript have?", or "what purpose or role does that HTML element have" (rather than "what does it look like?".)

Semantics in JavaScript: Consider a function that takes a string parameter, and returns an `<li>` element with that string as its `textContent`. Would you need to look at the code to understand what the function did if it was called `build('Peach')`, or `createLiWithContent('Peach')`?

Semantics in CSS: Consider styling a list with `li` elements representing different types of fruits. Would you know what part of the DOM is being selected with `div > ul > li`, or `.fruits__item`?

Semantics in HTML: for example, the h1 element is a semantic element, which gives the text it wraps around the role (or meaning) of "a top level heading on your page."

    <h1>This is a top level heading</h1>

By default, most browser's user agent stylesheet will style an h1 with a large font size to make it look like a heading (although you could style it to look like anything you wanted).

On the other hand, you could make any element look like a top level heading. Consider the following:

    <span style="font-size: 32px; margin: 21px 0;">Not a top-level heading!</span>

## Semantic Elements

### Main Root

| Element |      Description        |
|---------|-------------------------|
| `<html>`|Represents the root (top-level element) of an HTML document, so it is also referred to as the root element. All other elements must be descendants of this element.|

### Document Meta-Data

| Element |      Description        |
|---------|-------------------------|
|`<base>`|Specifies the base URL to use for all relative URLs in a document. There can be only one such element in a document.|
|`<head>`|Contains machine-readable information (metadata) about the document, like its title, scripts, and style sheets.|
|`<link>`|Specifies relationships between the current document and an external resource. This element is most commonly used to link to CSS, but is also used to establish site icons (both "favicon" style icons and icons for the home screen and apps on mobile devices) among other things.|
|`<meta>`|Represents metadata that cannot be represented by other HTML meta-related elements, like `<base>`, `<link>`, `<script>`, `<style>` and `<title>`.|
|`<style>`|Contains style information for a document, or part of a document. It contains CSS, which is applied to the contents of the document containing this element.|
|`<title>`|Defines the document's title that is shown in a browser's title bar or a page's tab. It only contains text; tags within the element are ignored.|

### Sectioning root

| Element |      Description        |
|---------|-------------------------|
|`<body>`|represents the content of an HTML document. There can be only one such element in a document.|

### Content Sectioning

| Element |      Description        |
|---------|-------------------------|
|`<address>`|Indicates that the enclosed HTML provides contact information for a person or people, or for an organization.|
|`<article>`|Represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). Examples include: a forum post, a magazine or newspaper article, or a blog entry, a product card, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.|
|`<aside>`|Represents a portion of a document whose content is only indirectly related to the document's main content. Asides are frequently presented as sidebars or call-out boxes.|
|`<footer>`|Represents a footer for its nearest ancestor sectioning content or sectioning root element. A `<footer>` typically contains information about the author of the section, copyright data or links to related documents.|
|`<header>`|Represents introductory content, typically a group of introductory or navigational aids. It may contain some heading elements but also a logo, a search form, an author name, and other elements.|
|`<h1>, <h2>, <h3>, <h4>, <h5>, <h6>`|Represent six levels of section headings. `<h1>` is the highest section level and `<h6>` is the lowest.|
|`<hgroup>`|Represents a heading grouped with any secondary content, such as subheadings, an alternative title, or a tagline.|
|`<main>`|Represents the dominant content of the body of a document. The main content area consists of content that is directly related to or expands upon the central topic of a document, or the central functionality of an application.|
|`<nav>`|Represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.|
|`<section>`|Represents a generic standalone section of a document, which doesn't have a more specific semantic element to represent it. Sections should always have a heading, with very few exceptions.|

### Text Content

| Element |      Description        |
|---------|-------------------------|
|`<blockquote>`|Indicates that the enclosed text is an extended quotation. Usually, this is rendered visually by indentation. A URL for the source of the quotation may be given using the cite attribute, while a text representation of the source can be given using the `<cite>` element.|
|`<dd>`|Provides the description, definition, or value for the preceding term (`<dt>`) in a description list (`<dl>`).|
|`<div>`|The generic container for flow content. It has no effect on the content or layout until styled in some way using CSS (e.g., styling is directly applied to it, or some kind of layout model like flexbox is applied to its parent element).|
|`<dl>`|Represents a description list. The element encloses a list of groups of terms (specified using the `<dt>` element) and descriptions (provided by `<dd>` elements). Common uses for this element are to implement a glossary or to display metadata (a list of key-value pairs).|
|`<dt>`|Specifies a term in a description or definition list, and as such must be used inside a `<dl>` element. It is usually followed by a `<dd>` element; however, multiple `<dt>` elements in a row indicate several terms that are all defined by the immediate next `<dd>` element.|
|`<figcaption>`|Represents a caption or legend describing the rest of the contents of its parent `<figure>` element.|
|`<figure>`|Represents self-contained content, potentially with an optional caption, which is specified using the `<figcaption>` element. The figure, its caption, and its contents are referenced as a single unit.|
|`<hr>`|Represents a thematic break between paragraph-level elements: for example, a change of scene in a story, or a shift of topic within a section.|
|`<li>`|Represents an item in a list. It must be contained in a parent element: an ordered list (`<ol>`), an unordered list (`<ul>`), or a menu (`<menu>`). In menus and unordered lists, list items are usually displayed using bullet points. In ordered lists, they are usually displayed with an ascending counter on the left, such as a number or letter.
|`<menu>`|A semantic alternative to `<ul>`, but treated by browsers (and exposed through the accessibility tree) as no different than `<ul>`. It represents an unordered list of items (which are represented by `<li>` elements).|
|`<ol>`|Represents an ordered list of items — typically rendered as a numbered list.
|`<p>`|Represents a paragraph. Paragraphs are usually represented in visual media as blocks of text separated from adjacent blocks by blank lines and/or first-line indentation, but HTML paragraphs can be any structural grouping of related content, such as images or form fields.|
|`<pre>`|Represents preformatted text which is to be presented exactly as written in the HTML file. The text is typically rendered using a non-proportional, or monospaced, font. Whitespace inside this element is displayed as written.|
|`<ul>`|Represents an unordered list of items, typically rendered as a bulleted list.|

### Inline text semantics

| Element |      Description        |
|---------|-------------------------|
|`<a>`|Together with its href attribute, creates a hyperlink to web pages, files, email addresses, locations in the same page, or anything else a URL can address.|
|`<abbr>`|Represents an abbreviation or acronym.|
|`<b>`|Used to draw the reader's attention to the element's contents, which are not otherwise granted special importance. This was formerly known as the Boldface element, and most browsers still draw the text in boldface. However, you should not use `<b>` for styling text or granting importance. If you wish to create boldface text, you should use the CSS font-weight property. If you wish to indicate an element is of special importance, you should use the strong element.|
|`<bdi>`|Tells the browser's bidirectional algorithm to treat the text it contains in isolation from its surrounding text. It's particularly useful when a website dynamically inserts some text and doesn't know the directionality of the text being inserted.|
|`<bdo>`|Overrides the current directionality of text, so that the text within is rendered in a different direction.|
|`<br>`|Produces a line break in text (carriage-return). It is useful for writing a poem or an address, where the division of lines is significant.|
|`<cite>`|Used to mark up the title of a cited creative work. The reference may be in an abbreviated form according to context-appropriate conventions related to citation metadata.v
|`<code>`|Displays its contents styled in a fashion intended to indicate that the text is a short fragment of computer code. By default, the content text is displayed using the user agent default monospace font.|
|`<data>`|Links a given piece of content with a machine-readable translation. If the content is time- or date-related, the time element must be used.|
|`<dfn>`|Used to indicate the term being defined within the context of a definition phrase or sentence. The ancestor `<p>` element, the `<dt>`/`<dd>` pairing, or the nearest section ancestor of the `<dfn>` element, is considered to be the definition of the term.|
|`<em>`|Marks text that has stress emphasis. The `<em>` element can be nested, with each level of nesting indicating a greater degree of emphasis.|
|`<i>`|Represents a range of text that is set off from the normal text for some reason, such as idiomatic text, technical terms, taxonomical designations, among others. Historically, these have been presented using italicized type, which is the original source of the `<i>` naming of this element.|
|`<kbd>`|Represents a span of inline text denoting textual user input from a keyboard, voice input, or any other text entry device. By convention, the user agent defaults to rendering the contents of a `<kbd>` element using its default monospace font, although this is not mandated by the HTML standard.|
|`<mark>`|Represents text which is marked or highlighted for reference or notation purposes due to the marked passage's relevance in the enclosing context.|
|`<q>`|Indicates that the enclosed text is a short inline quotation. Most modern browsers implement this by surrounding the text in quotation marks. This element is intended for short quotations that don't require paragraph breaks; for long quotations use the `<blockquote>` element.|
|`<rp>`|Used to provide fall-back parentheses for browsers that do not support display of ruby annotations using the `<ruby>` element. One `<rp>` element should enclose each of the opening and closing parentheses that wrap the `<rt>` element that contains the annotation's text.|
|`<rt>`|Specifies the ruby text component of a ruby annotation, which is used to provide pronunciation, translation, or transliteration information for East Asian typography. The `<rt>` element must always be contained within a `<ruby>` element.|
|`<ruby>`|Represents small annotations that are rendered above, below, or next to base text, usually used for showing the pronunciation of East Asian characters. It can also be used for annotating other kinds of text, but this usage is less common.|
|`<s>`|Renders text with a strikethrough, or a line through it. Use the `<s>` element to represent things that are no longer relevant or no longer accurate. However, `<s>` is not appropriate when indicating document edits; for that, use the del and ins elements, as appropriate.|
|`<samp>`|Used to enclose inline text which represents sample (or quoted) output from a computer program. Its contents are typically rendered using the browser's default monospaced font (such as Courier or Lucida Console).|
|`<small>`|Represents side-comments and small print, like copyright and legal text, independent of its styled presentation. By default, it renders text within it one font-size smaller, such as from small to x-small.|
|`<span>`|A generic inline container for phrasing content, which does not inherently represent anything. It can be used to group elements for styling purposes (using the class or id attributes), or because they share attribute values, such as lang. It should be used only when no other semantic element is appropriate. `<span>` is very much like a div element, but div is a block-level element whereas a `<span>` is an inline-level element.|
|`<strong>`|Indicates that its contents have strong importance, seriousness, or urgency. Browsers typically render the contents in bold type.|
|`<sub>`|Specifies inline text which should be displayed as subscript for solely typographical reasons. Subscripts are typically rendered with a lowered baseline using smaller text.|
|`<sup>`|Specifies inline text which is to be displayed as superscript for solely typographical reasons. Superscripts are usually rendered with a raised baseline using smaller text.|
|`<time>`|Represents a specific period in time. It may include the datetime attribute to translate dates into machine-readable format, allowing for better search engine results or custom features such as reminders.|
|`<u>`|Represents a span of inline text which should be rendered in a way that indicates that it has a non-textual annotation. This is rendered by default as a simple solid underline, but may be altered using CSS.|
|`<var>`|Represents the name of a variable in a mathematical expression or a programming context. It's typically presented using an italicized version of the current typeface, although that behavior is browser-dependent.|
|`<wbr>`|Represents a word break opportunity—a position within text where the browser may optionally break a line, though its line-breaking rules would not otherwise create a break at that location.|

### Image and Multimedia

| Element |      Description        |
|---------|-------------------------|
|`<area>`|Defines an area inside an image map that has predefined clickable areas. An image map allows geometric areas on an image to be associated with hyperlink.|
|`<audio>`|Used to embed sound content in documents. It may contain one or more audio sources, represented using the src attribute or the source element: the browser will choose the most suitable one. It can also be the destination for streamed media, using a MediaStream.|
|`<img>`|Embeds an image into the document.|
|`<map>`|Used with `<area>` elements to define an image map (a clickable link area).|
|`<track>`|Used as a child of the media elements, audio and video. It lets you specify timed text tracks (or time-based data), for example to automatically handle subtitles. The tracks are formatted in WebVTT format (.vtt files)—Web Video Text Tracks.|
|`<video>`|Embeds a media player which supports video playback into the document. You can use `<video>` for audio content as well, but the audio element may provide a more appropriate user experience.|

### Embedded Content

| Element |      Description        |
|---------|-------------------------|
|`<embed>`|Embeds external content at the specified point in the document. This content is provided by an external application or other source of interactive content such as a browser plug-in.|
|`<iframe>`|Represents a nested browsing context, embedding another HTML page into the current one.|
|`<object>`|Represents an external resource, which can be treated as an image, a nested browsing context, or a resource to be handled by a plugin.|
|`<picture>`|Contains zero or more `<source>` elements and one `<img>` element to offer alternative versions of an image for different display/device scenarios.|
|`<portal>`|Enables the embedding of another HTML page into the current one for the purposes of allowing smoother navigation into new pages.|
|`<source>`|Specifies multiple media resources for the picture, the audio element, or the video element. It is a void element, meaning that it has no content and does not have a closing tag. It is commonly used to offer the same media content in multiple file formats in order to provide compatibility with a broad range of browsers given their differing support for image file formats and media file formats.|

### SVG and MathML

| Element |      Description        |
|---------|-------------------------|
|`<svg>`|Container defining a new coordinate system and viewport. It is used as the outermost element of SVG documents, but it can also be used to embed an SVG fragment inside an SVG or HTML document.`
|`<math>`|The top-level element in MathML. Every valid MathML instance must be wrapped in it. In addition you must not nest a second `<math>` element in another, but you can have an arbitrary number of other child elements in it.`

### Scripting

| Element |      Description        |
|---------|-------------------------|
|`<canvas>`|Container element to use with either the canvas scripting API or the WebGL API to draw graphics and animations.|
|`<noscript>`|Defines a section of HTML to be inserted if a script type on the page is unsupported or if scripting is currently turned off in the browser.|
|`<script>`|Used to embed executable code or data; this is typically used to embed or refer to JavaScript code. The `<script>` element can also be used with other languages, such as WebGL's GLSL shader programming language and JSON.|

### Demarcating edits

| Element |      Description        |
|---------|-------------------------|
|`<del>`|Represents a range of text that has been deleted from a document. This can be used when rendering "track changes" or source code diff information, for example. The `<ins>` element can be used for the opposite purpose: to indicate text that has been added to the document.|
|`<ins>`|Represents a range of text that has been added to a document. You can use the `<del>` element to similarly represent a range of text that has been deleted from the document.|

### Table Content

| Element |      Description        |
|---------|-------------------------|
|`<caption>`|Specifies the caption (or title) of a table.|
|`<col>`|Defines a column within a table and is used for defining common semantics on all common cells. It is generally found within a `<colgroup>` element.|
|`<colgroup>`|Defines a group of columns within a table.|
|`<table>`|Represents tabular data — that is, information presented in a two-dimensional table comprised of rows and columns of cells containing data.|
|`<tbody>`|Encapsulates a set of table rows (`<tr>` elements), indicating that they comprise the body of the table (`<table>`).|
|`<td>`|Defines a cell of a table that contains data. It participates in the table model.|
|`<tfoot>`|Defines a set of rows summarizing the columns of the table.|
|`<th>`|Defines a cell as header of a group of table cells. The exact nature of this group is defined by the scope and headers attributes.|
|`<thead>`|Defines a set of rows defining the head of the columns of the table.|
|`<tr>`|Defines a row of cells in a table. The row's cells can then be established using a mix of `<td>` (data cell) and `<th>` (header cell) elements.|

### Forms

| Element |      Description        |
|---------|-------------------------|
|`<button>`|An interactive element activated by a user with a mouse, keyboard, finger, voice command, or other assistive technology. Once activated, it then performs an action, such as submitting a form or opening a dialog.|
|`<datalist>`|Contains a set of `<option>` elements that represent the permissible or recommended options available to choose from within other controls.|
|`<fieldset>`|Used to group several controls as well as labels (`<label>`) within a web form.|
|`<form>`|Represents a document section containing interactive controls for submitting information.|
|`<input>`|Used to create interactive controls for web-based forms in order to accept data from the user; a wide variety of types of input data and control widgets are available, depending on the device and user agent.
The `<input>` element is one of the most powerful and complex in all of HTML due to the sheer number of combinations of input types and attributes.|
|`<label>`|Represents a caption for an item in a user interface.|
|`<legend>`|Represents a caption for the content of its parent `<fieldset>`.|
|`<meter>`|Represents either a scalar value within a known range or a fractional value.|
|`<optgroup>`|Creates a grouping of options within a `<select>` element.|
|`<option>`|Used to define an item contained in a select, an `<optgroup>`, or a `<datalist>` element. As such, `<option>` can represent menu items in popups and other lists of items in an HTML document.|
|`<output>`|Container element into which a site or app can inject the results of a calculation or the outcome of a user action.|
|`<progress>`|Displays an indicator showing the completion progress of a task, typically displayed as a progress bar.|
|`<select>`|Represents a control that provides a menu of options.|
|`<textarea>`|Represents a multi-line plain-text editing control, useful when you want to allow users to enter a sizeable amount of free-form text, for example a comment on a review or feedback form.|

### Interactive Elements

| Element |      Description        |
|---------|-------------------------|
|`<details>`|Creates a disclosure widget in which information is visible only when the widget is toggled into an "open" state. A summary or label must be provided using the `<summary>` element.|
|`<dialog>`|Represents a dialog box or other interactive component, such as a dismissible alert, inspector, or subwindow.|
|`<summary>`|Specifies a summary, caption, or legend for a details element's disclosure box. Clicking the `<summary>` element toggles the state of the parent `<details>` element open and closed.|

### Web Components

| Element |      Description        |
|---------|-------------------------|
|`<slot>`|Part of the Web Components technology suite, this element is a placeholder inside a web component that you can fill with your own markup, which lets you create separate DOM trees and present them together.|
|`<template>`|A mechanism for holding HTML that is not to be rendered immediately when a page is loaded but may be instantiated subsequently during runtime using JavaScript.|

[Obselete and Deprecated Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#obsolete_and_deprecated_elements)
___

## [What is JavaScript?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript)

Example of Combining HTML, CSS, and JavaScript.

- HTML

      <p>Player 1: Chris</p>

  ![HTML Button](htmlPlayer1.png)

- CSS

      p {
        font-family: "helvetica neue", helvetica, sans-serif;
        letter-spacing: 1px;
        text-transform: uppercase;
        text-align: center;
        border: 2px solid rgb(0 0 200 / 0.6);
        background: rgb(0 0 200 / 0.6);
        color: rgb(255 255 255 / 1);
        box-shadow: 1px 1px 2px rgb(0 0 200 / 0.4);
        border-radius: 10px;
        padding: 3px 10px;
        display: inline-block;
        cursor: pointer;
      }
  ![CSS Button](cssPlayer1.png)
- JavaScript

      const para = document.querySelector("p");

      para.addEventListener("click", updateName);

      function updateName() {
        const name = prompt("Enter a new name");
        para.textContent = `Player 1: ${name}`;
      }
  |CSS + JS Button|Prompt to Change|JS Change to Name|
  |---------------|----------------|-----------------|
  |![JavaScript Button 1](jsPlayer1.png)|![JavaScript Button 2](jsPlayer1Entry.png)|![JavaScript Button 3](jsPlayer1Change.png)|

Browser APIs are built into your web browser, and are able to expose data from the surrounding computer environment, or do useful complex things. For example:

- The `DOM (Document Object Model) API` allows you to manipulate HTML and CSS, creating, removing and changing HTML, dynamically applying new styles to your page, etc. Every time you see a popup window appear on a page, or some new content displayed (as we saw above in our simple demo) for example, that's the DOM in action.
- The `Geolocation API` retrieves geographical information. This is how Google Maps is able to find your location and plot it on a map.
- The `Canvas` and `WebGL` APIs allow you to create animated 2D and 3D graphics. People are doing some amazing things using these web technologies — see Chrome Experiments and webglsamples.
- Audio and Video APIs like `HTMLMediaElement` and `WebRTC` allow you to do really interesting things with multimedia, such as play audio and video right in a web page, or grab video from your web camera and display it on someone else's computer (try our simple Snapshot demo to get the idea).
- The Twitter API allows you to do things like displaying your latest tweets on your website.
- The Google Maps API and OpenStreetMap API allows you to embed custom maps into your website, and other such functionality.

### JavaScript running order

When the browser encounters a block of JavaScript, it generally runs it in order, from top to bottom. This means that you need to be careful what order you put things in. For example, let's return to the block of JavaScript we saw in our first example:

    const para = document.querySelector("p");

    para.addEventListener("click", updateName);

    function updateName() {
      const name = prompt("Enter a new name");
      para.textContent = `Player 1: ${name}`;
    }

Here we are selecting a text paragraph (line 1), then attaching an event listener to it (line 3) so that when the paragraph is clicked, the `updateName()` code block (lines 5–8) is run. The `updateName()` code block (these types of reusable code blocks are called "functions") asks the user for a new name, and then inserts that name into the paragraph to update the display.

If you swapped the order of the first two lines of code, it would no longer work — instead, you'd get an error returned in the browser developer console — `TypeError: para is undefined`. This means that the `para` object does not exist yet, so we can't add an event listener to it.

### Internal JavaScript

1. First of all, make a local copy of our example file apply-javascript.html. Save it in a directory somewhere sensible.
2. Open the file in your web browser and in your text editor. You'll see that the HTML creates a simple web page containing a clickable button.
3. Next, go to your text editor and add the following in your head — just before your closing `</head>` tag:

        <script>
          // JavaScript goes here
        </script>

4. Now we'll add some JavaScript inside our `<script>` element to make the page do something more interesting — add the following code just below the "// JavaScript goes here" line:

        document.addEventListener("DOMContentLoaded", () => {
          function createParagraph() {
            const para = document.createElement("p");
            para.textContent = "You clicked the button!";
            document.body.appendChild(para);
          }

          const buttons = document.querySelectorAll("button");

          for (const button of buttons) {
            button.addEventListener("click", createParagraph);
          }
        });

5. Save your file and refresh the browser — now you should see that when you click the button, a new paragraph is generated and placed below.

### External JavaScript

1. First, create a new file in the same directory as your sample HTML file. Call it script.js — make sure it has that .js filename extension, as that's how it is recognized as JavaScript.
2. Replace your current `<script>` element with the following:

        <script src="script.js" defer></script>

3. Inside `script.js`, add the following script:

        function createParagraph() {
          const para = document.createElement("p");
          para.textContent = "You clicked the button!";
          document.body.appendChild(para);
        }

        const buttons = document.querySelectorAll("button");

        for (const button of buttons) {
          button.addEventListener("click", createParagraph);
        }

4. Save and refresh your browser, and you should see the same thing! It works just the same, but now we've got our JavaScript in an external file. This is generally a good thing in terms of organizing your code and making it reusable across multiple HTML files. Plus, the HTML is easier to read without huge chunks of script dumped in it.

### Using addEventListener instead

Instead of including JavaScript in your HTML, use a pure JavaScript construct. The `querySelectorAll()` function allows you to select all the buttons on a page. You can then loop through the buttons, assigning a handler for each using `addEventListener()`. The code for this is shown below:

    const buttons = document.querySelectorAll("button");
    
    for (const button of buttons) {
      button.addEventListener("click", createParagraph);
    }

This might be a bit longer than the `onclick` attribute, but it will work for all buttons — no matter how many are on the page, nor how many are added or removed. The JavaScript does not need to be changed.

**Note:** *Try editing your version of* `apply-javascript.html` *and add a few more buttons into the file. When you reload, you should find that all of the buttons when clicked will create a paragraph. Neat, huh?*

**Note:** *In the external case, we did not need to use the* `DOMContentLoaded` *event because the* `defer` *attribute solved the problem for us. We didn't use the* `defer` *solution for the internal JavaScript example because* `defer` *only works for external scripts.*

___
