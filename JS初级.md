# JS初级

### JS语言

* 面向对象
* 面向过程
* 基于对象 ( 基于window对象 )  ( 依赖于html )

### JS语言的特点

* 简单性
* 安全性
* 动态性
* 跨平台型
* 基于对象的语言
* 是一种脚本编写语言



### JS数据类型

#### 检测数据类型

1. typeof

* `typeof null // object`

* `typeof underfined // underfined` 

2. instanceof 

* `"x" instanceof String //false`
* typeof 可以检测出数据类型,instanceof只能判断是否属于这个类型,返回`true|false`

##### 数据类型

* 普通数据类型
  * String
  * Number
  * 空null, undefined
  * Boolean
* 复杂数据类型
  * Object
  * Array
  * Function

#####  typeof返回值

* String
* Number
* Function
* Object
* Boolean
* undefined

#### `+`运算符

* 如果两边都是字符串,则是字符串拼接

* 如果两边都是数字,则两边是相加

* 如果一边是数字,一边是字符串,则把数字强制转换为字符串

  * 第一种情况

  * ```js
    var a = 2;
    var b = "我";
    console.log(a/b)  //NaN  // Number
    ```

  * 第二种情况

  * ```js
    var a = 1;
    var b = '22';
    console.log(a+b)  //122  // String
    ```



### 算术及表达式

#### 表达式

> 定义
>
> 由运算符连接操作数组成的式子, 不管运算符多长, 最终都是一个值

* &  全为1则为1        `1&1 `     为1否则为0
* |  有1就是1          `1^0`    `0^1    1^1`      为1否则为0
* ^ 不同为1             `1^0`    `0^1`       为0否则为1



### 函数

* 递归函数
* 自调函数
* 匿名函数
* 局部变量
* 全局变量
* 只要有var 就会开辟一个内存空间,但是有作用域的限制
* 回调函数
* 返回值函数
* 内置函数
  * encodeURI() 
  
  * decodeURI()
  
  * parseInt()
  
  * parseFloat()
  
  * isNaN()
  
  * eval()   
  
    * 可以执行字符串表达式
  
    * ```js
      var str = "2+3"
      console.log(eval(str))
      ```
  
    * 可以执行js代码(字符串形式的)
  
    * ```js
      var str = "var a = 2, document.write(a)"
      ```

#### 局部修改函数

```js
function add(a,b){
    add = 20;
    console.log(add)
}
add(2,10)
```



## JS对象

* 内置对象
* BOM对象  DOM对象
* 自定义对象



#### 内置对象

* String
* Array
* Math
* Date
* Number
* Function
* RegExp
* Error



#### 字符串对象

> 创建方式:
>
> ​	 直接赋值
>
> ​	 new String()     构造函数创建
>
> 对象属性:
>
> ​	length属性
>
> ​	prototype属性(原型)
>
> ​	prototype: 为对象属性增加新的方法
>
> ​					   覆盖旧的方法,实现新的方法
>
> 对象方法:
>
> ​	chatAt()
>
> ​	chatCodeAt()
>
> ​	concat()     几乎不用
>
> ​	fromCharCode()
>
> ​	indexOf()
>
> ​	lastIndexOf()
>
> ​	localeCompare()
>
> ​	match()
>
> ​	replace()
>
> ​	slice()
>
> ​	search()
>
> ​	split()
>
> ​	substr()
>
> ​	substring()   几乎不用
>
> ​	toLowerCase()
>
> ​	toUpperCase()
>
> ​	valueOf()   几乎不用
>
> ​	toString()
>
> 
>
> substr()和slice()区别
>
> substr(开始索引,截取个数)  常用  负数从后面往前截
>
> slice(开始索引,结束索引)



#### 数组对象

>var arr = new Array()   //这种方式创建只知道是数组对象,但是没有长度和值
>
>join  连接成字符串
>
>pop  出栈
>
>push   入栈
>
>concat  连接
>
>reverse   倒置
>
>shift  将元素移出数组
>
>unshift    插入元素到数组头部
>
>slice  返回数组的一部分     返回一个新的数组
>
>sort   排序
>
>toString
>
>splice  插入,删除,替换元素       删除(开始索引,删除个数,替换的值)



#### new 到底做了什么

* var obj = {}
* `obj.__proto__=test.prototype`
* test.call(obj) 
* 把obj的地址赋值给等式左边的变量

