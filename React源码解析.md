# React源码解析

### 知识导读

* 资源说明 
* ![1568767118962](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1568767118962.png)

***



### 基础知识 React API 一览

#### 准备工作

* packages->events
* packages->react
* packages->react-dom
* 以上三个文件是核心需要关心的点

* React 和 React-Dom
* Flow Type

#### JSX到JavaScript的转换

* `<div></div>` 转换为 `React.createElement('div',null);`

*  React自定义函数返回一个JSX的时候,函数的名字需要首字母大写

#### ReactElement

* 最常使用到的API

* React.createElement(type,config,children)是在React的ReactElement.js文件中
* 创建一个元素的 $$typeof 是 REACT_ELEMEMT_TYPE

#### ReactComponent

* Component和PureComponent的区别: 在保证props没有更新的情况下,减少必要的刚更新(主要是根据: shouldComponentUpdate)
* 