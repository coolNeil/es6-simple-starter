# values()

keys()方法返回一个Array迭代器

```js
const cars = [
    { color:'red', engineSize: 1.0 },
    { color:'red', engineSize: 1.6 },
    { color:'blue', engineSize: 2.0 }
];

cars.values(); // ArrayIterator

const carValuesIterator = cars.values();
carValuesIterator.next(); // { 'value': { 'color':'red', 'engineSize': 1.0 }, 'done':false }
carValuesIterator.next(); // { 'value': { 'color':'red', 'engineSize': 1.6 }, 'done':false }
carValuesIterator.next(); // { 'value': { 'color':'blue', 'engineSize': 2.6 }, 'done':false }
carValuesIterator.next(); // { 'value': undefined, 'done':true}
```

## 迭代方式
```js
let arr = ['w', 'y', 'k', 'o', 'p'];
let eArr = arr.values();
// 您的浏览器必须支持 for..of 循环,for..of可以遍历迭代器
// 以及 let —— 将变量作用域限定在 for 循环中
for (let letter of eArr) {
  console.log(letter);
}
```

```js
let arr = ['w', 'y', 'k', 'o', 'p'];
let eArr = arr.values();
console.log(eArr.next().value); // w
console.log(eArr.next().value); // y
console.log(eArr.next().value); // k
console.log(eArr.next().value); // o
console.log(eArr.next().value); // p
```