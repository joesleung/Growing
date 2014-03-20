# viewport meta的含义和用法
*2013-07-20 10:12:29*


    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no" />

这个是最常见的一条 `viewport meta` 代码，其意为将 viewport 定义为： 宽度为设备宽度（width=device-width），初始缩放比例为 1 倍（initial-scale=1.0），禁止用户缩放（user-scalable=no）。 viewport 全部属性&amp;值如下：

*   width: viewport 宽

*   height: viewport 高

*   initial-scale: 初始缩放比

*   maximum-scale: 最大缩放比

*   minimum-scale: 最小缩放比

*   user-scalable: 是否允许用户缩放

例：

*   width=960 或 width=device-widt

*   height=1000 或 height=device-heigh

*   initial-scale=0.

*   maximum-scale=

*   minimum-scale=

*   user-scalable=1(yes) 或 user-scalable=0(no)

## layout viewport的默认值

需要指出的是，哥浏览器厂商在对layout viewport的表现并不完全一致：

*   Safari iPhone: 980p

*   Opera: 850p

*   Android WebKit: 800p

*   IE: 974px

## width=device-width

表面上看，其意思是viewport 宽度等于设备宽度，但实际上却是一个定值**320px**（源于早期 iPhone 的分辨率为 320px × 480px） viewport其实是Apple公司创造的一个标签，目的是为了能够在手机浏览器上获得更好的浏览体验。这一标签并没有被W3C做为一项标准采用，但是许多（移动端）浏览器已经开始支持这一标签，并且许多针对移动端优化了的网页也都会使用到这一标签。你可以在Mozilla开发者博客上的[一篇文章](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag "Using the viewport meta tag to control layout on mobile browsers")了解更多，在[Apple开发者网站](http://developer.apple.com/library/safari/#documentation/AppleApplications/Reference/SafariWebContent/UsingtheViewport/UsingtheViewport.html "Configuring the Viewport")上有更详细的描述。