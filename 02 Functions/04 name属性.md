# name属性

返回函数名


## 匿名函数
```js
var f = function () {};

// ES5
f.name // ""

// ES6
f.name // "f"
```

## 带名函数
```js
const bar = function baz() {};

// ES5
bar.name // "baz"

// ES6
bar.name // "baz"
```

