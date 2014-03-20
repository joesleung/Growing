# 用CSS3动画制作单页面逐渐显示效果
*2013-07-27 11:14:41*


之前看到一个网站，在打开时，网页上的每一个元素不是（几乎）同时加载，而是逐个展现。这样显得页面很生动富有层次感。我很好奇这是用什么首段做到的。

先来看一下这个网站[NICK DOWNIE](http://www.nickdownie.com/ "NICK DOWNIE")（IE8-版本不支持）

一开始以为是用了javascript或者框架插件之类的。后来经过查看分析源码。才发现原来是**CSS3动画**（animation）。

![CSS3 animation](http://blogimages.u.qiniudn.com/NICK+DOWNIE.png)

既然知道了实现所采用的技术，那么要实现这种效果自然就没什么难了。

## 下面是关键的代码

**创建动画：**

    @keyframes flip {
     0% {
     transform: rotateX(90deg);
     }
     90% {
     transform: rotateX(-4deg);
     }
     100% {
     transform: rotateX(0deg);
     }
    }

**创建元素并附加上上面的动画：**

    #logo .top {
    position: absolute;
    left: -20px;
    top: -10px;
    width: 0;
    height: 0;
    border-left: 50px solid transparent;
    border-bottom: 50px solid #292b36;
    border-right: 50px solid transparent;
    border-top: 0;
    transform: rotateX(90deg);
    transform-origin: 100% 100%;
    animation: flip 800ms 800ms forwards;
    }

(注意：为了简化本文长度，一些css3属性并没有加浏览器前缀，真正使用时需加上)

对于如何创建和使用css3动画的更多内容，可以到[W3school](http://www.w3school.com.cn/css3/css3_animation.asp "CSS3 动画")有更详细准确的教程描述。

[**效果演示→**](http://huangyang.me/demo/css3-animation/ "CSS3 animation")
