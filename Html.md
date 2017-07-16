# HTMl 相关问题
* `doctype`(文档类型) 的作用是什么？
	告知浏览器的解析器用什么文档标准解析这个文档
	
* 浏览器标准模式 (standards mode) 、几乎标准模式（almost standards mode）和怪异模式 (quirks mode) 之间的区别是什么？
在怪异模式下，排版会模拟 Navigator 4 与 Internet Explorer 5 的非标准行为。为了支持在网络标准被广泛采用前，就已经建好的网站，这么做是必要的。在标准模式下，行为即（但愿如此）由 HTML 与 CSS 的规范描述的行为。在接近标准模式下，只有少数的怪异行为被实现。

* HTML 和 XHTML 有什么区别？
XHTML 元素必须被正确地嵌套。
XHTML 元素必须被关闭。
标签名必须用小写字母。
XHTML 文档必须拥有根元素。

* 使用 `data-` 属性的好处是什么？
	可以存放数据，用于选择器
	
* 如果把 HTML5 看作做一个开放平台，那它的构建模块有哪些？

* 请描述 `cookies`、`sessionStorage` 和 `localStorage` 的区别。

* 请解释 `<script>`、`<script async>` 和 `<script defer>` 的区别。
https://sfault-image.b0.upaiyun.com/28/4a/284aec5bb7f16b3ef4e7482110c5ddbb_articlex

* 为什么通常推荐将 CSS `<link>` 放置在 `<head></head>` 之间，而将 JS `<script>` 放置在 `</body>` 之前？你知道有哪些例外吗？
避免白屏，1.个别特殊JS，比如用于调试的基础脚本（部署时未必有）、性能日志之类，必须放在尽量最前的位置。2.一些需要在body之前加载的js文件，html5-shim脚本必须在body之前加载

* 什么是渐进式渲染 (progressive rendering)？
bigpipe


