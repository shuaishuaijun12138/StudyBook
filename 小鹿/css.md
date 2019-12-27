 

\1.   Css层叠样式表，它是用于控制网页样式并允许将样式信息与网页内容分离的一种标记性语言

\2.   html缺点：维护困难、标记不足、网页过胖、定位困难

\3.   css四种引入方式：行内式，内嵌式，链接式，导入式

\4.   html：key=value  css:key:value

\5.   HTML:width=”200” height=”200” CSS:width:200px; height:200px;

\6.   行内样式：<p style=”width:200px;height:200px;background-color:#f00”></p>

\7.   内嵌式：把css所有代码集中区域，方便维护

<head>。

<title></title>

<style type=”text/css”>                  

P{style=”width:200px;height=200px;background-color:#f00”}

</style>

</head>

\8.   链接式：最常用的方式，html与css完全分离

<head>

 <link href=”1.css” type=”text/css” rel=”stylesheet”>

</head>

\9.   导入式

<style>

 @import url（“css保存路径”）

</style>标记中使用@import url（“url”）

 

Link：用href，什么时 

候用 什么时候加载；是一个标记，不存在兼容性问题

Import： 一直加载； 有兼容性问题，低版本IE不能用

 

\10.  优先级:行内>内嵌=链接=导入，谁在下面谁的优先级就高。

\11.  W3c是一个组织的名称，中文名称万维网联盟

\12.  Css基本选择器有三个：标记选择器、类别选择器、ID选择器

\13.  标记选择器：和标记名相同名称的选择器；自动应用到相同名称里，

\14.  类别选择器：类别名用户自己定义；手动应用到不同的标记中，

声明: .类别名{}  调用：<p class=”类别名”></p>

（不限定标记，谁都可以。）

\15.  ID选择器：ID名用户自己定义；手动应用到不同的标记中；与类别选择器不同地方在于，一个ID选择器只能在HTML中使用一次

声明:#ID名{}  调用：<p id=”ID名”>

\16.  行内样式的特点：即使加上宽高，也不会有，他的宽高取决于内容

\17.  选择器优先级：ID选择器>类别选择器>标记选择器

\18.  H1.one{}  <h1 class=”one”></h1>(指定类别选择器)

\19.  /*中间注释的内容*/

\20.  权重 优先级  id:100  类别：10  标记：1

\21.  选择器声明：集体声明、全局声明符号*、选择器嵌套

集体声明：h1,p,.one,one{}  中间用，隔开（英文的逗号）

全局声明：*{} 所有标记全部应用 优先级最低（星号）

选择器嵌套：div p{} 中间用空格，空格表示是后代（空格）

父子关系用> div>span就是div下面的span有效果（大于号）

22 继承：这个标记下面的所有标签都有效果

# 盒子模型

\1.   <div></div><span></span>相当于一个容器

Div是一个块级元素，他包围的元素会自动换行

Span仅仅是一个行内元素，在它的前后不会换行

Span没有结构上的意义，纯粹只是为了应用样式，当其他的行内样式都不合适时，就可以使用，

Div可以包含span，span不能包含div

\2.   块级：总是从新的一行上开始

​     高度宽度都是可控的

​     宽度缺省的时他的容器宽度为100%

​     块级元素中可以包含块级元素和行内元素

\3.   行内：

​     和其它元素都在一行上

​     高度，宽度及边距都是不可控的

​     宽高就是他的文字或图片的高度，不可改变

​     行内元素只能行内元素，不能包含块级元素

\4.  块级元素：Address,center,div,dl,form,h1-h6,hr,ol,p,table,ul

\5.  行内元素：A,strong,br,em,img,input,label,select,span,sub,sup,textarea

\6.  强制类型转换：display:block(行内转换为块);inline（块转换为行内）

\7.  一个盒子模型由content（内容）、border（边框）、padding（间隙）、margin（间隔）这四个部分组成：border-top,border-right,border-bottom,border-left,border与padding,margin。

\8.  margin-left+border-left+padding-left+width+padding-right+border-right+margin-left margin为盒子与盒子之间的距离

\9.  border就是边框他的元素有border-color:颜色，border-width:宽度，border-style:边框样式

边框的样式属性：none,hidden,dotted(点线),dashed,solid（实线）,double,groove,ridge,inset,outset

​    Border-left-color, Border-left-width, Border-left-style,哪个方向需要加哪个方向例如中间的left

​    Border-left：solid 10px #f00,   位置可以调换

Border：solid 10px #f00,     位置可以调换

​    正常情况下背景颜色是包含边框的

​    当只有边框时，可以只使用其中一个边，让其有颜色可以获得三角形

\10. padding设置的是内容跟边框之间的距离，1个值的话表示上下左右都一样

​    2个值上下，左右   4个为上右下左，   3个为上，左右，下，

字体与盒子之间的距离

\11. margin元素与元素之间的距离

\12. 行内元素单独设置margin-top和bottom是没效果的，如果想有，设置父元素的padding

\13. 行内元素的margin值的计算方式是margin-right加上margin-left

\15. 块级元素的margin值的计算方式是谁大谁有效果

\14. 代码重置：所有元素默认都会有自己margin与padding的值，我们将它设置为0。

Html,body,div,a,ul,li,img,span{

Margin:0;

Padding:0;

}

\16. w3c标准盒子与ie的区别：W3c盒子为盒子加上margin、padding的值 往外扩的，ie盒子为盒子减去margin、padding的值  往里面缩的。

# 文字

\1.   字体：font-family:字体名称1，字体名称2（有哪种字体用哪个）

<head>

<style>

P{font-family:宋体，黑体，微软雅黑；}

（代码从上往下，从左往右，所以先加载的是微软雅黑）

</style>

</head>

\2.   字体大小：font-size（默认大小为16px,最小支持12px0）

绝对大小：in(英寸)，cm（厘米）,mm(毫米)，pt（印刷点数），pc（1pc=12pt）

相对大小：

px（像素所占位置），

%（相对于父元素字体大小的百分比来设置的，仅限于字体大小或仅限于宽高）

em（倍数关系相对于父元素不管放在哪都是,所有乘一起）

\3.   文字颜色:color

\4.   文字粗细:Font-weight:bold(加粗,最常用)\lighter\normal\100-900九级粗细

\5.   斜体:font-style:italic(斜体,最常用)\oblique(倾斜)\normal(正常)

\6.   下划线\顶划线和删除线:text-decoration:underline\overline\line-through\blink\none

下划线 顶划线 删除线   发光  没有线

\7.   英文字母大小写:text-transform:capitalize\uppercase\lowercase;（仅限英文）

  首字母大 写全部大写 全部小写

\8.   段落对齐方式:

水平对齐方式:text-align:left\right\center\justify

   两端

   必须有 wertidal-align 垂直对齐方式:vertical-align:top\middle\bottom

\9.   行间距:line-height:数值   字间距:letter-spacing:数值

\10.  能设置右和下就不要设置左和上.

# 图片

Border属性添加图片边框  

Border-style 样式  border-color 颜色  border-width粗细  

Border-left  border-right  border-top  border-bottom 图片方向

Width  height 宽高  设置其中一个图片会成比例缩放或放大

Text-align:left/center/right  给父元素设置

Vertical-align:top/middle/bottom  纵向对齐方式  直接给图片设置有效果

行内元素：水平居中给父元素加text-align:center;

块级元素：不浮动直接加margin:0 auto;

​        浮动添加父元素，给父元素加margin:0 auto;

：hover 伪类选择器，鼠标划入的状态

鼠标方在图片上图片原地放大： 

Img{width:136px; height:136px;}

Img:hover{width:200px; height:200px;margin-top:-32px;margin-left:-32px}(-32为用hover宽度减去图片的宽度再除以2)

Float来实现文字环绕  让当前浮动的元素脱离文档流同时会影响后面元素显示方式，并且后面元素显示的时候，会把浮动元素让出来

Margin设置图片和文字的距离

# 网页背景

1、 Background-color:#ff0000; (背景颜色)

2、 Background-image:url;(背景图片)

3、 background-repeat(背景图片重复)：repeat-y（垂直重复） repeat-x（水平重复） no-repeat不重复

4、 background-attachment:fixed;(固定背景图片位置，不让他动)

5、 background-position（图片位置）:先写上下，再写左右 例如：top right就是上右             

还可以使用百分比：第一个是水平，第二个是垂直30% 50%

还可以使用像素：-20px -20px 上和左是负数，右和下是正数

6、css sprites  css 精灵  雪碧图：将多个图片拼接成一个大的图片，利用像素调整大图片位置background-position:-100px -100px 需要将div的大小设置为小图片的大小，不规则找左上角的位置就行。

7、background是一个复合属性，可以将多个属性直接写在background后面，例如：bac

kground:url(“../img/tupian.jpg”) no-repeat -100px -100px 

8、竖排显示文字writing-mode:tb-rl;

作业：圆角背景，雪碧图，背景渐变，颜色分层，电子书里两个案例

# 表格

1、 文字颜色color

2、 背景颜色background-color

3、 边框border 想要单元格也有边框，需要给td加border值。

4、 Border-collapse:collapse（边框合并为1px的一条线）/separate(边框分开)

5、   利用 ：hover可以设置鼠标划入变色  

6、 隔行变色   电子书上例子6.4

# 表单

1、    只设置下边框border：none；border-bottom：#000 solid 1px；width:120px;height:50px;color:#f00; font-size:30px; 

必须写background:transparent;兼容性问题，背景透明

2、    选择标记里面的背景颜色不能变，只能设置其大小  

3、    下拉列表框可以设置其背景色，但是背景图片只是表面显示，下拉菜单不显示背景图片

# 超链接

1、 去掉链接下划线：text-decoration:none;

2、 文字颜色：color

3、 文字大小：font-size

4、 伪类选择器：a:link（开始的状态） a:visited（访问过后状态） a:hover（鼠标划入状态） a:active(触发状态)书写顺序必须这样，否则有兼容性问题。

5、 不需要变化的写在a里上面，需要变化的写在a:link a:visited a:hove里

6、 按钮式链接 浮雕式链接

作业，鼠标划入向上走，改变文字颜色，加下划线，改变背景颜色，改变背景图片

# 鼠标

1、 Body{cursor:pointer}整个页面鼠标显示小手

# 列表

1、 list-style-type设置列表属性，他的值有九个

disc（实心圆） circle(圆心) square（正方形） decimal（123） upper-alpha（ABC） lower-alpha（abc） upper-roman（大写罗马字母） lower-roman（小写罗马字母） none(空)

列表前面的项目符号为40px 直接设置margin:0 padding:0px 取消间距

2、 list-style-image(前面的项目符号用图片来代替)

li{

height:30px;

line-height:30px;

list-style-type:none;(去掉前面符号) 

background:url(图片) no-repeat；

padding-left:35px;

}

3、 display属性

none(不显示) block（转为块级） inline（转换为内联元素） inline-block（转换为行内块元素） inherit  

display：none位置内容都隐藏

只隐藏内容，不隐藏位置visibility:hidden|visible(默认)

4、 实现侧导航步骤：

1先把项目符号去掉（给ul设置宽（宽度为所有li宽度加上项目符号的宽度）同时加上margin:0 auto; 就是导航居中）

2给li设置宽高（给（li）加上float:laft 就是正导航）

3给a转化为块级元素

4设置a的样式

5需要改变的样式放在a:link\a:visited\a:hover中

5、 要想给导航加上整条背景，给ul外面写一个div，设置DIV的背景颜色。

6、 Float左浮动定位

Left  right  both(两端)  

7、Position定位

Static（默认） absolute（绝对） relative（相对） fixed（固定）

8、Position定位要配和top right bottom left

Absolute（绝对定位），相对于当前窗口定位的（元素可以重叠）

Position:absolute;

Top:0px;

Left:0px;

​        (紧挨页面左上角，没有空隙)

9、当父元素没有定位，子元素还是相对于窗口定位的，当父元素有定位，子元素相对于父元素

绝对定位元素可以重叠，大的可以盖住小的

​                                                                                                                                                                                                    Relative 相对定位于元素自己本身（特点：元素不可以重叠）

10、两个定位的区别：

relative相对定位，相对于元素自己本身定位，元素不可以重叠，父元素高度有子元素决定，宽度依然是父元素本身

absolute绝对定位，相对于窗口定位，元素可以重叠，父元素宽高由子元素决定，如果父元素有定位的话，相对于父元素定位，宽高依然由子元素决定

absolute:

  绝对定位：

​    如果父元素没有定位的情况下，根据窗口来进行定位的

​    父元素有定位的话，根据父元素来进行定位的，并且父元素不管是什么定位都一样

​    父元素的宽高度：

​      不管是宽度也好，还是高度也好是由子元素决定的

relative：

  相对定位：

​    在任何情况下，都是相对于自己本身来进行定位的，那也就意味着它自己本身原来的位置是一直存在的

​    父元素的宽高度： 

​      宽度是自己本身的宽度，高度由子元素决定

 

如果父元素absolute，子元素relative

  那么父元素宽高就是子元素宽高

如果父元素relative，子元素absolute

那么父元素宽度是原来的宽度，高度肯定是没有的，因为子元素位置没有了

 

11、Float和position会脱离文档流

12、Fixed(固定定位) 相对于窗口定位 可以重叠 用left right top bottom定位

14、z-index调整重叠上下位置 想象页面为x-y轴，垂直于页面方向为z轴z-index值的大的页面位于其值小的上方。（就是把z-index的值写的最大就行）

15、overflow(如果内容溢出一个元素的框) 

​    Visible默认值，内容不会被修剪，会呈现在元素框之外

   Hidden内容被修剪，并且其余内容是不可见的 

Scroll内容被修剪，但浏览器会显示滚动条以便查看其余内容 

Auto如果内容被修剪，则浏览器会显示滚动一边查看其它内容 

16、visibility(指定一个元素是否可见)

​    Visible默认值，元素可见

​    Hidden元素不可见的

17、清除浮动：overflow：auto或hidden给父元素加 

​         Clear  

​          给父元素加宽高

18、bfc：块级格式化上下文

bfc父元素计算高度的时候，会把浮动的子元素的高度计算进去

# Css+div布局

1、 加载到哪，显示到哪（优点）不同浏览器有不同兼容性问题（缺点）

2、 固定布局（pc端）:浮动  position  

3、 流体布局（移动端）

4、 布局方式：固定浮动布局、固定定位布局

5、 固定浮动布局：

a)    不随窗口变化而变化

