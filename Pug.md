

h1 Learning Pug.

This tell express how to use pug. 

app.set('view engine', 'pug');

### HTML Boilerplate
```js
  doctype html
  html(lang="en")
    head
      title Landing Page
    body
      h1 The future home of a flashcard!
      p Difficulty on insensible reasonable in. From as went he they. 
      
```
### Basic Formatting

```js
doctype html
html(lang="en")
  head
    title Flash Cards
  body
    header
      h1 Flash cards
    section#content
      h2= prompt
      p
        i Hint: #{hint}
    footer
      p An app to help you study.

```

### Conditionals

```js
doctype html
html(lang="en")
  head
    title Flash Cards
  body
    header
      h1 Flash cards
    section#content
      h2= prompt
      if hint
        p
          i Hint: #{hint}
      else
        p There's no hint.
    footer
      p An app to help you study.
      
```
### Iteration

  - app.js
  
  ```js
  const express = require("express");
const app = express();

const colors = ["red", "orange", "yellow", "green", "blue", "purple"];

app.set("view engine", "pug");

app.get("/", (req, res) => {
  res.send("I am going over this for a 3rd time!");
});

app.get("/cards", (req, res) => {
  res.render("card", {
    prompt: "Who is buried in Grant's tomb?",
    colors
  });

  // res.locals.prompt = "Who is buried in Grant's Thumb?";
  // res.render("card");
});

app.listen(3000, () => {
  console.log("Server started on port 3000.");
});

  ```
  - pug template for colors
  
  ```js
  doctype html
html(lang="en")
  head
    title Flash Cards
  body
    header
      h1 Flash cards
    section#content
      ul 
        each color in colors
          li= color
      h2= prompt
      if hint
        p
          i Hint: #{hint}
      else
        p There's no hint.
    footer
      p An app to help you study.
  
  ```
### Form

```js
extends layout.pug

block content
  h2 Welcome, Student
  form(action="/hello", method="post")
    label Please enter your name 
      input(type="text", name="username") 
    button(type="button")  Submit

```

- **req.body** Contains key-value pair of data submitted in the request body. By default it is undefined.
