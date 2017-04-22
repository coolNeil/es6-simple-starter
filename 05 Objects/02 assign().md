# assign()

```js
var thing = { a: 1 };
var otherThing = { b: 1 };
var newThing = Object.assign(thing, otherThing);

newThing; // { a: 1, b: 1 }
thing; // { a: 1, b: 1 }
newThing === thing; // true
```

```js
var thing = { a: 1 };
var newThing = Object.assign({}, thing);

newThing; // { a: 1 }
thing; // { a: 1}
newThing === thing; // false  newThing和thing完全独立，互不影响

newThing.foo = 'hi';

newThing; // { a: 1, foo: 'hi' }
thing; // { a: 1}
```

## 合并对象
```js
var defaults = { logging: true };
var myConfig = Object.assign({}, defaults, { logLevel: 'verbose' });

myConfig; // { logging: true, logLevel: 'verbose' }

```

## 多个源
存在多个源对象时，会被覆盖
```js
var o1 = { foo: 1 };
var o2 = { foo: 2 };
var o3 = { foo: 3 };
var result = Object.assign({}, o1, o2, o3);

console.log(result); // { foo: 3 }
```

