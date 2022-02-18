# Code 301 Reading Notes

1. [Introduction to React and Components](code-301.md#introduction-to-react-and-components)
2. [State and Props](code-301.md#state-and-props)
3. [Passing Functions as Props](code-301.md#passing-functions-as-props)
4. [React and Forms](code-301.md#react-and-forms)
5. [Putting it all Together](code-301.md#putting-it-all-together)

---

# Introduction to React and Components

## Component-Based Architecture

 * A component is a modular, reusable software object that is designed to interoperate with other components.
 * The [characteristics of a component](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm#characteristics-of-components) are:
     * **Reusability**
     * **Replaceable**
     * **Not context specific**
     * **Extensible**
     * **Encapsulated**
     * **Independent**
 * The [advantages of component-based architecture](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm#advantages) are:
     * **Ease of deployment**
     * **Reduced cost**
     * **Ease of development**
     * **Reusable**
     * **Modification of technical complexity**
     * **Reliability**
     * **System maintenance and evolution**
     * **Independent**

## Props in React

* `props` is short for "properties"
* Props are used in React to pass information between React components
* Information is passed down from parent component to child components. 

## Things I want to know more about

* The additional features available to Function or Class components
* JSX in general

---

# State and Props

Based off [the diagram](https://miro.medium.com/max/1400/0*0saPKFiTUk6W3FYp), what happens first, the ‘render’ or the ‘componentDidMount’?
* the 'render'

What is the very first thing to happen in the lifecycle of React?
* the constructor is called in the Mounting phase

Put the following things in the order that they happen: 
* constructor 
* render 
* React Updates
* componentDidMount 
* componentWillUnmount 

What does componentDidMount do?
* it is a place to set instructions that require the component to be mounted before they are run, such as event subscriptions or network requests

What types of things can you pass in the props?
* static information that you don't expect to change

What is the big difference between props and state?
* Props are passed from without and cannot change, state is managed from within and is mutable

When do we re-render our application?
* Any time state changes

What are some examples of things that we could store in state?
* anything that may change through user interaction or that requires the component to be re-rendered

## Things I want to know more about
* state seems to be spoken of as if it is an object all its own--is there a state object, or are we just talking about the variables a component might use in general to manage internal data?

---

# Passing Functions as Props

## React Docs - lists and keys

* `.map()` returns a new array in which each element is the result of a callback function applied to each element of the source array.
* looping through an array in JSX is nearly identical as in JS.
* each list item needs a unique key.
* the purpose of the key is to help React know when items have changed.

## Spread operator

* The spread operator is a quick way to copy the data from an object or array and use it elsewhere
* Can be used:
    * in the place of arguments for a function call
    * in the place of elements in an array literal
    * in an object expression in place of key value pairs for an object literal
    * in place of `Function.prototype.apply()`
* To combine to arrays:
```
arrA = [...arrA, ...arrB];
```
* To add new items to an array:
```
let arrA = ['3', '2', '1']
let arrB = ['Ready?, ...arrA, 'Let's jam.']
```
* To combine two objects into one:
```
let combinedObj = { ...objA, ...objB } 
```

## How to pass functions between components

* The first step is to create the function within the object where the state that needs to change is located.
* In the [example video](https://www.youtube.com/watch?v=c05OL7XbwXU), the `increment` function takes a string argument and maps a state array through a callback function that increments the appropriate state object's `count` property based on the argument.
* A method is passed from a parent component to a child component as a prop.
* The method is invoked by accessing it from props through dot notation and initializing it.

## Things I want to know more about
* Nothing came to mind this time. It all seems pretty straightforward.

---

# React and Forms

## React Docs - Forms

* A 'Controlled Component' is an input form element whose value is controlled by React.
* The user's responses are stored as they are entered because the 'source of truth' for the input element's data is the React component state.
* If there is an event handler on an input field, in order to target what the user is entering we apply a name property to the elements, which we can reference through the `event` object.

## The Conditional (Ternary) Operator

* We use a ternary operator to shorthand and if/else statement.
* Example:
```
if(x===y){
  console.log(true);
} else {
  console.log(false);
}
```
becomes:
```
x === y ? console.log(true) : console.log(false);
```

## Things I want to know more about
* I have no further questions.

---

# Putting it all Together

## Thinking in React

* The **single responsibility principle** is a software engineering principle that states a software object should only ever have one reason to change.  In other words, it should exist in a state where it is only *responsible* for performing a *single* task. In terms of a React component, we should prefer creating a new component any time a new functionality must be added to the app, rather than adding that functionality to an existing component.  That way, if any one of those components needs to be edited it will likely only be for one reason--to ensure the sole responsibility of the component works correctly.
* A 'static' version of the application is made first primarily because the basic structure of a static application requires a lot of typing, but is not complex enough to require a lot of forethought. Conversely, interactivity involves making small, well thought-out additions to the code, and is therefore best saved for last.
* After building the static app, we must next identify the complete minimal representation of UI state.
* [Three questions you can ask to determine if something is state](https://reactjs.org/docs/thinking-in-react.html#step-3-identify-the-minimal-but-complete-representation-of-ui-state):
    * Is it passed in from a parent via props? If so, it probably isn’t state.
    * Does it remain unchanged over time? If so, it probably isn’t state.
    * Can you compute it based on any other state or props in your component? If so, it isn’t state
* [To determine where a piece of state should live](https://reactjs.org/docs/thinking-in-react.html#step-4-identify-where-your-state-should-live), for each piece of state in the app:
    * Identify every component that renders something based on that state.
    * Find a common owner component (a single component above all the components that need the state in the hierarchy).
    * Either the common owner or another component higher up in the hierarchy should own the state.
    * If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.

## Higher-Order Functions

* A higher-order function is a function that either takes another function as an argument or returns one.
* In the below example code, line 2 returns an anonymous function that compares the argument `n` from the higher-order function `greaterThan(n)` to its own argument `m` with the greater than operator.
```
function greaterThan(n) {
  return m => m > n;
}
let greaterThan10 = greaterThan(10);
console.log(greaterThan10(9));
```
<sup>https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK</sup>

* The `Array.prototype.map()` method is another example of a higher-order function. It takes a function as an argument, passes each element of an array into that lower-order function, and returns a new array with the results of the function applied to each element.

## Things I want to know more about
Are delegate functions a thing in JS?

---
