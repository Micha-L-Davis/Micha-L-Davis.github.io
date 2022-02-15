# Code 301 Reading Notes

1. [Introduction to React and Components](code-301.md#introduction-to-react-and-components)
2. [State and Props](code-301.md#state-and-props)

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
