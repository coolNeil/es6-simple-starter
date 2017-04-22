# freeze()

这个方法阻止属性被添加、移除、修改

```js
var user = { name: 'Johnny Five', isAlive: true, arms: 2 };

Object.freeze(user);

delete user.isAlive; // false
user.battery = 100; // 100
user.name = 'Johnny Six'; // 'Johnny Six'

user; // { name: 'Johnny Five', isAlive: true, arms: 2 }
```

判断是否被冻结
```js
var thing = {};

Object.isFrozen(thing); // false

Object.freeze(thing);

Object.isFrozen(thing); // true
```