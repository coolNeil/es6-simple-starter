# Template literals

## 多行字符串
```js
var multiLineString = `line one of a string
blah
blah
could stick a whole book in here
blah
blah`
```


## 表达式
```js
// 变量
var name = 'Mike';
var welcomeMessage = `Welcome ${name}.`; // 'Welcome, Mike.'

// 表达式
`5 x 5 is ${5 * 5}`; // '5 x 5 is 25'

// 函数
function multiply (a, b) { return a * b; }
`2 x 2 is ${multiply(2, 2)}`; // '2 x 2 is 4'
```