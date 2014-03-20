Title: I Give You My CSS3 Heart——CSS3绘制心型

Date: 2013-07-22 10:08:28

URL: /css3-heart.html

使用CSS3强大的圆角（`border`）属性，配合CSS中的`:before`伪元素就可以轻松绘制一个“心”型图案，省去了加载图片，并且可以自定义颜色等。下面是绘制“心”型的CSS代码，同时还让它在页面水平垂直居中。在不支持CSS3圆角属性的浏览器（如：IE8-）是看不到的。

**CSS代码：**

    #heart {
    position: relative;
    width:100px;
    height:90px;
    }
    #heart:before,#heart:after {
    position: absolute;
    content:"";
    left:50px;
    top:0;
    width:50px;
    height:80px;
    background: #f00;
    -moz-border-radius:50px 50px 0 0;
    border-radius:50px 50px 0 0;
    -webkit-transform: rotate(-45deg);
    -moz-transform: rotate(-45deg);
    -ms-transform: rotate(-45deg);
    -o-transform: rotate(-45deg);
    transform: rotate(-45deg);
    -webkit-transform-origin:0 100%;
    -moz-transform-origin:0 100%;
    -ms-transform-origin:0 100%;
    -o-transform-origin:0 100%;
    transform-origin:0 100%;
    }
    
    #heart:after {
    left:0;
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -ms-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    transform: rotate(45deg);
    -webkit-transform-origin:100% 100%;
    -moz-transform-origin:100% 100%;
    -ms-transform-origin:100% 100%;
    -o-transform-origin:100% 100%;
    transform-origin :100% 100%;
    }

**HTML:**

    <div id="heart"></div>

演示[Demo](http://huangyang.me/demo/css3-heart/ "CSS3绘制心型")