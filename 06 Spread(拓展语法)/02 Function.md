# Function

函数中的spread parameter会被当成一个数组

```js
function sentence(...words) {
    return words.join(' ');
}

function sum(...nums) {
    return nums.reduce((prev, curr) => prev + curr);
}

sentence('Who','is','this','Don','?')// Who is this Don?
sum(1,2,3)// 6
```