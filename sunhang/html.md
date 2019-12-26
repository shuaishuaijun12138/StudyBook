# 开始前端学习

## `Html`

- `html` 三种文档类型?
  - 过渡性,框架性,严格型 

#### 超文本标记语言?

- 超文本是指在文本的基础上加上声音,动画,图像等等信息
- 标记是指 左右尖括号

#### `xml`和`xHtml`

- `xml`是可扩展标记语言 
- `xml`区分大小写
- `xhtml`可扩展超文本标记语言 

#### `Html4`和`HTML5`的区别

- `H5`新增加了 语义化标签
- 例如: `nav` `header` `footer`



## `url`

- `Url`是统一资源定位符
- `smtp` 邮件传输协议

### `URL`和`URI`的区别

- `URI`统一资源标识符
- __`URL`包含 `URI`__

### Head标签

#### meta标签

- meta的常见属性是 `name http-equiv` 和 `content`
- `content`是用来解析`name  OR  http-equiv`
- `name` __主要用于描述页面__
- `http-equiv`__主要用于和服务器相关信息__
- `http-equiv`常用的两个值有
  - `refresh`刷新
  - `content-type`网站类型

### 常用段落标签

- `xmp`: 忽略`html`格式
- `blockquote`: 段落缩进标



## 列表

#### 无序列表

- `type`属性 : `circle,disc,square`   空心圆,实心圆,实心方块

#### 有序列表

- `type`属性 : `1,a,A,i,I` 阿拉伯数字,小写字母,大写字母,小写数字,大写数字



## 超链接

#### 链接路径

- 路径分为:   
  - 绝对路径
  - 相对路径
  - 物理路径   从电脑开始
  - 根路径   从磁盘开始

#### 邮件链接

- `<a href="mailto:E-mail地址?subject=邮件主题&cc">邮件链接</a>`
- `cc` 抄送
- `bcc` 暗送
- `body` 邮件内容
- 549404709@qq.com 肖哥老师邮箱
- 抄送和暗送的区别:   抄送发多份

#### 书签链接

- 成对存在
- 创建:  `<a name="one"></a>`
- 使用:  `<a href="#one"></a>`



## 表格

- `caption`  标题,在一行内居中
- `colspan` 跨列合并
- `rowspan` 跨行合并
- `valign` 垂直方向对齐方式
- `cellspacing` 单元格与单元格之间的距离
- `cellpadding` 单元格内容与单元格的边框



## 多媒体

#### 图片

- `vspace`  左右空白
- `hspace`  顶部和底部的空白
- `src` 和 `href` 关系
  - 他们都是输入`URL`
  - `src`是当浏览器执行到这的时候会自动加载,`href`是当使用的时候才执行
  - `href`是建立链接关系,`src`则是直接引入文件
  - **href引用 不停  src引入 停止**
- __(兼容性问题)__高版本浏览器不带有边框,低版本带有边框,在开发中直接设置border为0

#### 滚动文字

- `behavior `滚动方式
  - scroll 循环滚动
  - slide 滚动一次停止
  - alternate来回交替滚动
- `hspace`和`vspace`空白间距
- `scrolldelay `滚动间隔
- `srcollamount` 滚动文字每次移动的距离

#### 背景音乐

- `bgsound src="" loop=""` 
- `embed`



## 框架

- 在框架里 `frameset` 需要代替`body`

- `frameset` 是框架集

  - `rows` 水平分隔
  - `cols` 垂直分隔
  - `rows="200,*"`	代表200像素    *代表剩余空间

- `frame` 框架 

- 框架嵌套的时候, `frameset`内部内部直接套写`frameset`,不能写`frame`

- 用框架实现页面分隔布局

  - 点什么
  - `<a href="#" target="frame_name">`
  - 改哪里
  - `<frame name="frame_name">`

- `frame`属性

  - `frameborder` 是边框是否显示
  - `border` 是框架的边框粗细
  - `noresize` 是否可以拖拽 

  #### 浮动框架

- `iframe` 可以嵌套在body内部

- `srcolling`

  - `yes no auto` 

------



## 表单

- 使用get提交,当数据较长的时候是无法提交的
- get会提交一次,post会提交两次