# Rest parameters

```js
function calculator(type, ...nums) {
    var sum = 0;

    for (var y = 0; y < nums.length; y++) {
        if (type === 'add') {
            sum = sum + nums[y];
        }
    }

    return sum;
}

calculator('add', 1, 2, 3, 4); // 10
```

为什么不使用arguments？
* It's not clear
* It's not a real array
* Arguments can't be named, it's always called arguments
* Can't be used with arrow functions due to the scope