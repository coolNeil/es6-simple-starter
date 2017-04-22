# Array

简写的方式操作数组
```js
const parts = ['shoulders', 'knees'];

//same as unshift
const lyricsFirst = [...parts, 'toes'];
//['shoulders','knees','toes']

//same as push()
const lyricsLast = ['toes', ...parts];
//['toes','shoulders','knees']

//same as splice()
const lyricsMiddle = ['head', ...parts, 'and', 'toes'];
//['head','shoulders','knees,'and','toes']

//Same as concat()
const bones = ['spine', 'skull']
const grissle = [...bones, ...parts];
//['spine','skull','shoulders','knees']
```

也可以将类数组对象转换成数组(返回一个新数组)
```js
[...iterator] //convert iterator to array
[arguments] //convert arguments to array
```