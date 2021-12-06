# JavaScript Classes

A class is used to create one or more objects.

We can define two main area with a class definition.
  1. Instance Properties : What they have
  
      for example a human being may have:
      - name
      - age
      - height
  
  2. Instance Methods : what they do
  
      for example, a human being can: 
      - talk
      - run
      - jump

### Getters and Setters

Getters and setters are used to define methods on a class which are then used as if there are properties

They look like properties but are actually methods of that the class.
    
```js
class Rectangle {
// every class has a constructor which is used to setup the object
   constructor(){
      this.width = 5; // this refers to the object that is being created by that class
      this.height = 7;
      this.color = blue;
   }
   
 // instance methods can be define under the constructor
 // example : define a method that will compute the area of the rectangle
   getArea() {
      return this.width * this.height;
   }
}

```

Class example with getters and setters

```js
class Square {
  constructor(_width) {
    this.width = _width;
    this.height = _width;
  }
  
  // Getter
  get area () {
    return this.width * this.height;
  }
  
  // setter
  set area (area) {
    this.width = Math.sqrt(area);
    this.height = this.width;
  }
}

```
