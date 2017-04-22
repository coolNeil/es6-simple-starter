# Default parameters

```js
function newWay(a = 1, b = 10) {
    return a * b;
}
newWay(); // 10
newWay(0); // 0
newWay(1, 2); // 2
newWay(undefined, 11); // 11 (undefined is "missing")
newWay(null, 11); // 0 (null is explicitly null)
```

## 可以是表达式
```js
function foo(a = 1 + 1, b = 10) {
    return a * b;
}
foo(); // 20
```

## 调用函数
```js
var config = require('config');

function urlBuilder(host = config.get('host'), port = 27017) {
    return 'mongod://' host + ':' + port;
}

// assuming config.get('host') returns 'hostname'
urlBuilder(); // mongod://hostname:27017
```

```js
function madness(a = (function(){ return 10 }()), b = 5) {
    return a * b;
}

madness(); // 50
```

## 必须的参数
```js
function required () {
    throw new Error('Required param missing');
}

function foo (baz = 2, iReallyNeedThis = required()) {
    return baz + iReallyNeedThis;
}

foo(1, 2); // 3
foo(1, undefined); // "Error: Required param missing
```