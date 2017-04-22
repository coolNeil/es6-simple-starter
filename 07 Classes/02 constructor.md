# constructor

```js
class Person {
    constructor(name) {
        this.name = name;
        this.gender = (this.name === 'bob') ? 'male' : 'female'
    }
}

const person = new Person('Bob');
person.name; //Bob
person.gender; //male
```