# What is Async Await?

Async define and asynchronous function. 

  - Example
    ```js 
    async function fetchData(url) {
      const response = await fetch(url);
      //parse the reponse to json
      const data = await reponse.json();
      
      return data
    }
    ```

Await

  - Pauses the execution of an async function and waits for the resolution on a promise
  
  - Resumes execution and return the resolved value
  
  - Pausing the execution is not going to cause blocking behavior
  
  - Valid only inside function marked async
  
An Async function always return a promise. 

  - That promise resolves 
  with the value returned by the async function, or . rejects with an error thrown from within the function.
