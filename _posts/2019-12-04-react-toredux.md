---
layout: post
title:  "从0到redux"
date:   14:10 2019-12-04
categories: react
tags: redux
---
浏览器插件 redux DevTools 没有变成绿色，所以现在用它来调试 redux 数据是不可以的

先说 `redux` 的使用，需先看 创建store 这块的代码：
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

*******

> 接下来：actionCreators 那个 action 的创建方式，以及其中的 type 都要变成一种变量

![](http://img.deliberate-practice.club/reduxExportWhole.png)
接下来，再用的话， import { 总出口导出的变量 } from 公共出口

引入 import {fromJS} from 'immutable';
修改时 **return** state.set('[property]', value) 

两级的语法不同 state.element.get('[property]')
所以，将 state 也变成一个 immutable 对象，之来源： 大的store里面的reducer.js
combineReducer 让之来源于 redux-immutable 就可以了




