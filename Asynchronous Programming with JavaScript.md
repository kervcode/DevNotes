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

### Asynchronous JavaScript - The old Way

ex
```js

  function getRecipe() {
    setTimeout(() => {
      const recipeID = [523, 883, 432, 974];
      console.log(recipeID);
      
      setTimeout((id) => {
        const recipe = {title: 'fresh tomato passte',
                        publisher: 'Jonas'
                       }
      }, 4500, recipeID[2])
    }, 3000)
  }
  
```

# Promise

- Object that keeps track about whether a certain event has happened already or not

- Determines what happens after the event has happened

- Implements the concept of a future value that we're expecting

  ### Promise states
      
     - Pending is the default state for promises.
     
     - After pending, they can either change to resolve or reject.
     
     ```js
     
       const getIDs = new Promise((resolve, reject) => {
          setTimeout(() => {
            resolve([523, 883, 432, 974])
          }, 1500)
       })
       
       const getRecipe = recID => {
          return new Promise(() => {
              setTimeout(ID => {
                  const recipe = { title: 'Fresh Tomato pasta',
                                  publisher: 'Jonas', 
                                  resolve(`${ID}: ${recipe.title}`)
                  }, 1500, recID
              });
          });
       };
       
       const getRelated = publisher => {
        return new Promise((resolve, reject) => {
            setTimout(pub => {
              const recipe = {title: 'Italian Pizza',
                             publisher: 'Jonas'};
              resolve(${pub}: ${recipe}`);
            })
        }, 1500, publisher)
       }
       
       getIDs
         .then(IDs => {
            console.log(IDs)
         })
         .then(recipe => {
            console.log(recipe);
            return getRecipe(IDs[2])
         })
         .catch(error => {
            console.log(error)
         }) 
       
     ```