b)    主要使用float进行布局

c)    缩放窗口不会影响到网页布局

d)    采用margin：0 auto方式进行居中

6、 固定定位布局：

a)    不随窗口变化而变化

b)    主要采用position：absolute；进行定位

c)    缩放窗口不会影响网页布局

d)    采用position：absolute拉回方式进行剧中

7、 两列内容，左侧固定，右侧自适应，左侧浮动float：left；右侧不浮动

8、 三列内容 左右固定，中间自适应，左右float：left，right；中间不浮动（html要左右写上面，中间写下面）

9、 给页面所有元素居中Position：absolute；top：自己算（写在每一个di里）left：50%；margin-left:写负的宽度；

10、      两列内容的话，margin-left：左面的跟上面的一样，右面的需要加上左面的宽度

11、      流体浮动（自适应）布局

a)    随窗口变化而变化

b)    主要采用float

c)    当窗口比网页内容小时布局会变形

12、      流体固定布局

a)    随窗口变化而变化

b)    主要采用position:absolute绝对定位

c)    每一部分尽量都写上position：absolute，否则在ie浏览器会变形

# 兼容性问题

浏览器产生原因：由于不同厂商的浏览器或某浏览器的不同版本

浏览器内核：trident内核（ie内核）、gecko内核（firefox内核 苹果的）、webkit内核（safari内核，Chrome内核原）、presto（opera内核）

