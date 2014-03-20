# 纯CSS3绘制饼图
*2013-10-27 22:01:48*


纯css3实现，no js，no canvas。效果如下：

![pure-css3-pie-charts](http://blogimages.u.qiniudn.com/pure-css3-pie-charts.png)

简要说一下实现原理。主要用到css3的一些属性，包括圆角属性 `border-radius` ，2D转换 `transform` ，剪裁绝对定位元素属性 `clip` 。其中2D旋转和剪裁绝对定位元素是关键。 `clip` 是[剪裁绝对定位元素](http://www.w3school.com.cn/css/pr_pos_clip.asp)属性，其允许您规定一个元素的可见尺寸，这样此元素就会被修剪并显示为这个形状。

**在线演示及代码下载:** [Demo](http://huangyang.me/demo/pure-css3-pie-charts/)

兼容性：IE8-可以回家吃饭了。