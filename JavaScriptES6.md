# 
## ForEach Helper
Behave the same way as a for loop. 

```js
  var colors = ['red', 'blue', 'green'];
    colors.forEach(function(color) {
      console.log(color);
    }
  );
```

```js
  colors.forEach(color => console.log(color));
```
```js
    //Create an array of numbers
    const numbers = [6,7,4,7,3,9,2,6,7]

    // Create a variable to hold the sum
    let sum = 0;

    //Loop over the array, incrementing the sum variable
    numbers.forEach(number => sum += number)

    // print the sum variable
    console.log(sum);
 ```
 ```js
    //Create an array of numbers
    const numbers = [6,7,4,7,3,9,2,6,7]

    // Create a variable to hold the sum
    let sum = 0;

    // Create a function to handle the operation
    const add = number => sum += number;

    //Loop over the array, incrementing the sum variable
    numbers.forEach(add)

    // print the sum variable
    console.log(sum);
 ```
