# Asynchronous Programming with JavaScript

  - What you'll learn
  
    - Synchronous vs. asynchronous programming
    
    - Callbacks
    
    - Promises
    
    - Async/await
    
 ___

JavaScript is single threaded. This means it can process only one task at a time.

### Callback Functions

A callback function is a function passed into another function as an argument. The function that receives the callback function is often referred to as the "parent" function. The parent function will, at some point in the future, execute or call the callback.

For example, the add function below accepts a function as its third argument (via the parameter callback). When add is invoked, the function passed to it logs the sum of the values passed in for a and b.

```
  function add(a, b, callback) {
    callback(a + b);
  }

  add(2, 4, function(sum) {
    console.log(sum); // 6
  });
  
```

In the following example, the function getUserName accepts a function as an argument (via the parameter callback). The greeting function passed to getUserName is invoked after prompt() captures a name and stores it in the variable name.

```
  function getUserName(callback) {
    const name = prompt('What is your name?');
    callback(name);
  }

  function greeting(name) {
    alert('Hello, ' + name);
  }
  
  getUserName(greeting); // a reference to the greeting function is passed / to   the function

```
