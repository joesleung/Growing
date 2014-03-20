# CSS半透明背景的实现方案


    background: rgba(0, 0, 0, 0.3); /*CSS3半透明*/

    filter: progid:DXImageTransform.Microsoft.Gradient(GradientType=0, StartColorStr='#4c000000', EndColorStr='#4c000000');/*渐变滤镜*/

**其实现原理：**

**rgba（CSS3） + Gradient Filter(IE)**，既使用CSS3的RGBA颜色实现，在不支持CSS3的浏览器（主要是IE8-）使用IE的渐变滤镜[Gradient Filter](http://msdn.microsoft.com/en-us/library/ms532997(VS.85).aspx "Gradient Filter")变相实现半透明效果，并且没有继承问题。

注意：此效果在IE9下有一个bug，半透明为两倍(60&amp;%)。因为IE9+同时支持CSS3半透明和渐变滤镜。解决方法可以利用IE的hack，单独把IE9的filter变成透明度为0即可（高级浏览器大部分支持`:root`伪类，但不支持filter属性，而IE只有IE9支持）：

    :root .rgba{
    filter:progid:DXImageTransform.Microsoft.Gradient(GradientType=0, StartColorStr='#00000000', EndColorStr='#00000000');
    }

最终代码：

    div_bg{filter:progid:DXImageTransform.Microsoft.gradient(enabled='true',startColorstr='#33000000', endColorstr='#33000000');background:rgba(0,0,0,0.2);}

    :root div_bg{filter:progid:DXImageTransform.Microsoft.gradient(enabled='true',startColorstr='#00000000', endColorstr='#00000000');}/*for IE9*/

或者ie9的hack使用： 

    :root div_bg{filter:none;}/*for IE9*/

**如果对自己写代码比较不熟练的话，可以使用这个在线可视化生成工具：[css-semitransparent](http://huangyang.me/demo/css-semitransparent/ "css-semitransparent")**

**其他方法:**

① 使用一张半透明背景图片。我看百度空间顶部的固定导航就是这么干的。

![百度空间实现半透明](http://blogimages.u.qiniudn.com/hibaidutop.png)

主要代码：

    header{background: transparent url(**.png) repeat-x top left;}

② 或者，你可以采用最简单的方案——渐进增强。即在支持CSS3的浏览器使用RGBA，不支持CSS3的浏览器（[坑爹的IE8-](http://huangyang.me/kill-ie6.html "让我们一起消灭IE6！")）使用RGB（或Hex等）颜色替代方案。在多数情况下，其实谁又在乎是不是透明呢？

    background: rgba(255, 255, 255, .8);
    background: #fff\9;