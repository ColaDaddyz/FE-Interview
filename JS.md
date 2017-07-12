# JS面试题
* 请解释原型继承 (prototypal inheritance) 的原理。
	

* 请解释为什么接下来这段代码不是 IIFE (立即调用的函数表达式)：`function foo(){ }();`.
  * 要做哪些改动使它变成 IIFE?
* 什么是闭包 (closure)，如何使用它，为什么要使用它？
* 请指出 JavaScript 宿主对象 (host objects) 和原生对象 (native objects) 的区别？
	原生对象是es自带的，比如function，array;宿主是宿主环境带的，比如dom，bom
* 请指出以下代码的区别：`function Person(){}`、`var person = Person()`、`var person = new Person()`？
* 在什么时候你会使用 `document.write()`？
* 请指出浏览器特性检测，特性推断和浏览器 UA 字符串嗅探的区别？
* 请尽可能详尽的解释 Ajax 的工作原理。
* 使用 Ajax 都有哪些优劣？
* 请解释 JSONP 的工作原理，以及它为什么不是真正的 Ajax。

* 请解释变量声明提升 (hoisting)。
	往vo还是哪个上面挂载的原因
* 请描述事件冒泡机制 (event bubbling)。
* "attribute" 和 "property" 的区别是什么？
* 为什么扩展 JavaScript 内置对象不是好的做法？
	容易被覆盖
* 请指出 document load 和 document DOMContentLoaded 两个事件的区别。
* `==` 和 `===` 有什么不同？
	== 会做类型转换
* 请解释 JavaScript 的同源策略 (same-origin policy)。
* 如何实现下列代码：
```javascript
[1,2,3,4,5].duplicator(); // [1,2,3,4,5,1,2,3,4,5]
```
* 什么是 `"use strict";` ? 使用它的好处和坏处分别是什么？
* 请实现一个遍历至 `100` 的 for loop 循环，在能被 `3` 整除时输出 **"fizz"**，在能被 `5` 整除时输出 **"buzz"**，在能同时被 `3` 和 `5` 整除时输出 **"fizzbuzz"**。

* 为何你会使用 `load` 之类的事件 (event)？此事件有缺点吗？你是否知道其他替代品，以及为何使用它们？

* What is the extent of your experience with Promises and/or their polyfills?

* 使用 Promises 而非回调 (callbacks) 优缺点是什么？
http://efe.baidu.com/blog/promises-anti-pattern/

* 请解释可变 (mutable) 和不变 (immutable) 对象的区别。
  * 请举出 JavaScript 中一个不变性对象 (immutable object) 的例子？
  * 不变性 (immutability) 有哪些优缺点？
  * 如何用你自己的代码来实现不变性 (immutability)？

* 什么是事件循环 (event loop)？
  * 请问调用栈 (call stack) 和任务队列 (task queue) 的区别是什么？

promise规范


- Commonjs amd cmd es6

Commonjs 同步，node用
Amd Requirejs  尽早获取依赖
Cmd seajs 需要时才去取依赖
Commonjs 和 es6 区别
	• CommonJS 模块输出的是一个值的拷贝，ES6 模块输出的是值的引用。
	• CommonJS 模块是运行时加载，ES6 模块是编译时输出接口。
	• 循环加载处理不同

事件循环机制

闭包

Mvvm mvc 单向数据流

Throlle debounce

