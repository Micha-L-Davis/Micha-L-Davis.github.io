# Code 201 Reading Notes

Notes from assigned readings for CodeAcademy's **Code 201: Foundations of Software Development** course (Jan 10-28, 2022).

## Contents

1. [Introductory HTML and JavaScript](README.md#introductory-html-and-javascript)
2. [HTML Text, CSS Introduction, and Basic JavaScript Instructions](README.md#html-text-css-introduction-and-basic-javascript-instructions)
3. [HTML Lists, CSS Boxes, JS Control Flow](README.md#html-lists-css-boxes-js-control-flow)
4. [HTML Links, CSS Layout, JS Functions](README.md#html-links-css-layout-js-functions)
5. [HTML Images; CSS Color & Text](README.md#html-images-css-color--text)
6. [JS Object Literals; The DOM](README.md#js-object-literals-the-dom)
7. [HTML Tables; JS Constructor Functions](README.md#html-tables-js-constructor-functions)
8. [More CSS Layout](README.md#more-css-layout)
9. [Forms and Events](README.md#forms-and-events)
10. [JS Debugging](README.md#js-debugging)
11. [Assorted Topics](README.md#assorted-topics)
12. [Docs for the HTML \<canvas\> Element & Chart.js](README.md#docs-for-the-html-canvas-element--chartjs)
13. [Local Storage](README.md#local-storage)
14. [CSS Transforms, Transitions, and Animations](README.md#css-transforms-transitions-and-animations)
15. [What Google Learned About Teams](README.md#what-google-learned-about-teams)

---

## Introductory HTML and JavaScript

### HTML Chapter 1: Structure

  An HTML page is a text document that uses special tags to enhance the text within them in some way. These tags usually come in pairs, with opening and closing tags. The opening tag can define a named attribute, the value of which adds additional context to the function of the tag.
  
  The structure of a page is defined by the placement of tags.  The common tags that for the code of most pages include:
* `<html>` - indicates to the browser that the code between the tags is HTML code.
* `<head>` - contains information about the page, including the \<title\> tag.
* `<body>` - holds the visible elements of the web page.  Everything in this tag will be rendered by the browser.

### HTML Chapter 8: Extra Markup

  The structure of a page can further be ordered using the following tags and attributes:
  
* `<div>` and `<span>` - group block-level and inline elements together (respectively).
* `<iframes>` - creates a web page embedded within a web page.
* `id` and `class` attributes - can be added to any tag, and give the content within the tag a named grouping which can be referenced by other code.

  Additional information can also be added to the page by including:
  
* A `<!DOCTYPE>` dcelaration - to indicate the version of HTML used by the document.
* `<meta>` tags - allows for numerous types of data about a page, including a description of the page and keywords related to the page's content.
* `<!--**` and `**-->` markers - enclose text that will not be parsed by the web browser. This can be used for human-read comments and to temporarily 0remove sections of code for debugging.

### HTML Chapter 17: HTML5 Layout

  The latest version of HTML contains new tags for establishing the layout of a webpage.  These standards are evolving, but are already in use. The major difference in layout is replacing `<div>` tags with properties identifying the grouping's purpose with simplified tags that achieve the same result and mirror common website design trends.  The new tags are:

* `<header>` and `<footer\>` - for content that goes at the top and bottom of every page.
* `<nav>` - contains the sites primary navigation links.
* `<article>` - indicates a section of content which could potentially stand alone. A page may contain several, and these tags can be nested to indicate associated information.
* `<aside>` - inside an `<article>` element, it should contain additional information related to the content of the article.  Elsewhere, it should contain additional information related to the entire page.
* `<section>` - provides another way to group content on a page, either by collecting pieces of content together or by spreading out large content over multiple areas.
* `<hgroup>` - groups header content together so it can be treated as a single piece of content regardless of the size of the headers within. Good for subtitles.
* `<figure>` - used to contain content referenced from the main flow of an article. Examples: images, videos, graphs, diagrams, code samples, supporting text

Note: using these tags requires additional JavaScript in order for the content to be displayed properly by older browsers: *http://html5shiv.googlecode.com/svn/trunk/html5.js*

### HTML Chapter 18: Process & Design

  Certain information is crucial to obtain before designing a site, including:

* Target audience
* Purpose for the audience to engage with the site
* What information the audience will want
* Expected frequency of visits from audience members

  A site can be planned using a *site map* which shows the relationships between content pages, and a *wireframe* which illustrates the layout of content on a given page. In order to effectively communicate, the content on the site should be organized using principles of [visual hierarchy](https://xd.adobe.com/ideas/process/information-architecture/visual-hierarchy-principles-examples/). Keep the presentation of information simple by grouping content of a similar type or subject.

### JS Chapter 1: The ABC of Programming

#### A: What is a script and how do I create one?
  A script is a series of instructions read line by like by a computer in order to perform a task. In order for a computer to accomplish any task it must be told every minute step along the way.  To peform tasks with a computer it is necessary to break large tasks into smaller, specific sub tasks. This is often done with a [flowchart](https://mundrisoft.com/tech-bytes/flowchart-in-software-engineering-testing/).
  
#### B: How do computers fit in with the world around them?
  Computers rely on using data to form a model of a given object. Each object can have properties that contain data about the object, methods which provide instructions for performing specific tasks using those properties, and events which interpret a user's interactions with the computer into responses from the model.
  In order to make a web page interactable, the code of a script uses a model of the web page based on the HTML tags present within it.
  
#### C: How do I write a script for a web page?
  JavaScript files are text files, just like HTML files. They use the .js file extension. The HTML \<script\> tag is used to indicate the place where the browser should execute the script file. JavaScript does not alter the HTML file when it executes; rather, it changes the live presentation of a site natively within the browser itself.

---

## HTML Text, CSS Introduction, and Basic JavaScript Instructions

### HTML Chapter 2: Text

HTML tags can be used to structure the page into headings and paragraphs.  There are six levels of heading in HTML, (H1 - H6) each smaller compared to the last. Paragraphs are each shown on a new line by default, with a small amount of space between them. I new line can be made in the middle of a paragraph with the \<br /> tag. A horizontal line can be drawn between elements on the page with the \<hr /> tag.

HTML tags can also be used to provide semantic information.  Below is a list of some of these tags:

* `<strong>` - emboldens text
* `<em>` - italicizes text
* `<blockquote>` - to show a block of quoted text
* `<q>` - for shorter quotes
* `<abbr>` - to show the meaning of an abbreviation, initialism, or acronym
* `<cite>` - to show the source for a particular piece of text
* `<dfn>` - to show the definition of a new term
* `<address>` - contains contact information for the page author
* `<ins>` and `<del>` -  to show when content has been removed or added
* `<s>` - to show content has been removed

### HTML Chapter 10: Introducing CSS

CSS is a way to group content on a page to add styling and layout specific to that group. This is done by using a **selector** to specify a particular element or range of elements.  There are many kinds of selectors, here are three common ones:

* Type selectors - these specify a specific kind of element to style, such as `h1`or `p`.  This will style all elements of a given type
* Class selectors - these styles act on all elements with the given class property
* ID selectors - this will target the element with the given unique id.

Style declarations are formed by first indicating the name of the property to modify, such as the `font-family`, and the value to assign to the property.

### JS Chapter 2: Basic JavaScript Instructions

A script contains a series of instructions called 'statements.' These statements must cover every detail of the work to be done. To facilitate this, we can declare _variables_ which act as containers for data. Data can be added to, removed from or modified within a variable. When a script requires the data in a variable, it can ask for it by name.

Variables can also be made into _arrays_, which are containers that can hold multiple data values of the same type.  JavaScript recognizes three basic types: numbers, strings and boolean values.

We can also create _expressions_, which are statements which result in a single value.  This can be as simple as assigning a value to a variable, or a complex evaluation of multiple values using _operators_ such as `=`, `*`, `+`, `>` and `&&`.

### JS Chapter 4: Decisions and Loops

The program can make logical evaluations to decide what part of the code to run. This is typically done with an `if... else` statement. These statements allow us to use conditional operators to evaluate a set of values.  If the evaluation is `true` then whatever is enclosed within the `if` statement will run--otherwise it will run whatever does is found within the `else` statement (if present), or the next line of code after the `if` statement (if not).

If the logical evaluations for a given condition are too numerous, we can instead use a `switch` statement.  The switch evaluates a variable and compares it to case conditions.  If the condition is satisfied, the code within that case is run.  At the end of each case is a `break` statement that ends the execution of code within the switch.

---

## HTML Lists, CSS Boxes, JS Control Flow

### HTML Chapter 3: Lists

Content can be organized into lists in three ways: 

* Ordered List `<ol>` - produces a numbered list. List items are enclosed in `<li>` tags.
* Unordered List `<ul>` - produces a bulleted list. List items are enclosed in `<li>` tags.
* Definition List `<dl>` - produces a list of terms and their meanings. Terms are enclosed within `<dt>` tags, and definitions are enclosed whithin `<dd>` tags.

Lists can be nested within one another by putting a new list inside an existing list item element.

### HTML Chapter 13: Boxes

Each HTML element has properties which can manipulate the attributes of the box containing it. Most values can be set in absolute pixels, as a percentage of the browser window's (or containing box's) total width, based on the size of the text within the box with ems, among other units of measure.

* Dimension - `width` and `height` set the dimensions of the box
* Border - `border-width` draws the border at the given width
* Padding -  `padding` adds space between the border of a box and its content
* Margin - `margin` add space between a box and the edges of the screen or adjacent boxes

Elements can be hidden by applying a `visibility` property. This will hide the box and everything within it, but leaves a space in its place. To hide an element and collapse other elements into the space it would otherwise leave, the `display` property can be set to `none`.  The `display` property can also be used to reogranize block content into inline content (or vice versa) with the `inline` and `block` values. 

### CSS Chapter 4: Decisions and Loops (revisited)

JS is loosely typed, and will not necessarily throw an error if a variable has an unexpected type for the operation in which it is used. JS will use _type coercion_ to attempt to convert an unexpected type into the expected type.  This can lead to some unexpected results.  It is therefore recommended to use strict equality `===` to ensure that type coercion doesn't [play telephone](https://www.thefreedictionary.com/Game+of+telephone) with a variable's value.

Because of this flexibility, any value can be evaluated as `true` or `false` by a boolean condition. This leads to _truthiness_ and _falsiness_, making another case for using strict equality in most conditional evaluations.

JS has three different kinds of loops.
* `for` - is best used for looping through the values of an array. The loop increases an iterator with each loop, and terminates the loop when the iterator reaches a defined limit.
* `while` - continues to loop as long as a given value evaluates to true--potentially forever. Dangerous magic.
* `do...while` - similar to `while` but it performs the code block designated by `do` before evaluating the `while` conditional. This guarantees at least one run through the code, even if the condition was false from the start.

---

## HTML Links, CSS Layout, JS Functions

### HTML Chapter 4: Links

Links are essential to the worldwide web. A link is created with the `<a>` tag and the address the link references is assigned via the `href` property.  Anything enclosed within the tag will link a user's browser to the address when it is clicked on. The addresses can be simple, such as a directory or file within the web site's file structure, or the address can be detailed and specific. 

One such specific form of address is a link to an email address.  These links are preceeded with `mailto:` followed by the email address. It is also possible to create a link to a place inside the currently open page using the `#` symbol followed by the name of an existing id property on the page.

### HTML Chapter 15: Layout

The boxes which contain HTML elements are considered inherently either _block-level_ (meaning it will organize itself vertically with respect to adjacent elements) or _inline_ (meaning it is contained within or beside a line of text). Block-level elements are the primary layout organizers, and can be nested within one another to form parent/child relationships which CSS can use when deciding how style is applied.

The position of elements on the page is dependent on the active _positioning scheme_ set in the element's `position` property. In some schemes, boxes can overlap. The `z-index` peoperty can be set to decide what element goes on top. Below are the possible schemes:

* Normal flow - default behavior.
* Relative positioning - shifts the element relative to where it should be in normal flow.
* Absolute positioning - takes the item out of normal flow and sets it to an absolute position relative to its parent.
* Fixed positioning - takes the item out of normal flow and sets it to an absolute position in the view window.
* Floating elements - takes the item out of normal flow and sets it to the far right or left side of its parent as a block-level element.

A page can be structured to have a fixed width by setting the width of elements in absolute pixels. Alternatively, the size of elements can be described in percentages, in which case the content will stretch to fit the window provided. Pages are typically between 960-1000 pixels wide.

### JS Chapter 3: Functions

A function is a set of instructions which can be called as needed to do a specific piece of work. Functions can be created either as an expression(fig 1) or as a declaration (fig 2).

<sub>fig 1. function expression</sub>
```js
let myFunction = function() {
  // code goes here, hon
}
```

<sub>fig 2. function declaration</sub>
```js
function myFunction() {
  // this space intentionally blank
}
```

Expression form is best used when the function will only be used within limited scope (like a method). It cannot be called unless it has already been loaded into memory. Conversely, a declared function will be recognized by the compiler before the first expressions are read from the script.

---

## HTML Images; CSS Color & Text

### Chapter 5: Images

Images can be added via the `<img>` tag, usually within a semantic `<figure>` element. The specific image to display is given via the `src` property. This can be a local file path or a URL. It is also important for accessibility reasons to include `alt` property values for all images that detail the contents of the image. Images should be saved at the size they will be displayed on the page. Acceptable image formats include:

* .jpg
* .gif
* .png

### Chapter 11: Color

Color is an important design aspect that helps the user empotionally connect with the experience you are attempting to provide. Color can be designated in three ways:

* RGBA - values for Red, Green, Blue and Alpha from 0 to 255
* HSLA - values for Hue (0-360), Saturation (0-100%), Lightness (0-100%) and Alpha (0.0-1.0)
* hexadecimal codes - six-figure hexadecimal codes usually preceeded with a #.
* name - many colors can be called by name, such as `red`, `light blue`, or `goldenrod`

Contrast between text and background is also an important accessibility feature.

### Chapter 12: Text

Text can be presented in a number of ways, included properties to designate the font, the size of text, the font weight, style, kerning, spacing, and more. Many fonts are widespread and commonly found on most computers.  Other fonts are rarer, so it is important to use common font families.

---

## JS Object Literals; The DOM

### Chapter 3: Object Literals

An object is a collection of variables and functions which can be used to model something--in the case of a website this would be the browser or the document it displays. The variables within an object are called the object's "properties" and the functions are called the object's "methods." There are many ways to create an object.  Perhaps the most common is with Literal Notation, as follows:

```js
let myObject = {
  propertyOne: "value 1",
  propertyTwo: 2,
  myMethod: function() {
    return propertyOne;
  };
```

The properties of an object can be accessed either via dot notation (such as `let myVariable = myObject.propertyTwo;`) or via bracket notation (as in `let myOtherVariable = myObject['propertyOne'];`). 

### Chapter 5: The DOM

When a web document is loaded, a series of objects is loaded into memory in the form of a tree representing all of the elements of the document.  This tree is called the Document Object Model (DOM).  JavaScript can use this model to access and change the contents and properties of any element in the document.

The DOM is comprised of nodes.  Each node can be of one of four types: document nodes, element nodes, attribute nodes and text nodes. Element nodes can be selected via a range of methods that identify an element based on its id, class, attributes, tag name, or using CSS selectors. If a query for a node could return a range of nodes, the query will always return a `NodeList`. Once an element node is selected, the properties or text witin the element can be modified.

---

## HTML Tables; JS Constructor Functions

---

## More CSS Layout

---

## Forms and Events

---

## JS Debugging

---

## Assorted Topics

---

## Docs for the HTML \<canvas\> Element & Chart.js

---

## Local Storage

---

## CSS Transforms, Transitions, and Animations

---

## What Google Learned About Teams
