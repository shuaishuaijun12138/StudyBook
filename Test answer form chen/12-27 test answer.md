## 1,多列布局

```
#father{
	column-count: 3 ;
	}
h1{
	column-span: all ;  //text-align:center; 可加可不加
	}
```

兼容性自己添加

## 2,文字滚动

```
$.fn.extend{
	A:function(){
	var str = $(this).html();
	setInterval(function(){
		str = str.substr(1)+str.substr(0,1);
		$(this).html(str)
		},200)
	}
}
```

## 3,鼠标滑入增加外边框(outline)

```
$("img").hover(function(){
	$(this).css({outline:"2px solid #000"})
},function(){
	$(this).css({outline:""})
})
```

## 4,src & href 的区别

**1.href：它指向一些网络资源，建立和当前元素或者说是本文档的链接关系。**

**2.src:	表示的是对资源的引用，它指向的内容会嵌入到当前标签所在的位置**

## 5,判断数据类型的方法

### 1.typeof :	返回一个表示数据类型的字符串，返回结果包括：number、boolean、string、object、undefined、function等6种数据类型。

### 2.instanceof:	判断对象和构造函数在原型链上是否有关系，如果有关系，返回真，否则返回假.