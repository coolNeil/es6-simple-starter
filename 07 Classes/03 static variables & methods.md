# static variables & methods

## 静态属性和方法只能通过Class来调用

```js
class Person {

    constructor(name) {
        this.name = name;
    }

    static version = 0.0.1

    static desc() {
        return `This is a description of this Person Class`
    }

}

Person.version; 0.0.1
Person.desc(); //This is a description of this Person Class
```

也可以这样写：
```js
class Person {
    constructor(name) {
        this.name = name;
    }
}

Person.version = 0.0.1
Person.desc = () => This is a description of this Person Class;
```