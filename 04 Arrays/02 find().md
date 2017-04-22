# find()

```js
const cars = [
    { color:'red', engineSize: 1.0 },
    { color:'red', engineSize: 1.6 },
    { color:'blue', engineSize: 2.0 },
    { color:'green', engineSize: 3.0 }
];

cars.find(c => c.color === 'red' );

// { color:'red', engineSize: 1.0 }
// returns first match
```