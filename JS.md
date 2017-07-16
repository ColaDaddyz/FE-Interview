# JS面试题
* 请解释原型继承 (prototypal inheritance) 的原理。
	> 原型链 prototype那张图

* 请解释为什么接下来这段代码不是 IIFE (立即调用的函数表达式)：`function foo(){ }();`.
  * 要做哪些改动使它变成 IIFE?
  
  > 以function关键字开头的语句会被解析为函数声明，而函数声明是不允许直接运行的，只有当解析器把这句话解析为函数表达式，才能够直接运行，怎么办呢？以运算符开头就可以了
  (function foo(){ })()
!function foo(){ }()
+function foo(){ }()都可以

* 什么是闭包 (closure)，如何使用它，为什么要使用它？
	> 闭包就是能够读取其他函数内部变量的函数
		作用：
 			1. 管理私有变量和私有方法，将对变量（状态）的变化封装在安全的环境中
			2. 将代码封装成一个闭包形式，等待时机成熟的时候再使用，比如实现柯里化和反柯里化

* 请指出 JavaScript 宿主对象 (host objects) 和原生对象 (native objects) 的区别？
	> 原生对象是es自带的，比如function，array;宿主是宿主环境带的，比如dom，bom

* 请指出以下代码的区别：`function Person(){}`、`var person = Person()`、`var person = new Person()`？
> 函数声明
函数表达式
实例化一个person ：
(1) 创建一个新对象；
(2) 将构造函数的作用域赋给新对象（因此 this 就指向了这个新对象） ；
(3) 执行构造函数中的代码（为这个新对象添加属性） ；
(4) 返回新对象。

* 在什么时候你会使用 `document.write()`？

* 请指出浏览器特性检测，特性推断和浏览器 UA 字符串嗅探的区别？
	> document.XXX 是特性检测
	
* 请尽可能详尽的解释 Ajax 的工作原理。
* 使用 Ajax 都有哪些优劣？

* 请解释变量声明提升 (hoisting)。
	> 往vo还是哪个上面挂载的原因

* 请描述事件冒泡机制 (event bubbling)。
* "attribute" 和 "property" 的区别是什么？
	> DOM有其默认的基本属性，而这些属性就是所谓的“property”，无论如何，它们都会在初始化的时候再	  DOM对象上创建。
     如果在TAG对这些属性进行赋值，那么这些值就会作为初始值赋给DOM的同名property。
     
     HTML标签中定义的属性和值会保存该DOM对象的attributes属性里面；
		这些attribute属性的JavaScript中的类型是Attr，而不仅仅是保存属性名和值这么简单；
		
* 为什么扩展 JavaScript 内置对象不是好的做法？
	>容易被覆盖

* 请指出 document load 和 document DOMContentLoaded 两个事件的区别。
	http://www.cnblogs.com/caizhenbo/p/6679478.html
	document load
	document DOMContentLoaded


* `==` 和 `===` 有什么不同？
	> == 会做类型转换

* 请解释 JavaScript 的同源策略 (same-origin policy)。
脚本只能读取和所属文档来源相同的窗口和文档的属性

* 什么是 `"use strict";` ? 使用它的好处和坏处分别是什么？
	> 消除一些不严谨，不科学的代码

* 为何你会使用 `load` 之类的事件 (event)？此事件有缺点吗？你是否知道其他替代品，以及为何使用它们？

* What is the extent of your experience with Promises and/or their polyfills?

* 使用 Promises 而非回调 (callbacks) 优缺点是什么？
> http://efe.baidu.com/blog/promises-anti-pattern/

* 请解释可变 (mutable) 和不变 (immutable) 对象的区别。
  * 请举出 JavaScript 中一个不变性对象 (immutable object) 的例子？
  * 不变性 (immutability) 有哪些优缺点？
  * 如何用你自己的代码来实现不变性 (immutability)？

* 什么是事件循环 (event loop)？
  * 请问调用栈 (call stack) 和任务队列 (task queue) 的区别是什么？
	- 什么是同步和异步
		> 【一般而言，操作分为：发出调用和得到结果两步。发出调用，立即得到结果是为同步。发出调用，但无法立即得到结果，需要额外的操作才能得到预期的结果是为异步。同步就是调用之后一直等待，直到返回结果。异步则是调用之后，不能直接拿到结果，通过一系列的手段才最终拿到结果（调用之后，拿到结果中间的时间可以介入其他任务）。】
【上面提到的一系列的手段其实就是实现异步的方法，其中就包括event loop。以及轮询、事件等。】
【所谓轮询：就是你在收银台付钱之后，坐到位置上不停的问服务员你的菜做好了没。】
【所谓（事件）：就是你在收银台付钱之后，你不用不停的问，饭菜做好了服务员会自己告诉你。】

- Commonjs amd cmd es6
	> Commonjs 同步，node用
	Amd Requirejs  尽早获取依赖
	Cmd seajs 需要时才去取依赖
	Commonjs 和 es6 区别
		• CommonJS 模块输出的是一个值的拷贝，ES6 模块输出的是值的引用。
		• CommonJS 模块是运行时加载，ES6 模块是编译时输出接口。
		• 循环加载处理不同

Mvvm mvc 单向数据流

