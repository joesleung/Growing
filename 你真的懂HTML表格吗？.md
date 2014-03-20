# 你真的懂HTML表格吗？
*2013-07-23 12:00:40*


在HTML5时代，HTML表格`&lt;table&gt;`似乎已经离开发者们渐行渐远。但是表格在排列和显示数据信息行列方面其实非常优美且简洁。

HTML表格有10个相应的标签属性

![table](http://blogimages.u.qiniudn.com/table.png)

下面这张图很直观的展现了一个标准的表格结构：

![table](http://blogimages.u.qiniudn.com/table1.png)

其包含一个标题(caption)、头部(thead)、主体(tbody)和底部(tfoot)。

需要注意的：

1.  如果您使用`thead`、`tfoot`以及`tbody`元素，您就必须使用全部的元素。**它们的出现次序是：thead、tfoot、tbody**，这样浏览器就可以在收到所有数据前呈现页脚了。您必须在 table 元素内部使用这些标签（来自[w3schools](http://www.w3school.com.cn/tags/tag_tfoot.asp "w3school")）

2.  在HTML 5中,表格的`align`和`bgcolor`属性已被淘汰（或不赞成使用）

3.  `empty-cells`属性定义了不包含任何内容的表单元格如何表示，如果显示，就会绘制出单元格的边框和背景。除非`border-collapse`设置为`separate`，否则将忽略这个属性（某些版本的 IE 浏览器不支持此属性）。（来自[w3schools](http://www.w3school.com.cn/css/pr_tab_empty-cells.asp)）