Css reset(css重置)

html, body, div, span, applet, object, iframe,h1, h2, h3, h4, h5, h6, p, blockquote, pre,a, abbr, acronym, address, big, cite, code,del, dfn, em, font, img, ins, kbd, q, s, samp,small, strike, strong, sub, sup, tt, var,dl, dt, dd, ol, ul, li,fieldset, form, label, legend,table, caption, tbody, tfoot, thead, tr, th, td {

 margin: 0;

 padding: 0;

 border: 0;

 outline: 0;

 font-weight: inherit;

 font-style: inherit;

 font-size: 100%;

 font-family: inherit;

 vertical-align: baseline;

}

:focus {

  outline: 0;

}

body {

  line-height: 1;

  color: black;

  background: white;

}

ol, ul {

  list-style: none;

}

table {

  border-collapse: separate;

  border-spacing: 0;

}

caption, th, td {

  text-align: left;

  font-weight: normal;

}

blockquote:before, blockquote:after,

q:before, q:after {

  content: "";

}

blockquote, q {

  quotes: "" "";

}

Css hack：为了获得统一的页面效果，就需要针对不同的浏览器或不同版本写特定的css样式，我们把这个针对不同的浏览器/不同版本写相应的css code的过程，叫做css hack

Css hack方式有三种：css属性前缀法、选择器前缀法以及IE条件注释

 

