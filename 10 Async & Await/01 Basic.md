# Basic

Promise快速复习
```js
import request from 'request';

function getAddress () {
    return new Promise((resolve, reject) => {
        request('https://anyaddress.com/api/get', (err, res, body) => {
            if (err) {
                reject(err); return;
            }
            resolve(body);
        });
    });
}

getAddress()
    .then(data => {
        count : data.length,
        result : data
    })
    .catch(err => console.error(err));
```

使用Async和Await

await后面是一个Promise对象

```js
import request from 'request';

function getAddress () {
    return new Promise((resolve, reject) => {
        request('https://anyaddress.com/api/get', (err, res, body) => {
            if (err) {
                reject(err); return;
            }
            resolve(body);
        });
    });
}

async function asyncFunc () {
    const address = await getAddress()
        .then(data => {
            count : data.length,
            result : data
        })
    return address;
}

// 调用asyncFunc函数会返回一个Promise对象
asyncFunc().then(data => console.log(data.result));
```

await只能在async标记的函数中使用，延迟执行知道promise处理完毕，如果await后面跟的不是Promise对象，那么它会被转成一个立即resolve的Promise对象

## 链式async函数
```js
async function asyncFunc1 () {
    return await asyncFunc2()
        .then(data => data)
}

async function asyncFunc2 () {
    return await getAddress()
        .then(data => {
            count : data.length,
            result : data
        })
}

asyncFunc1().then(data => console.log(data.result));
```