Title: jQuery实现侧边栏跟随浏览器滚动固定显示

Date: 2013-07-18 20:34:56

URL: /jquery-pin-fixed.html

开发中，有时需要将页面的一些组建（通常是导航、侧边栏等）在跟随浏览器滚动到顶端时开始固定显示。下面是实现这一功能的方法

## 1 jQuery.Pin插件

插件地址：[jQuery.Pin](http://www.bootcss.com/p/jquery.pin/ "jquery.pin")

此插件能将任意页面元素“钉”在某个容器顶部，并且可以在尺寸小的屏幕上将其自动禁用。

使用起来很简单：

    $(".pinned").pin()

当然需首先引入jQuery库及`jquery.pin.js`插件，然后只需进行简单的引用和设置即可钉住你的网页元素。具体的内容在[Pin插件网站](http://www.bootcss.com/p/jquery.pin/)已经讲的很详细了就不再多说。

**目前这个插件不支持IE8-浏览器。**

## 2 Sidebar Follow插件

插件地址：[sidebar follow](https://github.com/wuzhao/sidebar-follow)

来自[wuzhao](https://github.com/wuzhao)写的插件，当页面滚动到跟随区域下方，跟随区域将固定在窗口上。适用于所有网站侧边栏。兼容IE8。

具体使用请查看此开源项目，还是比较方便的。希望自己也尽快学好js，写一些自己常用的优秀的插件来。

## 3 jQuery代码

如果嫌引用代码还不够方便，并且想尽可能的给页面“减负”，也可以使用如下代码：

**JS**

    //侧栏跟随浏览器
    
    $(function () {
        if ($(".fixed_side").length &gt; 0) {
            var offset = $(".fixed_side").offset();
            $(window).scroll(function () {
                var scrollTop = $(window).scrollTop();
                //如果距离顶部的距离小于浏览器滚动的距离，则添加fixed属性。
                if (offset.top &lt; scrollTop) $(".fixed_side").addClass("fixed");
                //否则清除fixed的css属性
                else $(".fixed_side").removeClass("fixed");
            });
        }
    });

**CSS**

    .fixed{position:fixed; top:20px; width:250px;}

另外还有**带滑动效果**的侧边栏随窗口滚动jQuery代码：

    <script>
    var documentHeight = 0;
    var topPadding = 15;
    $(function() {
        var offset = $("#sidebar").offset();
        documentHeight = $(document).height();
        $(window).scroll(function() {
            var sideBarHeight = $("#sidebar").height();
            if ($(window).scrollTop() &gt; offset.top) {
                var newPosition = ($(window).scrollTop() - offset.top) + topPadding;
                var maxPosition = documentHeight - (sideBarHeight + 300);
                if (newPosition &gt; maxPosition) {
                    newPosition = maxPosition;
                }
                $("#sidebar").stop().animate({
                    marginTop: newPosition
                });
            } else {
                $("#sidebar").stop().animate({
                    marginTop: 0
                });
            };
        });
    });
    </script>
    
修改 `#sidebar` 为你网站侧边栏选择器名称即可。