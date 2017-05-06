```js
let myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('good')
  }, 2000)
  setTimeout(() => {
    reject('fuck')
  }, 1000);
});
// 下面错误处理，也能够通过.catch()方法来做
myPromise.then((res) => {
  console.log(res)
}, (error) => {
  console.log(error)
})
```

```js
let myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('good');
  }, 2000);
});

let myPromise2 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('good two');
  }, 1000);
});

Promise.all([myPromise, myPromise2])
  .then((data) => {
    console.log(data)
  })
  .catch((err) => {
    console.log(err);
  });
  ```