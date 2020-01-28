# Working with Objects in Arrays

```
  const users = [
  
    {name: 'Samir'},
    {name: 'Angela'},
    {name: 'Beatrice'}
    
  ]
  
  const newUsersArray = users.filter(user => user.name !== 'Samir');
  console.log(newUsersArray);
  
```


Using map to print something like `Samir is 27 years old`.


```
  const users = [
  
    {name: 'Samir'},
    {name: 'Angela'},
    {name: 'Beatrice'}
    
  ]
  const newUsersArray = users.map(user => `${user.name} is ${user.age} years old.`);
  console.log(newUsersArray);
  
```

### using reduce to combine the elements of an array into one value

```
  const users = [
    {name: 'Samir'},
    {name: 'Angela'},
    {name: 'Beatrice'}
  ]
  const newUsersArray = users.reduce((usersObject, user) => {
    usersObject[user.name] = user.age;
    return usersObject;
  }, {};
  
```
 - Output example
 
  ```
    {
      Samir: 27,
      Angela: 33,
      Beatrice: 42
    }
    
  ```
  ## Challenge Task 1 of 1
  
  - Using the map method on the authors array, create an array of full name strings, comprising the first name, then a space, then the last name. See the comments below for reference. Store the new array in the fullAuthorNames variable.
  
  ```
    const authors = [
      { firstName: "Beatrix", lastName: "Potter" },
      { firstName: "Ann", lastName: "Martin" },
      { firstName: "Beverly", lastName: "Cleary" },
      { firstName: "Roald", lastName: "Dahl" },
      { firstName: "Lewis", lastName: "Carroll" }
    ];
    let fullAuthorNames;

    // fullAuthorNames should be: ["Beatrix Potter", "Ann Martin", "Beverly Cleary", "Roald Dahl", "Lewis Carroll"]
    // Write your code below
    
    fullAuthorNames = authors.map(author => `${author.firstName} ${author.lastName}`);
    
  ```
  
  # Combining filter() and map()
  
    - Combining `filter()` and `map()` can be useful when you want to remove some elements before transforming the remaining elements.
    
   ```
      const usernames = ['Samir', Angela, 'Beatrice', 'Shaniqua', 'Marvin', 'Sean']
      //expected result: [{'name: 'Samir'},{name: 'Shaniqua'}, {name: 'Sean'}]
      
      const users = userNames
          .filter(name => .name.charAt(0) === 'S')
          .map(name => ({name}))
      
      console.log(users)
     
   ```
   
   - New exmaple
      
   ```
   
     const users = [
        {name: 'Samir', age: 27},
        {name: 'Angela', age: 33},
        {name: 'Beatrice', age: 42},
        {name: 'Shaniqua', age: 30},
        {name: 'Marvin', age: 23},
        {name: 'Sean', age: 47}
     ];

     // Result: ['Angela', 'Beatrice', 'Shaniqua', 'Sean'];
  
  ```
  
  ```
    const userNames = users
      .filter(user => age >= 30)
      .map(user => user.name);
    console.log(userNames);
    
  ```
  
  ## Challenge Task 1 of 1
  
  - Using the filter and map methods on the todos array, create an array of unfinished task strings. See the comments below to see the correct result. Store the new array in the variable unfinishedTasks.
  
  ```
    const todos = [
      {
          todo: 'Buy apples',
          done: false
      },
      {
          todo: 'Wash car',
          done: true
      },
      {
          todo: 'Write web app',
          done: false
      },
      {
          todo: 'Read MDN page on JavaScript arrays',
          done: true
      },
      {
          todo: 'Call mom',
          done: false
      }
    ];

    let unfinishedTasks;

    // unfinishedTasks should be: ["Buy apples", "Write web app", "Call mom"]
    // Write your code below

    unfinishedTasks = todos
                      .filter(todo => todo.done === false)
                      .map(todo => todo.todo);

```

# Combining filter() and reduce()

  - Combining filter() with reduce(), you can remove values from an array, using the results to compute some value. Get some practice with this combination.
  
```
    const products = [
      { name: 'hard drive', price: 59.99 },
      { name: 'lighbulbs', price: 2.59 },
      { name: 'paper towels', price: 6.99 },
      { name: 'flatscreen monitor', price: 159.99 },
      { name: 'cable ties', price: 19.99 },
      { name: 'ballpoint pens', price: 4.49 }
    ];

    // Result: { name: 'paper towels', price: 6.99 }
    
```

```
  const product = products
    .filter(product => product.price < 10)
    .reduce((highest, product) => {
        if (highest.price > product.price) {
          return highest;
        }
    return product;
    });

    console.log(product)
  
  ```
  
  using const and reduce to 
  
  ```
   const total = products
    .filter(product => product.price > 10)
    .reduce((sum, product) => sum + product.price, 0)
    .toFixed(2)
  
   console.log(total)
   
  ```
  
 # Nested Data and Additional Exploration
  
  ```
  
    const movies = [
    
      ['The Day the Earth Stood Still', 'Superman', 'Ghostbusters'],
      ['Finding Dory'],
      ['Jaws', 'On the Waterfront']
    ]

    // Result: ['The Day the Earth Stood Still', 'Superman', 'Ghostbusters', 'Finding Dory', 'Jaws', 'On the Waterfront']
    
  ```
   - Taking elements out of an array and place them inside of one big array - flattening
   
     - The spread operator places element of an array inside of another array
   
 ``` 
    const flatMovies = Movies.reduce((arr, innerMovies) => [...arr, ...innerMovies], []);
    
    cosole.log(flatMovies);
    
 ```
 Product the same result
 
 ```
   const flatMovies = movies
    .reduce((arr, innerMovies) => arr.concat(innerMovies), []);
    
 ```
# example 2

```
    const users = [
      {
        name: 'Samir',
        age: 27,
        favoriteBooks:[
          {title: 'The Iliad'},
          {title: 'The Brothers Karamazov'}
        ]
      },
      {
        name: 'Angela',
        age: 33,
        favoriteBooks:[
          {title: 'Tenth of December'},
          {title: 'Cloud Atlas'},
          {title: 'One Hundred Years of Solitude'}
        ]
      },
      {
        name: 'Beatrice',
        age: 42,
        favoriteBooks:[
          {title: 'Candide'}
        ]
      }
    ];

    // Result: ['The Iliad', 'The Brothers Karamazov', 'Tenth of December', 'Cloud Atlas', 'One Hundred Years of Solitude', 'Candide'];

```

  const books = users
    .map(user => user.favoriteBooks.map(book => book.title))
    .reduce((arr, titles) => [...arr, ...titles], []);

  console.log(books);

```
