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
