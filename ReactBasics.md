# What is React? 

React is a JavaScript Library for building user interface. 

# Add React to a Project
- There are two common ways to install or get set up with React.
  - Create React app
  - or with CDN
  
```js
const title = React.createElement(
  'h1', 
  { id: 'main-title', title: 'This is a title.' },
  'My first React Element!'
);

console.log(title);
```

* important : react does not create actual DOM nodes. it creates Objects representation of the DOM node.

ReactDOM.render() renders React elements to the DOM. ReactDOM.render() does the creating and updating of the DOM.

# What is a component

- A **component** is a piece of UI you cab reuse. 

Everything in react is considered to be a component. 

- React components are required to begin with an upper case letter.

```js
  function Header() {
    return (
      <header>
        <h1>Scoreboard</h1>
        <span className="stats">Players: 1</span>
      </header>
    );
  }
```

- There are two ways that data get handle in react.
  - Props : read only or immutable
  - State : We use state for any data that is going to change.
  
# this.props

Props is one way that component can pass data from one component to another.

## Passing props to components

Props can be pass to a component by passing an attibute to the JSX component

# State
## What is state?
- State is the data that you want to track in your app. allows to create components that are dynamic, interactive, and it is the only data that changes over time.

- State is a regular JavaScript object with properties that defibe the peice of data that is changed.

- State is only available to class component


## Type of State

  - Application State : data available to the entire application
  
  - Component State : State that is specific to a component and not shared outside of the component.

# Lifting State Up

When two or more component need access to the same state, we move the state into their common parent.

## Creating a Controlled Component
- Initialize state for the Value of the input
- Listen for changes on the input to detect when value is updated
- Create an event handler that updates the value state

# Component Lifecycle
Every component instance follows a cycle: it's mounter onto the DOM, it's update with changes in data, and it's unmounted from the DOM.

## React Lifecycle methods
- Built-in methods that get called at each point in the life cycle

- Hooks that run code at key times in a component's life cycle

- Give you the ability to control what happens when a component mounts, updates, and unmounts.
