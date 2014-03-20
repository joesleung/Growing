# 三个实现点击图片放大效果的jQuery插件
*2013-08-20 12:45:28*


## 1、jQuery Image Magnify

这款插件使用起来比较简单，能够实现简单的点击放大效果。

[访问插件主页（英文）](http://www.dynamicdrive.com/dynamicindex4/imagemagnify.htm "关于插件的使用下载及演示") OR [查看演示](http://huangyang.me/demo/jquery-image-magnify/ "jQuery Image Magnify Demo")

**引入jQuery库及[插件](http://www.dynamicdrive.com/dynamicindex4/jquery.magnifier.js)：**

    <script src="jquery.js"></script>    
    <script src="jquery.magnifier.js"></script>

**配置参数：**

*   class="magnify"  //给图片添加clas

*   data-magnifyby="number"  //放大倍

*   data-magnifyto="number"  //放大到宽度（单位：px

*   data-magnifyduration="number"  //放大过渡时间（单位：s）

**举个栗子：**

    <img src="ocean.gif" class="magnify" data-magnifyto="900" data-magnifyduration="1000" />

即：**ocean.gif** 这张图片在鼠标点击后在**1秒**内等比放大到宽度为**900px**。

**也可通过jQuery代码设置：**

    <img src="ocean.gif" class="maimage">

    $("img.myimage").imageMagnify({    
    magnifyto:750,    
    magnifyduration: 1000    
    })

**当鼠标经过图片时，需要让鼠标图标变成放大镜型 [magnify.cur](http://www.dynamicdrive.com/dynamicindex4/magnify.cur "放大镜图标")：**

cursorcss: 'url(magnify.cur), -moz-zoom-in', //这个默认已添加，只需将magnify.cur放到指定路径（默认为网页根目录）

* * *

## 2、ZOOMIMAGE

此插件功能强大，效果也比较多，可以设置图像描述和分组浏览。但是需要引用的js文件较多，并且需要引入css样式。

[访问插件主页](http://www.eyecon.ro/zoomimage/ "使用、下载及演示")

**引入jQuery库及插件库：**

    <link rel="stylesheet" href="zoomimage.css" />
    <script src="jquery.js"></script>
    <script src="eye.js"></script>
    <script src="utils.js"></script>
    <script src="zoomimage.js"></script>

**调用插件：**

    $('a.myLinks').zoomimage(options);

更多参数设置可访问插件网站或[下载中文版插件](http://pan.baidu.com/share/link?shareid=2497793557&amp;uk=219570419)（包括使用文档）

* * *

## 3、Lightbox2

> Lightbox is small javascript library used to overlay images on top of the current page. It's a snap to setup and works on all modern browsers.

Lightbox2使用起来比较简单，只需调用插件、相应的CSS样式文件和图片即可。

    <script src="jquery.js"></script>    
    <script src="lightbox-2.6.min.js"></script>    
    <link href="lightbox.css" rel="stylesheet" />

配置

<a href="img/image-1.jpg" data-lightbox="image-1" title="My caption">image #1</a>

更多参数设置可[访问插件网站](http://lokeshdhakar.com/projects/lightbox2/ "Lightbox2 主页")或[下载插件](http://pan.baidu.com/share/link?shareid=1791752932&amp;uk=219570419 "百度网盘下载")（包括使用文档）

『本文来自[黄杨的博客]( http://huangyang.me/2-zoom-image-jquery-plug.html "三个实现点击图片放大效果的jQuery插件")，转载请保留本段』