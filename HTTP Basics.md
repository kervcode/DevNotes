# HTTP Basics

- HTTP : plain text protocol

### Format of an HTTP Request

  - begin with a request line which start with a request method `GET` or `POST`.
  
      - get is used to view a resource on a server without making any changes
  
      - Post used to make/update changes to listed ressource.
      
      - next is URL
  
      - HTTP
   - Next line is the header, the header communicates information related to the request being made.
      - the header can include all sorts of info.
      
          EX: Host, User-Agent, Accept-Language
          
   - After the header is a blank line

   - then comes the request Body (this is optional only for POST requests not GET requests)


- https://tools.ietf.org/html/rfc7231

- https://tools.ietf.org/rfc/rfc7231.txt

### HTTP Response Format

First line is Status-line: `HTTP/[version] [status message]` 
  - Example `HTTP/1.1 200 OK`

- 200 level codes are success messages.

- 404 Page not found

- other 400s level code mean something went wrong in the client request

- 300s ressource requested have moved

- 500 level codes means that something went wrong on the server

Next line is the header: `[Header Name]: [Header Value]`

      - Ex: 
 ```js 
            Server: Nginx
            Date: Wed, 15 Jan 2020 20:18:59 EST
            Content-Type: application/xml
  ```
          
   ### Sending Data With Get Request  
   
   
   
   
   ### Sending Data With Post Request  
   ```
      telnet httpbin.org 80
      POST /post HTTP/1.1
      Host: httpbin.org
      Content-Length: 32
      
      firstname=Chris&language=English
   ```
   
   ### Example - Making a request to Restcountries.eu
   
   ```js
   const countryCode = 'HT';

//Make an HTTP request
const requestCountry = new XMLHttpRequest();

requestCountry.addEventListener('readystatechange', (e) => {
  if (e.target.readyState === 4 && e.target.status === 200){
    const data = JSON.parse(e.target.responseText)
//     console.log(data)
    const country = data.find((country) => country.alpha2Code === countryCode)
    console.log(country.name)
  }
})

requestCountry.open('GET', 'https://restcountries.eu/rest/v2/all')
requestCountry.send()
```
   
   
   

