
# AJAX BASICS

Introduced by microsoft

initial name was `XMLHttpRequest Object` or `XHR`

- AJAX stands for Asynchronous JacaScript and XML (eXtensible Markup Language)

#### How AJAX Works

1. Create an XMLHTTP Request object

2. create/define a callback function

3. Open a request

4. Send the request

#### A Simple AJAX Example

```
 <script>
      var xhr = new XMLHttpRequest();
      xhr.onreadystatechange = function () {
        if (xhr.readyState === 4){
          document.getElementById('ajax').innerHTML = xhr.responseText;
        }
      };
      xhr.open('GET', 'sidebar.html');
      xhr.send();
  </script>
  ```
  #### GET and POST
  
  Use GET when you are only interested in receiving or getting information from a server.
  
  Use POST you are sending that is going to be saved.
  
  Character encoding
  
  - `& => %26`
  
  - `Space => +`
  
  - `+ => %2B`
  
  GET method is a simple way to send data to a web server
  
    - Downside of using GET
    
      - all of the data is sent from the URL
      
      - URL Limitation
      
 POST method send data differently than get. It sent data separate from te URL. 
 
 a POST request need a special header
 
 # Web proxy
 
 CORS : Cross Origin Resource Sharing