```js
function People(name, age, phone) {
  this.name = name;
  this.age = age;
  this.phone = phone;
  //若构造函数中`没有reutrn 或return this或基本类型`（number、string、boolean、null、undefined）的值，则返回obj在堆中的内存地址；若`return 引用类型`，则返回值为这个引用类型
  // return null;//无影响
  // return {};//返回此对象
  // return function(){};//返回此函数
}

function _new(fn, ...arg) {
    const obj = Object.create(fn.prototype);
    const ret = fn.apply(obj, arg);
    return ret instanceof Object ? ret : obj;
}

let a = _new(People, 'aa', 20, 132456);
let na = new People('aa', 20, 132456);
console.log(a, na);
//运行结果
People { name: 'aa', age: 20, phone: 132456 }
People { name: 'aa', age: 20, phone: 132456 }
```



### JS原型链图片

![1490251-293b8fe01cf2ef5f](E:\node\md\1490251-293b8fe01cf2ef5f.webp)



#### 数组去重

1. ```js
   //两重for循环进行去重
   var arr = [23,45,23,53,75,75,75,341]
   for(var i=0;i<arr.length;i++){
       for(var j=i+1;j<arr.length;j++){
           if(arr[j]==arr[i]){
               arr.splice(j,1)
               j--
           }
       }
   }
   console.log(arr)
   ```

2. ```js
   //利用函数的indexOf()去重
   var arr = [23,45,23,53,75,75,75,341]
   var temp = []
   for(var i=0;i<arr.length;i++){
       if(temp.indexOf(arr[i])===-1){
           temp.push(arr[i])
       }
   }
   console.log(temp)
   ```



#### Math对象

* 唯一的静态对象
* 静态对象:不需要创建, 可以直接调用

```js
random   	*随机数
floor     *下舍入
log
max
min
pow
round    
sqrt
valueOf
abs
ceil    *上取舍
exp 返回e的指数
```



#### Date对象

```js
date.getDate() 1-31
date.getDay() 0-6
date.Month()  0-11
date.getFullYear()   获取年份
date.getHours()    小时
date.getMinutes()    分
date.getSeconds()     秒
date.getMilliseconds()    毫秒
date.setTime()   用时间戳来定义时间

时间对象转换为字符串对像
toString()
toTimeString()
toDataString()
toUTCString()
toLocaleString()
toLocaleTimeString()
toLocaleDateString()
```



#### Number对象

```js
toString      转换为字符串,指定为基数
toFixed    转换为指定位数的小数      四舍五入
```



#### Function对象

```js
静态属性
length   获取形参的个数
arguments  实参  (看做为实参的对象)
arguments.callee()    该方法用来调用当前函数
```



#### Error对象

```js
name: 错误类型
number:  错误类型 (IE)
message: 错误信息
```



#### BOM对象

* 浏览器对象

