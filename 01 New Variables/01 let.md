# let

## Block-Level Declarations
```js
function letScope () {

    if (true) {
        let price = 10;
        console.log(price); // 10
    }

    {
        let price = 100000;
        console.log(price); // 100000
    }

    console.log(price); // "ReferenceError: price is not defined
}

letScope();
```

## TDZ (Temporal Dead Zone)(变量名不提升)
```js
console.log(a); // throws a ReferenceError
let a = 'hey';
```

为了避免暂死区错误，注意声明let变量应在块级作用域顶部声明，如下所示

```js
function name(obj) {
    var name = '';

    {
        let tmp;

        tmp = obj.name;
        name = tmp;
    }

    return name;
}

name({ name: 'matt' });
```

## No Redeclaration
```js
var count = 30;
let count = 40; // Syntax error
```

## 循环中的块级作用域
```
var funcs = [];

for (let i = 0; i < 10; i++) {
  funcs.push(function() {
    console.log(i);
  });
}

funcs.forEach(function(func) {
  func(); // 会输出0 1 2 3 4 5 6 7 8 9
});
```