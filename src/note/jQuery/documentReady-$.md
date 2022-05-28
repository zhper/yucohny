# 入口函数

## 两种写法

```js
//1
$(document).ready(function () {

})
//2
$(function () {
    
})
```



# 与原生的区别

+ `window.onload`入口函数不能写多个，不然后面的会覆盖掉前面的；`jQuery`的入口函数可以写多个
+ 两者执行时机不同，`jQuery`入口函数要快于`window.onload`
  + `jQuery`入口函数要等待页面上的`DOM`树加载完后执行
  + `window.onload`要等待页面上的所有资源（`DOM`树/外部`CSS`/`js`链接、图片等）都加载完后执行。



# `$`符号

本质上是一个立即执行函数。

+ 引入一个`js`文件，会立即执行这个`js`文件中的代码。
+ `jQuery`文件是一个立即执行函数，执行这个`jQuery`文件中的代码，其实就是执行这个立即执行函数。
+ 这个立即执行函数就是给`window`对象添加了一个`jQuery`属性和`$`属性。

> `jQuery`与`$`属性是等价的，是相同的函数。

## 传递参数不一样，效果不一样

如果参数传递的是一个匿名函数-入口函数；

如果参数传递的是一个字符串-选择器/创建一个标签；

如果参数传递的是一个`DOM`对象，那他就会把`DOM`对象转换为`jQuery`对象。