条件注释法只能在IE下生效：只能在IE 6下生效:只能在IE6以上版本生效：只在IE8上不生效：非IE浏览器生效：

IE条件注释法：

<!--[if IE]>在IE浏览器显示<link rel="stylesheet" href="1.css"><![endif]-->

<!--[if IE 6]>这段文字只在IE6浏览器上显示<![endif]-->

<!--[if gte IE 6]>这段文字只在IE6以上（包括）版本IE浏览器显示<![endif]-->

<!--[if !IE 8]>这段文字在非IE8浏览器显示<![endif]-->

<!--[if !IE]>这段文字只能在非IE浏览器显示<![endif]-->* IE6IE7 例子:*color:#0ff;_ IE5IE6 例子：_background:#fff;\9 IE6~IE11都能识别，火狐与谷歌不能识别。例子：height:120px\9;\0 IE5~IE11能识别,火狐与谷歌不能识别\9\0 IE8~IE10能识别,火狐与谷歌不能

 

css属性前缀法

\* IE6IE7 例子:*color:#0ff;

_ IE5IE6 例子：_background:#fff;

\9 IE6~IE11都能识别，火狐与谷歌不能识别。例子：height:120px\9

\0 IE5~IE11能识别,火狐与谷歌不能识别

\9\0 IE8~IE10能识别,火狐与谷歌不能

