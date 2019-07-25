# Basic React Principles

React is a JavaScript library, and so we’ll assume you have a basic understanding of the JavaScript language.
Please reference our Javascript principles for help as well.


React is a JavaScript library, not a framework.
---------------
> Libraries differ from frameworks by their relationship to the parent application using them. 
> Frameworks dictate the entire applications structure while libraries give the developer the 
> freedom to make their own application design decisions.

---

Only include one React component per file.
---------------

---

Always use [JSX syntax](https://reactjs.org/docs/introducing-jsx.html).
---------------

---

Always use [React Hooks](https://reactjs.org/docs/hooks-intro.html)
---------------
> *Only use React Class Components when they are truly required.*

---

Default to [Javascript ES6 Spec](basic-javascript-principles.md)
---------------

---

React component can only return a single root level element.
---------------

---

[Class Components](https://reactjs.org/docs/react-component.html)
---------------
> Use ES6 `React.Component` if a class component is required.

```jsx
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

---

[Composition vs Inheritance](https://reactjs.org/docs/composition-vs-inheritance.html)
---------------
> React has a powerful composition model, and we recommend using composition 
> instead of inheritance to reuse code between components.

```jsx
function Dialog(props) {
  return (
    <FancyBorder color="blue">
      <h1 className="Dialog-title">
        {props.title}
      </h1>
      <p className="Dialog-message">
        {props.message}
      </p>
    </FancyBorder>
  );
}

function WelcomeDialog() {
  return (
    <Dialog
      title="Welcome"
      message="Thank you for visiting our spacecraft!" />

  );
}
```


- [Passing Functions to Components](https://reactjs.org/docs/faq-functions.html)
- [state vs props](https://reactjs.org/docs/faq-state.html)
- [Virtual Dom](https://reactjs.org/docs/faq-internals.html)
- Rendering Multiple Components [Key](https://reactjs.org/docs/lists-and-keys.html)
- Local State / Reactivity Model [docs](https://reactjs.org/docs/state-and-lifecycle.html)
- Changing parent component's state[docs](https://reactjs.org/docs/lifting-state-up.html)
- [Conditional Rendering](https://reactjs.org/docs/conditional-rendering.html)
- [Event Handling](https://reactjs.org/docs/handling-events.html)
- [Components and Props](https://reactjs.org/docs/components-and-props.html)
- [Rendering Elements](https://reactjs.org/docs/rendering-elements.html)
- [Glossary](https://reactjs.org/docs/glossary.html)