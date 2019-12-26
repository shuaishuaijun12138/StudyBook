## 1,服务器字体样式

```
@font-face{
	font-family:name;字体名称
	src:URL;//路径
	font-weight:normal |bold; 字体变宽
		}
```

#### 调用

```
font-family:name;
```

注: 多个服务器字体需要多次引入 @font-face

## 2,居中的办法

**1.margin 固定大小居中**

```
#father{
          overflow: hidden;
       }
   #son{
          margin:0 auto;/*水平居中*/
          margin-top: 50px;
        }
```

在进行垂直居中时你需要明确父元素的height，并且进行计算，如果父元素的高度变了，子元素将不再垂直居中

**2.绝对定位进行偏移**

```html
#father{
         position:relative;
       }
   #son{
         position: absolute;
         left:50%;
         margin-left: -50px;
         top:50%;
         margin-top: -50px;
        }
```

**3.弹性盒子居中**

```html
#father{
           display: flex;
           justify-content: center;
           align-items: center;
        }
```

