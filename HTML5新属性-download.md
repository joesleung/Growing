# HTML5中a标签的新属性：download
2013-07-18 22:26:06


HTML5新增了一些标签，他们优雅，富含语义。也淘汰了一些过时的，无意义的标签。`<a>`标签作为超链接标签，虽然在HTML5中没有添加新的语义，但是却新增了一个目前还很少有人知道和应用的`download`属性。通过`<a>`标签设置download属性，可以让浏览器生成下载窗口下载文件，而不是直接跳到url链接上去。如下：

    <a href="img/photo.jpg" download="img">下载图片</a>

其中href后面是需要下载的文件的url（如果是链接到页面则会下载此页面）downlond的参数（上面代码中的img）是指定下载文件名，它不一定是原文件名(上面代码中的photo)

需要注意的是，此属性**目前只有Chrome浏览器才支持，**这也许就是到目前_(2013-07)_为止很少有人知道和使用此属性的原因吧。并且我自己也几乎找不到互联网上有关此属性的一些更多信息。如果你知道的更多，可以给我留言，大家一起学习一起纠正，不胜感激。

演示：

- <a href="http://huangyang.qiniudn.com/poster.jpg">下载图片（无download属性</a>
- <a href="http://huangyang.qiniudn.com/poster.jpg" download="img">下载图片（添加了download属性）</a>
