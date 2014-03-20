Title: CSS自定义滚动条样式

Date: 2013-07-19 13:44:29

URL: /css-scrollbar.html

浏览器右边默认的滚动条或许有点呆板。并且在不同操作系统平台（Mac OS，Win xp78）上也有不一致的展现。一般这也不算什么大问题，甚至不算什么问题。但是总有写时候你需要改变一下，为了突出个性而来点不一样的。比如像[QQ音乐](http://y.qq.com/ "QQ音乐")和[我的个人主页](http://huangyang.me "huangyang.me")。这里所讲的css定义滚动条样式只限于**webkit**浏览器，通过css的一些伪类来定义。

    ::-webkit-scrollbar //滚动条整体部分
    ::-webkit-scrollbar-button //滚动条两端的按钮
    ::-webkit-scrollbar-track //外层轨道
    ::-webkit-scrollbar-track-piece //内层轨道，滚动条中间部分（除去）
    ::-webkit-scrollbar-thumb //（滚动条里面可以拖动的那个）
    ::-webkit-scrollbar-corner //边角
    ::-webkit-resizer //定义右下角拖动块的样式

实际上还有很多更多的更丰富的伪类来控制滚动条样式，不过在以上列出的一些已经能够满足基本的需要了。

**此外：**

需要说明的是，IE浏览器其实是最早提供滚动条的样式支持的，但是其他浏览器并不买微软的账，所以只有IE才支持，并且个人以为IE那套实现的样式比较丑陋。有人开发了一套在线生成此样式的flash工具，想了解的同学可以移步[这里](http://www.dengjie.com/temp/scroller.swf)。另外网上也有一些插件来实现自定义。如果你希望在多种浏览器都拥有一致的体验，可以尝试使用[插件](http://www.jqueryrain.com/2012/07/jquery-scrollbar-plugin-examples/ "20 jQuery Scrollbar plugin with examples")来实现。

[webkit官方滚动条自定义DEMO](http://trac.webkit.org/export/41842/trunk/LayoutTests/scrollbars/overflow-scrollbar-combinations.html "webkit官方滚动条自定义DEMO")