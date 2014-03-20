# Remove Tap Highlight from Mobile Webkit


`-webkit-tap-highlight-color: <color>;`

说明：默认情况下，mobile Safari 浏览器会对超链接文字，表单输入/提交空间等，在触发时默认添加短暂的阴影效果。

Apple 此举大概在于告诉用户当前聚焦到页面的什么地方。但实际使用中有时可能不需要这种效果。

解决方案：

`-webkit-tap-highlight-color: rgba(0,0,0,0);`

严格的说，这个办法并没有关掉 tap highlight，只是把 highlight 颜色设置成完全透明的白色。对不喜欢这个效果的同学，直接把这个设置放在 body 里，页面就干净了。

更多属性规则：

	*{
        -webkit-touch-callout:none;                /* prevent callout to copy image, etc when tap to hold */
        -webkit-text-size-adjust:none;             /* prevent webkit from resizing text to fit */
        -webkit-tap-highlight-color:rgba(0,0,0,0); /* prevent tap highlight color / shadow */
        -webkit-user-select:none;                  /* prevent copy paste, to allow, change 'none' to 'text' */
    }