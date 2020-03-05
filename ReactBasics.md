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
