# Destructuring

```js
var weekDays = ['Mon', 'Tue', 'Wed', 'Thu', 'Fri'];

var [monday, tuesday, wednesday, thursday, friday] = weekDays;
console.log(monday); // 'Mon'
```

## 省略变量名
```js
var [a, ,b] = [1, 2, 3];
console.log(a, b); // 1, 3
```

## 约束返回的数据
```js
var foo = () => {
    return [1, 2, 3];
};

var [a, b] = foo(); // 这里我约束只要其中的两项
console.log(a, b); // 1 2
```

## 交换变量
```js
var a = 1, b = 2;
[b, a] = [a, b];
console.log(a, b); // 2, 1
```

## 默认值
```js
var [a = 1, b = 2, c = 3] = [5, 10];
console.log(a, b, c); // 5, 10, 3
```