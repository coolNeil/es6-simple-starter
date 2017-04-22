# keys()

keys()方法返回一个Array迭代器，包含数组中每个索引的键

```js
const cars = [
    { color:'red', engineSize: 1.0 },
    { color:'red', engineSize: 1.6 },
    { color:'blue', engineSize: 2.0 },
    { color:'green', engineSize: 3.0 }
];
const carKeyIterator = cars.keys();
console.log(carKeyIterator.next()); // { value: 0, done: false }
console.log(carKeyIterator.next()); // { value: 1, done: false }
console.log(carKeyIterator.next()); // { value: 2, done: false }
console.log(carKeyIterator.next()); // { value: 3, done: false }
console.log(carKeyIterator.next()); // { value: undefined, done: true }
```