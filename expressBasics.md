




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

- Templates are speciale type of file that have their own syntax and language.They live on the server, and act as some kind of form letter for HTML. 

## Most popular template languages

- Handlebars

- EJS 

- Pug 

- A template provides the basic HTML for your app and serves it to the users. 

- Template also lets you vary the output to provide customized responses. 

# Pug

## What is Pug? 

Pug is one of the most popular templating engines for Node. 

- Pug Example

```js
h1 I love TreeHouse

ul

  li Red
  li Yellow
  li Blueconst
  
```

# Using Pug in Your Express App

  - Steps to Using Pug
  
    - Down **Pug** with npm
    
    - Update code in app to use Pug
    
    - Create Templates
    
    - Render templates with response.render()
    
```js
npm install pug --save

const express = require('express');
const app = express();

app.set('view engine', 'pug') // The app.set method defines different settings in Express.

app.get('/', (req, res)=>{
    res.render('index');
});

app.get('/hello', (req, res)=>{
    res.send('<h1>Express is amazing</h1>');
});

app.get('/page', (req, res)=>{
    res.send('<h1>Another page</h1>');
});
app.listen(3000);

```
# GET Requests
Asks for data from the server like a web page from a server.

# POST Requests
is when a client send data to the server.

the form tag in pug require a method and action attibute. 
```js
form(action='', method= '')

```
# The Request Object
the request object allows the application to look at the request that the client has made.

# The response object 
The reponse object offer ways to reshape the reponse bak to the client

# Someobject methods

- .send() : sends a response string

- . render() : merges the data with the templates to surf dynamic pages.

- json()

# HTTP

is called a stateless protocol. This fundamental principle of HTTP means that the server does
track the relationship between one request and another.

this means each transaction with the server is independent and unrelated.

- Clients and servers have stateless interations. 
  - A server retains no memory of the client after sending a response, no matter how recently or often they interact.

- A cookie is a piece of data that the service stores on the client.
  - Cookies are stored on the browser by domain.
  
  res.cookie('username', req.body.username);
  
  - **cookie-parser** : 
  
  - **cookie-parser** : 
