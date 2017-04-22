# startsWith() endsWith() includes()

```js
var s = 'Hello world!';

s.startsWith('Hello') // true
s.endsWith('!') // true
s.includes('o') // true
```

支持第二个参数
```js
var s = 'Hello world!';

s.startsWith('world', 6) // true
s.endsWith('Hello', 5) // true
s.includes('Hello', 6) // false
```

上面代码表示，使用第二个参数n时，endsWith的行为与其他两个方法有所不同。它针对前n个字符，而其他两个方法针对从第n个位置直到字符串结束。如

```js
'abc.gif'.endsWith('.g', 5); // true 表示前5个字符，即：'abc.g'是以'.g'结尾的
```