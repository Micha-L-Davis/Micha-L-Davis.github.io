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
* **\<html\>** - indicates to the browser that the code between the tags is HTML code.
* **\<head\>** - contains information about the page, including the \<title\> tag.
* **\<body\>** - holds the visible elements of the web page.  Everything in this tag will be rendered by the browser.

### HTML Chapter 8: Extra Markup

  The structure of a page can further be ordered using the following tags and attributes:
  
* **\<div\>** and **\<span\>** - group block-level and inline elements together (respectively).
* **\<iframes\>** - creates a web page embedded within a web page.
* *id* and *class* attributes - can be added to any tag, and give the content within the tag a named grouping which can be referenced by other code.

  Additional information can also be added to the page by including:
  
* A **\<!DOCTYPE\>** dcelaration - to indicate the version of HTML used by the document.
* **\<meta\>** tags - allows for numerous types of data about a page, including a description of the page and keywords related to the page's content.
* **\<!--** and **--\>** markers - enclose text that will not be parsed by the web browser. This can be used for human-read comments and to temporarily 0remove sections of code for debugging.

### HTML Chapter 17: HTML5 Layout

  The latest version of HTML contains new tags for establishing the layout of a webpage.  These standards are evolving, but are already in use. The major difference in layout is replacing **\<div\>** tags with properties identifying the grouping's purpose with simplified tags that achieve the same result and mirror common website design trends.  The new tags are:

* **\<header\>** and **\<footer\>** - for content that goes at the top and bottom of every page.
* **\<nav\>** - contains the sites primary navigation links.
* **\<article\>** - indicates a section of content which could potentially stand alone. A page may contain several, and these tags can be nested to indicate associated information.
* **\<aside\>** - inside an \<article\> element, it should contain additional information related to the content of the article.  Elsewhere, it should contain additional information related to the entire page.
* **\<section\>** - provides another way to group content on a page, either by collecting pieces of content together or by spreading out large content over multiple areas.
* **\<hgroup\>** - groups header content together so it can be treated as a single piece of content regardless of the size of the headers within. Good for subtitles.
* **\<figure\>** - used to contain content referenced from the main flow of an article. Examples: images, videos, graphs, diagrams, code samples, supporting text

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

* \<strong> - emboldens text
* \<em> - italicizes text
* \<blockquote> - to show a block of quoted text
* \<q> - for shorter quotes
* \<abbr> - to show the meaning of an abbreviation, initialism, or acronym
* \<cite> - to show the source for a particular piece of text
* \<dfn> - to show the definition of a new term
* \<address> - contains contact information for the page author
* \<ins> and \<del> -  to show when content has been removed or added
* \<s> - to show content has been removed

### HTML Chapter 10: Introducing CSS

CSS is a way to group content on a page to add styling and layout specific to that group. This is done by using a **selector** to specify a particular element or range of elements.  There are many kinds of selectors, here are three common ones:

* Type selectors - these specify a specific kind of element to style, such as `h1`or `p`.  This will style all elements of a given type
* Class selectors - these styles act on all elements with the given class property
* ID selectors - this will target the element with the given unique id.

Style declarations are formed by first indicating the name of the property to modify, such as the `font-family`, and the value to assign to the property.

### JS Chapter 2: Basic JavaScript Instructions

A script contains a series of instructions called 'statements.' These statements must cover every detail of the work to be done. To facilitate this, we can declare _variables_ which act as containers for data. Data can be added to, removed from or modified within a variable. When a script requires the data in a variable, it can ask for it by name.

Variables can also be made into _arrays_, which are containers that can hold multiple data values of the same type.  JavaScript recognizes three basic types: numbers, strings and boolean values.

We can also create _expressions_, which are statements which result in a single value.  This can be as simple as assigning a value to a variable, or a complex evaluation of multiple values using _operators_ such as =, \*, +, > and &&.

### JS Chapter 4: Decisions and Loops

The program can make logical evaluations to decide what part of the code to run. This is typically done with an `if... else` statement. These statements allow us to use conditional operators to evaluate a set of values.  If the evaluation is `true` then whatever is enclosed within the `if` statement will run--otherwise it will run whatever does is found within the `else` statement (if present), or the next line of code after the `if` statement (if not).

If the logical evaluations for a given condition are too numerous, we can instead use a `switch` statement.  The switch evaluates a variable and compares it to case conditions.  If the condition is satisfied, the code within that case is run.  At the end of each case is a `break` statement that ends the execution of code within the switch.

---

## HTML Lists, CSS Boxes, JS Control Flow

---

## HTML Links, CSS Layout, JS Functions

---

## HTML Images; CSS Color & Text

---

## JS Object Literals; The DOM

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
