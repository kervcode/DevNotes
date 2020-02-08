




- The first thing to do when starting a new node.js project is to install the project dependencies.

  - Dependencies are parties node module use in a project.
  
### How to start a new node project and install express

 - ```js
        npm install express
   ```


in other to use express, we must add it using the node require statement. 

 - ```js 
        const express = require('express'); 
     ```

### Creating a Server in Express

- Express setup a server.

  - A server is a program that runs on a remote computer. it's job is to wait for HTTP reqiest from clients. 
  
  - Express can be called to create an express application.
  
  - ```js

     const app = express();

    ```
    
  then setup the development server using listen
  
  ```js
    app.listen(3000)
  ```
  
  # Creating a Route with Express
  
  Express handle resquest through ***Routes*** that we can setup in the app.
  
  ex: 
  ```js
    kervintznoel.com
      /home
      /about
      /projects
  ```
  - The get method can be used to create a route.
  
    ```js
        app.get()
    ```
    
    - To indicate the site's rout route, use the slash as the first parameter. The first parameter is sometime called the location parameter
    
    - The second parameter of the get method is an anonymous calback function which will run when the client resquest a route. The anonymous callback function takes two parameters. a request object and a reponse object.
    
    ```js
        app.get('/', (request, response) => {
          response.send(); // The send method send a string to the client.
        })
    ```
    
    
    
# Chapter example

  ```js
    const express = require('express'); 
    const app = express();
    
    app.get('/', (request, response) => {
          response.send(); // The send method send a string to the client.
        });
        
    app.listen(3000)
  ```
    
 # Adding Multiple Routes to the App
 
 - The listen method can take a callback function as a parameter. 
 
 app.listen
 
 ```js
    const express = require('express'); 
    const app = express();
    
    app.get('/', (req, res) => {
          res.send(); // The send method send a string to the client.
        });
        
    app.listen(3000)
  ```
  
# Using Templates with Express

- Templates are speciale type of file that have their own syntax and language.They live on the server, and act as some lind of form letter for HTML. 

## Most popular template languages

- Handlebars

- EJS 

- Pug 

- A template provides the basic HTML for your app and serves it to the users. 

- Template also lets you vary the output to provide customized responses. 

# Pug

## What is Pug? 

Pug is one of the most popular templating engines for Node. 