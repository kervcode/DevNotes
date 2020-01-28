# Test

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
