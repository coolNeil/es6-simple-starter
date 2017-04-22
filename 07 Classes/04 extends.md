# extends

```js
class Person {

    constructor(name) {
        this.name = name;
    }

    getName() {
        return this.name
    }

}

class Introvert extends Person {

    constructor(options) {
        super(options); // 继承父类的name
        this.quiet = true;
    }

    getName() {
        const name = super.getName(); //继承父类的getName()
        return `${name} is quiet`;
    }

}

const person = new Introvert('Don');
person.name; //Don
person.quiet; //true
console.log(person.getName()); //Don is quiet
```

super()方法可以获取父类当中的所有变量和方法，并允许在子类中使用