​                                  

  

关于CSS布局的顺口溜 

 

　　如果在用CSS设计布局时遇到BUG，请认真阅读以下内容，非常容易记忆的，不知道哪位高人把CSS BUG编成了顺口溜了!关于CSS布局的顺口溜如下所示：

 

　　一、IE边框若显若无，须注意，定是高度设置已忘记;

 

　　二、浮动产生有缘故，若要父层包含住，紧跟浮动要清除，容器自然显其中;

 

　　三、三像素文本慢移不必慌，高度设置帮你忙;

 

　　四、兼容各个浏览须注意，默认设置行高可能是杀手;

 

　　五、独立清除浮动须铭记，行高设无，高设零，设计效果兼浏览;

 

　　六、学布局须思路，路随布局原理自然直，轻松驾驭html，流水布局少hack，代码清爽，兼容好，友好引擎喜欢迎。

 

　　七、所有标签皆有源，只是默认各不同，span是无极，无极生两仪—内联和块级，img较特殊，但也遵法理，其他只是改造各不同，一个*号全归原，层叠样式理须多练习，万物皆规律。

 

　　八、图片链接排版须小心，图片链接文字链接若对齐，padding和vertical-align:middle要设定，虽差微细倒无妨。

 

　　九、IE浮动双边距，请用display：inline拘。

 

　　十、列表横向排版，列表代码须紧靠，空隙自消须铭记。

 

以上就是关于CSS布局的顺口溜，希望能对web前端工程师(div+css)们带来帮助。

IE6 BUG

1、 双边距问题：

a)    产生时机：父元素设置浮动，子元素也设置浮动并且子元素设置margin-left，就会出现margin-left双倍的问题

b)    解决办法：给子元素加display：inline；

2、  3像素bug

a)    产生时机：两个元素，第一个元素设置左浮动float：left，第二个元素不设置浮动，造成之间产生3px的问题

b)    解决方法：给第二个元素加上左浮动floa：left；

3、 照片下方间隙问题

a)    产生时机：图像下方添加块状元素，之间就会产生间隔，firfox、ie、chrome中都存在这个问题

b)    解决方法：给图片标记添加display：block；或者设置vertical-align

4、 空元素的高度问题

a)    产生时机:如果一个元素中没有任何内容，当样式中为这个元素设置了0-19px之间的高度时，此元素的高度始终为19px;

b)    解决方法：

\1.    设置：overflow:hidden;

\2.    Font-size:0;

5、 超链接文字动态效果的顺序问题

a)    产生时机：没有按照顺序设置样式

b)    解决方法：按照顺序写a:link a:visited a:hover

6、 Li外边距问题

a)    产生时机：当li标记中最后一个子元素设置浮动后会导致，每一个之间产生3px的间距

b)    解决方法：给<li>标记添加css样式vertical-align:top;

7、 Png图片背景透明问题

a)    Ie6不支持png格式的图片透明效果

b)    解决方法：使用ie条件注释添加js插件

c)    <--[if IE6.0]>

​           i.      <script type=”text/javascript” src=”DD_belatedPNG.js”></script>

​          ii.      <script type=”text/javascript”>

​         iii.      DD_belatePNG.fix(‘img’);

​         iv.      </script>

d)    <--[endif]-->