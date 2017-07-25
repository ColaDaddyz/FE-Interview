# react
## 虚拟DOM
在浏览器端用JS实现的一套DOM API，就像是一套虚拟空间，实现了VDOM模型，声明周期的维护，diff算法，以及VDOM像真实DOM的转变

像是一个缓冲区，每次修改只会更改虚拟DOM，在下一次事件循环时才去更新真正的DOM

### 模型
VDOM 不是很复杂，大概如下
1. 标签名
2. 节点的属性，样式，事件等等
3. 子节点
4. 标识的id

VDOM 分为三种类型，ReactComponentElement，ReactDomElement，ReactText，还有一个空组件


### 更新
涉及两部分
1. 属性的更新，包括样式，属性，事件
2. 子节点的更新，包括更新内容，子节点，这里涉及到diff算法了

## 生命周期
1. 首次挂载:getDefaultProps，getInitialState，componentWillMount，render，componentDidMount
2. 卸载：componentWillUnmount
3. 重新挂载组件:getInitialState，componentWillMount，render，componentDidMount，但是不会 getDefaultProps
4. 状态更新：componentWillReceiveProps，shouldComponentUpdate，componentWillUpdate，render，componentDidUpdate

componentWillMount 中调用 setState 不会触发 re-rnder,而是会进行 state 合并，React 利用更新队列 pendingStateQueue 以及 pendingReplaceState 和 pendingForceUpdate 实现 setState 的异步更新机制

如果在 componentWillReceiveProps 中 setState，不会触发rerender，componentWillReceiveProps，shouldComponentUpdate，componentWillUpdate都无法获取更新后的 state

## setState
setState 通过一个队列机制实现 state 更新

在 shouldComponentUpdate 和 componentWillUpdate 中如果调用了 setState，此时 pendingStateQueue !== null，因此会进行组件更新，可能会导致循环调用

更新时会判断是否处于批量更新模式，如果是，会保存在 dirtyComponents 中，后续批量处理，否则直接更新

## diff算法
策略
1. DOM 跨层级的移动非常少，因此只比较同级的节点，并且只做删除和增加，所以，要注意开发时尽量避免移除和添加DOM
2. 不同组件不会有相同的DOM结构，如果是同一个组件类型，继续深入比较DOM树，此时需要 shouldComponentUpdate来判断是否要更新，如果不同组件，直接替换
3. 利用 key 对同一层级的节点做区分：先通过唯一的key判断是否存在，如果存在，进行移动，移动前将当前节点在旧集合中的位置 与 lastIndex 对比，if(mountIndex < lastIndex)不操作。这是一种优化操作，因为lastIndex一直在更新，如果新集合中当期节点比 lastIndex 大，说明当期节点在旧集合上的位置比上个节点靠后，则当前节点不会影响到别人

## patch