![E66W(WK~QYPCOAZMAYX0G3M](E:\node\md\ll.jpg)

##### window对象

> 属性

* innerHeight     可视窗口实际宽高  不包含有滚动条和工具栏
* innerWidth
* length       返回页面使用的框架的个数

> 弹出框方法

* alert(message:string)     错误提示
* confirm(message:string)   返回真假
* prompt(message:string, default:string)    返回输入的内容

> 方法

*  open("url","窗口名称","属性=值,属性=值")
  * left
  * top
  * width
  * height
  * **不需要写像素**
* print()   //打印当前页面内容
* close()   //关闭当前页面
* scrollBy()   滚动了
* scrollTo()    滚动到
* setTimeout()
* setInterval()

##### navigator

* userAgent  返回user-agent
* appVersion 返回浏览器平台和版本信息
* javaEnabled 判断是否开启java

##### screen屏幕

* availHeight   屏幕高
* availWidth   
* height     分辨率(常用)
* wdith
* 上面的两个区别是: height包含下面任务条的高度

##### history历史

*  length   之前访问过的页面的数量

> 方法

* go(number)            *可以替代back和forward     参数为正负数,代表前进和后退的路由   **仅支持正负1**

```js
- back()       * 和forward相对应
- forward()      和go相对应
```

##### location   获取的和URL相关的信息

* href    可以跳转
* port      端口
* search    获取?后面的
* host     返回端口号
* hostname     URI
* hash     获取#后面的数据
* pathname       路径
* protocol     协议

> 方法
>
> assign() 重新加载新的文档
>
> reload()
>
> replace()

##### Frames





#### DOM对象

* body内部全是DOM对象

* DOM树
* ![](E:\node\md\domTree.png)

```js
1. 标签内的文本称为文本节点
2. 标签内的属性称为属性节点
3. 注释称为注释节点
4. 每一个html标签都是一个节点
```

##### 获取节点

1. document.getElementById(id)
2. document.getElementsByTagName(tagName)  //数组
3. document.getElementsByName(name)     //数组
4. document.getElementsByClassName(className)     //数组

* 如果循环打印这个节点( alter DOM ),不能使用for in   推荐使用for



##### 节点属性

* nodeName  节点名字
* nodeType   节点类型
* nodeContent    节点内容



##### DOM操作节点

###### 创建节点

* createElement()   创建元素节点
* createTextNode()   创建一个文本节点

###### 添加节点

* parentNode.appendChild( newNode)   添加节点到当前节点内部的后面      移动节点到当前节点内部的后面
* parentNode.insertBefore( newNode, whoNode )    添加节点到当前节点内部的前面      移动节点到当前节点内部的前面

###### 操作节点

* removeChild()  删除节点
* cloneNode(default:false)    //  true深拷贝一个节点  false浅拷贝一个节点
* replaceChild(新节点,被替换的节点)
* hasChildNodes判断是否有子节点        **注:空格是一个节点**
* contains()是否包含某节点          **注:能判断,但是不能判断个数**

###### 访问节点的相关节点

* parentNode     某节点的父元素
* firstChild
* lastChild
* childNodes
* children                     不包含文本节点
* nextSibling                包含文本节点
* previousSibling        包含文本节点

* nextElementSibling      不包含文本节点

###### 操作属性

* getAttribute()
* setAttribute()
* removeAttribute()

###### 样式设置

* style属性
* style.cssText可以设置多个
* className
* html

###### 判断两个节点是否是同一个节点

* element.isEqualNode()            可以深度查询



## JS事件

#### 事件绑定方式

* 行内绑定
* 对象名.事件名
* addEventListener(事件名,函数名,捕获事件,冒泡事件) 
  * 兼容    d.attachEvent('onclick',test)

```js
if(d.addEventListener){
    d.addEventListener('click',test,false);
}else{
    d.attachEvent('onclick',test)
}
```

#### 鼠标事件

* 支持onload的对象 img, window,layer
* 支持onresize的对象  window
* 支持onscroll的对象   window
* onclick
* ondblclick
* onunload
* onmousedown
* onmouseup
* onmouseover
* onmouseout

#### 键盘事件

* onchange
* onblur
* onselect
* onfocus
* onreset
* onsubmit
* onkeydown
* onkeyup
* onkeypress

#### 事件对象

* 定义: 只有事件才能调用事件对象函数

  * ```js
    onclick=function(){
        e = window.event||e   //可以获取到
    }
    function myTest(){
        e = window.event||e   //获取不到
    }
    ```

* e = windown.event || e    获取事件对象

##### 事件对象的属性

* button 可以获取鼠标左中右
  * 普通浏览器012
  * ie浏览器142
* target   触发当前事件的对象DOM节点
* altKey shiftKey ctrlKey 返回true|false      不用记
* type   返回事件名称
* screenY   电脑屏幕
* clientY     窗口屏幕
  * ie   =>    x,y
  * fireFox    =>    pageX,pageY
* offsetY     相对于区域
  * firefox不支持

##### 事件对象的方法

* preventDefault()     //阻止事件默认行为

  * IE兼容写法    `e.returnValue = false`

* stopPropagation() 阻止冒泡

  * IE兼容写法cancelBubble = true

  * 定义: 多个元素绑定同一事件,触发最内层的元素,这些事件从内到外以此触发,就是冒泡,默认的事件流就是冒泡

* addEventListener('click',function,事件冒泡|事件捕获)
  * attchEvent()  不支持事件捕获

##### 正则表达式

* 包含
  * 元字符
    * .任何字符
    * \d 数字
    * \w 字母数字下划线
    * \s 空格
    * ^ 开始
    * $ 结束
    * | 或
  * 限定符
    * `*` 0 次或多次
    * `+` 大于等于1次
    * `?` 0次或1次
    * {n} 恰好n次
    * {n,m} n到m次
    * {n,} 最少n次
    * {,m}最多m次
  * 字符类
  * 范围类
    * [123456] 数字
    * [0-4]范围内的数字
    * [a-z] 字母
  * g 全局搜索
  * i忽略大小
* 方法
  * test() 验证是否匹配
  * exec()   **最常用**
  * match(reg)  匹配正则表达式
  * replace(reg,newStr)
  * search(reg)

