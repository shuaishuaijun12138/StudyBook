## 1,鼠标滑入中心放大

```
div:hover{
	transform : scale(1.5);
}
```



## 2,鼠标滑入旋转720 黄变蓝 左移动200px 停留

```
div:hover{
	animation: name 2s forwards;
}
@keyframes name{
form{
	background-color:yellow;
	}
to{
	transform:rotate(720deg) translate(-200px);
	background-color:blue;
	}
}
```



## 3,鼠标滑入增加宽度

```
div:hover{width:增加的宽度};
```

#### 方法不唯一  div事先定位好   ,增加宽度也好,定位位移也罢,再不济还能transform:translate(-200px);

#### 请看官自行感觉