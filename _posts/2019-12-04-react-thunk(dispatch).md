---
layout: post
title:  "react immutable"
date:   14:10 2019-12-04
categories: react
tags: 
---

取得源头活水来
获取ajax 不会写组件里，异步组件 action里，或 redux-thunk 异步操作放其中
redux-thunk 可以使 action 里面写函数
此中间件：action 与 store 之间，是 dispatch 的一个升级，应该是在 创建 store 的时候被使用
有了之，就可以在 action 里面做异步操作了

可以在之前的数据操作前，先派发一个 action，此时不再是 返回对象了
而是帮助返回一个函数，且可以用 ()=> { return (dispatch)=> {} };

用的我ajax结果替换，又到了改 store，action->store->reducer
const action = {data: fromJS(data.data)}

const { name, list } = this.props;

> 一些样式：
box-shadow: 0 0 8px rgba(0,0,0,.2);
border-radius: 3px;