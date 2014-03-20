# 使用rem单位设置文字大小
*2013-07-20 12:02:06*

URL: /rem-css-font-size.html

CSS3新增了一个相对单位 **rem**（_root em_），使用`rem`同`em`一样皆为相对字体大小单位，不同的是`rem`**相对的是HTML根元素**。这个单位可谓集相对大小和绝对大小的优点于一身，通过它既可以做到只修改根元素就成比例地调整所有字体大小，又可以避免字体大小逐层复合的连锁反应。目前除[IE8](http://fuckie6.html5g.cn/ "Fuck!IE6")及更早版本外，所有浏览器均已支持rem。对于不支持它的浏览器，应对方法也很简单，就是多写一个绝对单位(px)的声明。不支持它的浏览器会忽略用`rem`设定的字体大小。下面是一个栗子：

/*IE8及之前版本的 IE浏览器使用 14像素*/

    p {font-size:14px; font-size:.875rem;}

为了使用的方便（不需要计算），我们可以在一开始把根元素定义一个基本字体大小为**62.5%**（即10px，若没有设置，将以16px为基准）。

    html {
      font-size: 62.5%;/*10 ÷ 16 × 100% = 62.5%*/
    }
    
    body {
      font-size:14px;
      font-size: 1.4rem;/*1.4 × 10px = 14px */
    }
    
    h1 {
      font-size:2.4px;
      font-size: 2.4rem;/*2.4 × 10px = 24px*/
    }
    
    p {font-size:14px; font-size:1.4rem;}/*IE8及之前版本的IE浏览器使用14像素*/
    
参考图：

![font-size](http://blogimages.u.qiniudn.com/font-size.png)

本文来源[黄杨的技术博客](http://huangyang.me/rem-css-font-size.html)，转载请保留此段，谢谢。