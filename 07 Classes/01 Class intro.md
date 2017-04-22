# Class intro

```js
function Person(name) {
    this.name = name
}

Person.prototype.getName = function() {
    return this.name;
}

Person.prototype.setName = function(name) {
    this.name = name
}

var person = new Person('Don');
person.getName(); //Don
person.setName('Paul');
person.getName(); //Paul
```

```js
class Person {

    constructor(name) {
        this.name = name;
    }

    getName() {
        return this.name;
    }

    setName(name) {
        this.name = name;
    }

}

var person = new Person('Don');
person.getName(); //Don
person.setName('Paul');
person.getName(); //Paul
```