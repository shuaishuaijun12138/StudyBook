# 第一章bootstrap基本原理和布局

--Bootstrap是由Twiter得Mark Otto和jacob Thomton开发得、bootstrap是2011年八月在GitHub上发布得开源产品，是目前最受欢迎得前端框架之一。Bootstrap是基于HTML、CSS、JAVASCRIPTde ,它简洁灵活，使得Web开发更加快捷。

--优势：

--移动设备优先：自Bootstrap3起，框架包含了贯穿于整个库的移动优先的样式。

--浏览器支持：所有得主流浏览器都支持Bootstrap，（IE8及以上）

--容易上手：只要您具备HTML和CSS得基础知识，您就可以开始学习Bootstrap。

--响应式设计：Bootstrap得响应式css能够自适应于台式机、平板电脑和手机，更多有关响应式设计的内容详见Bootstrap响应式设计。

--为开发人员创建接口提供了一个简洁统一得解决方案。

--包含了功能强大得内置组件，易于定制。

--提供了基于Web得定制。

## Bootstrap环境安装

将bootstrap文件引入页面

​                                

Bootstrap得所有JavaScript插件都依赖jquery，因此jquery必须在Bootstrap之前引入

## Bootstrap CSS

Bootstrap使用了一些HTML5元素和CSS属性。需要使用HTML5文档类型（Doctype）。

Bootstrap3得设计目标是移动设备优先，然后才是桌面设备。为了让Bootstrap开发的网站对移动设备友好，确保适当的绘制和触屏缩放，需要在网页的head之中添加viewprt meta标签，如下所示：

<meta name=”viewport” content=”width=device-width,initial-scale=1.0”>

## 容器(container)

--Bootstrap 3的container class用于包裹页面的内容（固定宽度）。

--例如：<div class=”container”>…</div>

--Bootstrap 3 CSS有一个申请响应的每日查询，在不同的媒体查询阈值范围内都为container设置了max-width，用以匹配网格系统。

--.container 响应式固定宽度

--.container-fluid 100%宽度

## 栅格系统

原理：利用的是响应式来实现的，会把一行平均最多划分成12列，然后根据不同得尺寸进行相应的设置，xs(<768px)、sm(>=768px)、md(>=992px)、lg(>=1200px)

Bootstrap提供了一套响应式、移动设备优先的流式栅格系统，随着屏幕或视口(viewport)尺寸的增加，系统会自动分配12列，他包好了易于使用的预定义类，还有强大的mixin用于生成更具语义的布局。

栅格系统用于通过一系列的行（row）与列（column）的组合来创建页面布局，你的内容就可以放入这些创建好的布局中。

栅格系统基本工作原理：

--“行(row)”必须包含在。Container(固定宽度)或.container-fluid(100%宽度)中，以便为其赋予合适的排列(aligment)和内外(padding).

--通过”行(row)”在水平方向创建一组”列(column)”.

--你的内容应当放置于“列(column)”内，并且，只有”列(column)”可以作为行(row)“的子元素。

--类似.row和.col-md-4这种预定义的类，可以用来快速创建栅格布局。

--通过为”列(column)”设置padding属性，从而创建与列之间的间隔(gutter),通过.row元素设置负值margin从而抵消掉为.container元素设置的padding,也就健介为”行(row)”所包含的”列(column)”抵消掉了padding.

--如果在一个.row内包含的列(column)大于12个，包含多与(column)的元素将作为一个整体单元被另起一排。

  

通过下标可以详细查看Bootstrap的栅格系统是如何在多种屏幕设备上工作的。

<html lang=”en”>如果是bootstrap就是<html lang=”zh-cn”>

  

列偏移

使用.col-md-offset-*类可以将列向右侧便宜，这些类实际是通过使用*选择器为当前元素增加了左则的边距(margin)。例如，。Col-md-offset-4类将.col-md-4元素向右侧偏移了4个列(column)的宽度。

  

嵌套列

--为了使用内置的栅格系统将内容再次嵌套，可以通过添加一个新的.row元素个一系列.col-sm-*元素到已经存在的.col-sm-*元素内。被嵌套的行(row)所包含的列(column)的个数不能超过12(其实，没有要求你必须占满12列)。

--列排序

--通过使用.col-md-push-*和.col-md-pull-*类可以很容易的改变列(column)的顺序。

  

表格

--为任意<table>标签添加.table类可以为其赋予基本的样式—少量的内补(padding)和水平方向的分割线。

--通过.table-striped类可以给<tbody>之内的每一行增加斑马条纹样式。

--添加.table-bordered类为表格和其中的每个单元格增加边框。

--通过添加.table-hover类可以让<tbody>中的每一行对数表悬停状态做出相应。

--将任何.table元素包裹在.table-responsive元素内，即可创建响应式表格，其会在小屏幕设备上(小于768px)水平滚动。当屏幕大于768px宽度时，水平滚动条消失。

## 表单

基本表单

--单独的表单控件会被自动赋予一些全局样式。所设置了.form-control类的<input>、<textarea>和<select>元素都将被默认设置宽度属性为width:100%;。将label元素和前面提到的空间包裹在.form-group中可以获得最佳效果

--为<form>元素添加.form-inline类可以时期内容左对齐并且表现为inline-block级别控件。只适用于视口(viewport)至少在768px宽度时(视口宽度再小的滑就会使表单折叠)。

--水平排列的表单

--通过为表单添加.form-horizontal类,并联合使用Bootstrap预置的删格类，可以将label标签和控件组水平并排布局。这样做将改变.form-group的行为，使其表现为栅格系统中的行(row),因此就无需再额外添加.row了。

类别选择器来实现的

轮播图：

Div—最外层嵌套的—carousel slide(横向的每一屏)

ul—li—>按钮

每一张图片

div—carousel-inner

里面的每一张图片加上变得位子都是一个item

在fullpage绑定导航的话使用的是data来进行绑定的，而在bootstarp中用的data来进行绑定的，在bootstrap中使用data绑定的时候的写法:data-

Li需要绑定到哪一个轮播图上，data-target

并且还有一点，每一个item被触发的时候都会调用active这个类别选择器，包括li也是

将小圆点绑定在每一个item上，使用的是data-slide-to=”0”

如果图片上需要文字的话：carousel-captionf

左右两个按钮的话直接用的a就可以了，并且使用role伪装成一个按钮=button

类别选择器：carousel-control  left/right

href:#id名,

除此之外这个按钮还具备单机切换图片的功能，data-slide这个属性，左边显示的时候显示前一张图片，所以值就是prev，如果是下一张这个值就是next

在fullpage中就有active，当导航被触发的时候自动加上这个类别选择器

在fullpage中$.fun.fullpage.moveSlideRight()

不管是不是开源的，你都不能直接改人的代码

Aria-hidden=”false”à是控制带不带鼠标划入的阴影的，默认是true

如果你想要用其他样式的轮播图的话，那么就必须使用js或jquery来实现的