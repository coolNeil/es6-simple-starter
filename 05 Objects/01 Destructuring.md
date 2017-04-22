# Destructuring

```js
var data = { productName: 'Hat', price: 20 };

var { productName, price } = data;

console.log(productName); // 'Hat'
console.log(price); // 20
```

## 指派不同的变量名
```js
var data = { productName: 'Scarf', price: 10 };

var { productName: title, price } = data;

console.log(title); // 'Scarf'
console.log(price); // 10

console.log(productName); // "ReferenceError: productName is not defined
```

## 缺少变量
```js
var data = { productName: 'Belt', price: 50 };

var { productName, price, discount } = data;

console.log(discount); // undefined
```

## 默认值
```js
var data = { productName: 'Coat', price: 150 };

var { productName, price, discount = 0 } = data;

console.log(productName); // 'Coat'
console.log(price); // 150
console.log(discount); // 0
```

## 嵌套的对象
```js
var data = {
    productName: 'Shoes',
    price: 24,
    stock: {
        store: 4,
        online: 100
    }
};

var { stock: { store } } = data;
console.log(store); // 4

var { stock: { store: inStoreStock } } = data;
console.log(inStoreStock); // 4
```