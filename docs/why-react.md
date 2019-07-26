---
title: Why React
---

React offers up a variety of benefits that have driven its rise in popularity. Let us review a couple of them real quick:
=> Getting started is easy
React is basically JavaScript, so, as long as you know its basics, you’re good to go! The React API is quite simple to use and you will be able to create your first component with very limited markup.
=> Easy DOM (Document Object Model) manipulation
In the past, using the actual DOM API was a pain, a fact that made it difficult for developers to manipulate the DOM. React solves this problem by providing a virtual DOM (in memory) that acts as an agent between the developer and the real DOM. The virtual DOM is a lot more user-friendly for developers.
=> Speed
Because of React’s virtual DOM, it has a pretty cool way of handling changes to a web page; React is constantly listening for changes to the virtual DOM. It keeps a record of the actual DOM tree and when a change is detected on the virtual DOM, React calculates the differences between the two, it reacts to this change by making the changes and re-rendering only the elements on the DOM that have changed. This precision is what makes React lightning quick.
=> React is declarative
React allows you to describe what the application interface should look like as opposed to you describing how it should build the UI. React makes it such that you are not concerned with the details of how the different UI elements are created and rendered, giving you more time to think about what look you want to achieve with your interfaces as opposed to the tiny details of how to make that happen. Declarative programming is becoming more advanced and bringing more and more exciting features to the space. This post by Tyler Mcginnis is a good place to start finding more information on declarative programming vs imperative programming.
=> React makes use of reusable components
A component is simply a function/class that returns a section of your interface. Building an application with React allows you to reuse components in different sections of your application. It follows the pattern of creating a component once and declaring it in multiple locations as required. This helps you write a lot more maintainable code as it’s easy to make cascading changes throughout your application.
=> Unidirectional data flow
React applications are built as a combination of parent and child components. As the names suggest, each child component has a parent and a parent component will typically have one or more child components. Components receive data via props and in the case of a parent and child component, props are passed down from the parent to the child. Data (props) is never passed up from the child to the parent, hence the phrase, unidirectional data flow. This is a powerful concept because it leads to a more predictable application and creates a single source of truth so that any changes to the parent’s state propagate to all its children consistently.
=> Powerful type-checking using PropTypes
With the power of PropTypes, React allows you to protect your components from abuse (and catch bugs early) by strictly and efficiently enforcing type-checking on the props(props are to components what arguments are to functions) passed to them without the need to add the complexity that comes with using TypeScript or flow for type-checking in your project.
As of React 15.5.0, PropTypes is no longer part of the React core package but is used as a separate dependency.
=> Large community
React’s popularity ensures an ever-growing community around it, which means, there’s a ton of resources out there to help you as you grow your skills. More importantly, packages such as React-router and React-redux that extend React’s capabilities are actively maintained.
As you start out, these concepts may seem numerous and confusing; do not lose steam if everything doesn’t make sense right now. During the course of reading the book, things will get a lot clearer. Reviewing earlier sections of the book as you go along will help you to further internalise the content.
