# getter &setter

```js
// ES5
var player = {
    level: 5
};

Object.defineProperty(player, 'health', {
    get: function() {
        return player.level * 10.5;
    }
});

console.log(player.health); // 52.5
```

```js
// ES6
class Person {

	constructor(name) {
		this._name = name;
	}

	get name() {
		return this._name;
	}

	set name(name) {
		this._name = name;
	}

}

var person = new Person('Don');
person.name; //Don
person.name = 'Paul';
person.name; //Paul
```