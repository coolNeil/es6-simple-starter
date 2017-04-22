# seal()

这个方法阻止属性被添加、移除、修改

```js
var user = { name: 'Johnny Five', isAlive: true, arms: 2 };

Object.seal(user);

delete user.isAlive; // false
user.battery = 100; // 100
user.name = 'Johnny Six'; // 'Johnny Six'

user; // { name: 'Johnny Six', isAlive: true, arms: 2 }
```

严格模式下，添加和移除会导致TypeErrors
```js
var user = { name: 'Johnny Five' };

Object.seal(user);

user.legs = 2; // TypeError

user; // { name: 'Johnny Five' }
```

```js
var data = {};
Object.defineProperty(data, 'timestamp', { get: function() { return Date.now(); } });

data.timestamp; // 626649295

data.timestamp = Date.now(); // TypeError
```

**注意**：被密封对象中的其他对象仍然时可以**修改**的，除非他们也是密封
```js
var error = { reason: 1 };
var data = { error: error, response: '' };

Object.seal(data);
data; // { error: { reason: 1 }, response: '' }

delete error.reason;

data; // { error: {}, response: '' }
```