# 让footer始终显示在页面底部
*2013-07-26 15:17:33*


## 遇到的问题：

当页面内容（#container）高度不足以撑开浏览器高度时，有时会出现页脚（footer）跟随内容的底部，而不是我们希望的始终显示在（浏览器）页面的底部。

## 解决方案：

HTML:

    <div id="container">
        <div id="content">页面正文</div>
    </div>
    
    <div class="footer"></div>

CSS:

    html, body{
        height:100%;
    }

    #container {
        min-height:100%; /*使内容高度和body一样*/
        margin-bottom:-80px;/*向上缩减80像素，不至于footer超出屏幕可视范围*/
    }

    #content {
        padding-bottom:150px; /*这个是关键，处理页面高度超出屏幕可视范围时，控制内容和底部高度之间距离*/
    }
    #footer {
        height:80px;
    }
