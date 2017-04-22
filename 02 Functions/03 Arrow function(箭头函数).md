# Arrow function

两个参数，需要括号
```js
var add = (a, b) => { a + b };
add(1, 2); // 3
```

一个参数，省略括号
```js
var double = a => { a * 2 };
double(1); // 2
```

零个参数，只有括号
```js
var foo = () => 1000;
foo(); // 1000
```

## 箭头函数中的this不是动态绑定的，是lexical的
```js
function MyCounter () {
    this.number = 0;
}

// 这里不需要像es5那样用一个that变量缓存this
MyCounter.prototype.count = function () {
    setInterval(() => {
        this.number++;
    }, 1000);
}

var count = new MyCounter();
count.count();

```

## 不能使用arguments变量
```js
() => {
    var level = arguments[0]; // global
    var message = arguments[1]; // global
}
```