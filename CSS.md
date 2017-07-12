# CSS 面试题
页面导入样式时，使用link和@import有什么区别？

（1）link属于XHTML标签，除了加载CSS外，还能用于定义RSS, 定义rel连接属性等作用；而@import是CSS提供的，只能用于加载CSS;

（2）页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;
（3）import是CSS2.1 提出的，只在IE5以上才能被识别，而link是XHTML标签，无兼容问题;


* CSS 中类 (classes) 和 ID 的区别。
权重不一样，id是唯一的，可以用做锚点，样式中class支持多个叠加

* 请问 "resetting" 和 "normalizing" CSS 之间的区别？你会如何选择，为什么？
http://jerryzou.com/posts/aboutNormalizeCss/
* 请解释浮动 (Floats) 及其工作原理。
* 描述`z-index`和叠加上下文是如何形成的。
* 请描述 BFC(Block Formatting Context) 及其如何工作。
* 列举不同的清除浮动的技巧，并指出它们各自适用的使用场景。
* 请解释 CSS sprites，以及你要如何在页面或网站中实现它。
雪碧图，多个图片放在一起，用background-position

* 你最喜欢的图片替换方法是什么，你如何选择使用。

* 你会如何解决特定浏览器的样式问题？
autoprefixer

* 如何为有功能限制的浏览器提供网页？
  * 你会使用哪些技术和处理方法？
  
* 有哪些的隐藏内容的方法 (如果同时还要保证屏幕阅读器可用呢)？
visibility:hidden

* 你用过栅格系统 (grid system) 吗？如果使用过，你最喜欢哪种？
了解锅bootstrap的

* 你用过媒体查询，或针对移动端的布局/CSS 吗？

* 在书写高效 CSS 时会有哪些问题需要考虑？
* 使用 CSS 预处理器的优缺点有哪些？
  * 请描述你曾经使用过的 CSS 预处理器的优缺点。

* 如果设计中使用了非标准的字体，你该如何去实现？

* 请解释浏览器是如何判断元素是否匹配某个 CSS 选择器？
https://www.zhihu.com/question/20185756

* 请描述伪元素 (pseudo-elements) 及其用途。
模拟dom了

* 请解释你对盒模型的理解，以及如何在 CSS 中告诉浏览器使用不同的盒模型来渲染你的布局。
box-sizing

* 请罗列出你所知道的 display 属性的全部值
block,inline,inline-block,run-in
https://swordair.com/css-display-run-in/

* 请解释 inline 和 inline-block 的区别？
是否能设置宽高

* 请解释 relative、fixed、absolute 和 static 元素的区别

* CSS 中字母 'C' 的意思是叠层 (Cascading)。请问在确定样式的过程中优先级是如何决定的 (请举例)？如何有效使用此系统？

* 为什么响应式设计 (responsive design) 和自适应设计 (adaptive design) 不同？
* 你有兼容 retina 屏幕的经历吗？如果有，在什么地方使用了何种技术？
* 请问为何要使用 `translate()` 而非 *absolute positioning*，或反之的理由？为什么？

* Viewport 视口相关 rem 看看

* Flex
Justify-content 主轴
Align-items 

Flex-grow 放大比例 如果为0 放大
Flex-shink 缩小比例
Flex-basis flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小

Flex
	flex属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。
	该属性有两个快捷值：auto (1 1 auto) 和 none (0 0 auto)。
	当 flex 取值为一个非负数字，则该数字为 flex-grow 值，flex-shrink 取 1，flex-basis 取 0%，如下是等同的
	当 flex 取值为一个长度或百分比，则视为 flex-basis 值，flex-grow 取 1，flex-shrink 取 1，有如下等同情况（注意 0% 是一个百分比而不是一个非负数字）：
	 flex 取值为两个非负数字，则分别视为 flex-grow 和 flex-shrink 的值，flex-basis 取 0%，如下是等同的：
	当 flex 取值为一个非负数字和一个长度或百分比，则分别视为 flex-grow 和 flex-basis 的值，flex-shrink 取 1，如下是等同的：

	• auto：首先检索该子元素的主尺寸，如果主尺寸不为 auto，则使用值采取主尺寸之值；如果也是 auto，则使用值为 content。
	• content：指根据该子元素的内容自动布局。有的用户代理没有实现取 content 值，等效的替代方案是 flex-basis 和主尺寸都取 auto。
百分比：根据其包含块（即伸缩父容器）的主尺寸计算。如果包含块的主尺寸未定义（即父容器的主尺寸取决于子元素），则计算结果和设为 auto 一样。

