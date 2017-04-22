# Error

处理错误

```js
async function myFunc() {
    return await promiseFunc()
        .then(data => data)
        .catch(err => console.log(err))
}

//Similar too

async function myFunc() {
    let data = {};
    try {
        data.first = await promiseFunc();
        //We can also synchronous out wait
        data.second = await promiseFunc1();
        data.third = await promiseFunc2();
    } catch (err) {
        console.log(err);
    }
    return data;
}
```