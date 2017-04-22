# Trailing commas

允许在函数调用和定义时候的参数尾部加上逗号，这样的话在git中添加一行参数，就只会显示一行改变而不是两行
```js
 function helloWorld(
     one,
     two,
+    three,
 ) { return one + two }

 helloWorld(
     1,
     2,
+    3,
 );
```