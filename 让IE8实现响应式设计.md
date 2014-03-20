# 让IE8实现响应式设计
*2013-10-18 12:13:38*


有人说2013年是响应式网页设计（_Responsive Web Design_）之年，不论是国外还是国内的一些大的网站，简约风、扁平化、响应式这些似乎成为了今年网页设计的一股潮流。36Kr、淘宝、天猫、一淘相继改版后都采用了响应式的设计。淘宝和一淘已经能够响应到iPad（_Width: 1024px_），36Kr更是桌面、平板、手机设备通吃。

响应式设计是通过 CSS3 的 Media Queryes 特性来实现的，众所周知，IE8 及更早期的版本对 CSS3 支持太差，但是在中国这个环境下，即时你可以无视IE6/7，但是 IE8 却是你不得不考虑的。幸运的是，有问题就有解决方案。

## respond.js

**[Respond.js]( https://github.com/scottjehl/Respond)** 是一个快速、轻量的脚本（3kb minified / 1kb gzipped），它能够使那些不支持 CSS3 Media Queryes 特性的浏览器支持基本的响应式设计。respond.js 压缩后1k，只实现了 media query 中最常用的 _min-width &amp;_ _max-width _的兼容，但是对于一般的响应式宽度网站设计也基本够用了。它可能不是唯一的 css3 Media query polyfill 脚本，但是它可能是最快的。

## css3-mediaqueries-js

目前实现兼容 css3 Media query 的库比较成熟的还有 **[css3-mediaqueries-js](https://code.google.com/p/css3-mediaqueries-js/ "https://code.google.com/p/css3-mediaqueries-js/") **。它基本实现了 css3 规范中 media query 所有特性的兼容，所以导致压缩有16kb，测试反馈其性能远低于 respond.js。有兴趣可以试一试。但个人更推荐前者。

为了测试 respond.js 我做了一个简单的 **[demo](http://huangyang.me/demo/media-query/)** 实际测试能够兼容 ie6 , ie8。
