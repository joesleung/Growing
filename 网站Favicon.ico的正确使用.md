# 网站Favicon.ico的正确使用
*2013-07-18 16:47:38*

URL: /favicon-for-website.html

网站开发者都知道，过去，为保证favicon出现，很难明确地保证favicon可以在所有电脑上显示，即使是用同一版本的一种浏览器。下面是让网站显示favicon.ico的兼容性正确写法。

1.  在网站根目录位置放置favicon.ico文件，确保 _http://example.com/favicon.ico_ 能访问

2.  在网页的`<head></head>`放置两行代码：

`<link href="http://example.com/favicon.ico" rel="shortcut icon" type="image/vnd.microsoft.icon" />`
<link href="http://example.com/favicon.ico" rel="icon" type="image/vnd.microsoft.icon" />`


**注意：这两行代码只能添加在&lt;head&gt;&lt;/head&gt;之间。只有第一行是必须的，并且href可以，但不必指向/favicon.ico的位置。它可以指向任何URL。favicon.ico尺寸一般为32*32或16*16，大小一般控制在1k以下较好。**

顺便介绍两个Favicon制作（生成）工具：

1.  favicon.cc(Web在线应用，可以方便的制作或上传图片自动生成适合网页的favicon.ico文件)。[应用地址](http://www.favicon.cc/ "favicon.cc"

2.  Axialis IconWorkshop（一款专业的功能强大的图标制作工具，可以为windows，MacOS，UNIX系统甚至移动智能终端平台创建图标）[中文版官网](http://www.iconworkshop.cn/ "Axialis IconWorkshop")

了解更多可查看[维基百科](http://zh.wikipedia.org/wiki/Favicon "Favicon-维基百科，自由的百科全书")上的解释