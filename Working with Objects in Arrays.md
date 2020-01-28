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
  
  
