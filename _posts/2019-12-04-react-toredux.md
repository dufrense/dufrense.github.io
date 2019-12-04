---
layout: post
title:  "从0到redux"
date:   14:10 2019-08-23
categories: react
tags: redux
---
浏览器插件 redux DevTools 没有变成绿色，所以现在用它来调试 redux 数据是不可以的

先说 `redux` 的使用，需先看 创建store 这块的代码：
<b>nihao</b>
其下有 入口文件index.js
关键文件 reducer.js
此其一个处理类：
----
为自己的组件提供store：
mapDispatchToProps 里面是 return { m(){} }
-----

```
mapStateToProps = (state) => {
不是 (props)******，同样也是 return {}
```

如要分离再整合
reducer.js -> element/store/reducer.js

内容移去，然后 import 之
再 import combineReducers 函数，此调用而无返回，前台是 header: 别名
store 下面再添 index.js export { reducer };
接下来，要用 element/store的reducer 直接通过 store 就默认导入了


