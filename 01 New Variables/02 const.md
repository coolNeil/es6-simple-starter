# const

## 已经定义的变量都不能通过const改变，不管是通过var还是let定义的。例如：
```js
var message = "hello";
let age = 25;

const message = "goodbye"
const age = 10;
```

```js
const maxItems = 5;
maxItems = 6
```

## 对于复杂的变量，如array或者object，可以修改，但是不能重新赋值。例如：
```js
const person = {
  name: "Neil"
};

// works
person.name = "Jack";

// throws an error
person = {
  name: "Jack"
}
```