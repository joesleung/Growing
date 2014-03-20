# Emmet，又一个强大的Sublime插件
2013-08-15 11:47:51


在用过Sublime Text 2这个强大的编辑器之后，我就打算彻底抛弃其他编辑器（包括过去一直偏爱的Dw）甚至IDE了。Sublime Text凭借其对多种平台的支持（OS X, Windows &amp; Linux）、免费（可永久试用）、轻巧优雅和强大的插件扩展吸引了我。

![Sublime-Text-2](http://blogimages.u.qiniudn.com/Sublime-Text-2.jpg)

之前介绍过ST2上的一个很实用的SFTP插件的安装配置和使用，今天说一个可谓前端开发神器的ST2插件：**Emmet**。实际上，使用它能够大大提升码字的速度和效率，避免无意义的重复劳动，让你更多的把时间和精力专注于代码的质量上。

Emmet使用起来非常简单，最重要的一点是记住**Tab键**。下面介绍一些技巧。

**生成 HTML 文档初始结构**

用ST2新建或打开一个空的HTML文档，然后输入`html5`，点击**Tab键**，奇迹出现。

    <!DOCTYPE html>
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <title></title>
            <link rel="stylesheet" href="">
        </head>
        <body>
        </body>
    </html>

**生成标签**

如，想生成一对 `<div></div>` 标签，你只需输入 `div` ，然后**Tab**。

**生成带有 id 、class 的 HTML 标签**

如，想生成 `<div class="cont"></div>` ，只需输入 `div.cont` ，然后**Tab**。（id也一样）。

**生成一段随机文字**

只需要输入 `lorem` ，然后**Tab**即可。这能让开发者忽略内容的含义而专注内容的排版，可作为测试数据填充用。

还有很多很多实用的用法技巧可以看看我爱水煮鱼的[这篇文章](http://blog.wpjam.com/series/frontend-develop-tool-emmet/ "前端开发神器 Emmet")。不过我在测试后发现并不是完全能够实现一些功能。不知道是因为这个插件已经做了调整还是因为与我安装的其他插件有冲突造成的。不过基本的一些功能已经很实用很强大了，Emmet仍然是一个值得安装的前端开发者的ST插件。
