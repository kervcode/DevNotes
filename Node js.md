# Node.js basics

### The four peices of problem solving

  - Prepare
  
  - Plan
  
  - Perform
  
  - Perfect
  
  -
  
### Type of events

In JavaScript, there are two types of events that can occurs. 

  - User Events
  
    - Example : mouse click
    ```js
         button.addEventListener('click', () => {
          alert('You clicked me');
         });
    ```
  
  - Another Examle: System Events
  
    - Data Events
    
    - Completion Events
    
    - Error Events
  
    ```js
        setTimeout(() => {
          alert("Timer finished!");
        }, 1000);
    ```
   - Another ExaMple: is a System event is the ready state change of an AJAX request
   
   ```js
      httpRequest.onreadystatechange = () => {
          switch (httpRequest.readyState){
              case XMLHttpRequest.DONE:
                  console.log('Finished');
                  break;
          }
      
      }
   ```
  
  ### JavaScript in the browser
