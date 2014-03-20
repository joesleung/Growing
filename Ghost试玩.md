# Ghost试玩
2013-10-19 20:50:56

我说的 Ghost 可不是平常说的那种系统盘的意思。这个 [Ghost](http://ghost.org/) 是基于 [Node.js](http://nodejs.org/) 的Blog平台（Just a Blogging Platform）,它简洁纯粹，只做写blog这一件事，支持完全自定义，与生俱来的 Geek 气质并且当然是免费的！关于 Ghost 出现的原因和到底与Wordpress有什么关系和不同，可以去 [Ghost官网](https://en.ghost.org/)了解。

由于我使用的平台是OS X，所以下面只写在**Mac下的安装**，其他系统平台应该大同小异或者都可以找到相关教程。

## 安装Node.js

使用Ghost写博客的第一步是安装最近程序界谈论很火的 Node.js 。简单如下：

到 [node.js 官网](http://nodejs.org/) 首页点击 **DOWNLOADS 按钮，选择相应的安装文件。**

![install node](images/install-node.png)

下载完毕后，找到下载的文件 node-v0.10.21.pkg （注：文件名依据版本号会有所不同）双击，按正常方式安装。这一步很简单，唯一需要注意的是 $PATH 路径问题，调出“终端”（Terminal），调试 _echo $PATH _命令，看是否有 _/usr/local/bin/ _路径。

![install-node-path](http://blogimages.u.qiniudn.com/install-node-path1.png)

**Node在Mac下的整个安装过程**如下：

![install node on mac](http://huangyang.qiniudn.com/install-node-mac.gif)

## 安装和运行 Ghost

同样是先到[官网下载]( http://ghost.org/)最新版的ghost压缩文件。解压文件夹（如：ghost-0.3.3）。打开终端，把文件夹拖入新标签栏（小心这一步，如果看不到终端标签栏，可以快捷键 shift＋cmd＋T 呼出）。输入 _npm install --production _，然后等待片刻（大概2-30秒），待 npm 安装完毕，输入 _npm start_ 启动Ghost。之后在浏览器地址栏输入： 127.0.0.1:2368 ，OK的话就可以看到Ghost的welcome页面啦！

![ghost welcome](http://blogimages.u.qiniudn.com/ghost-welcome.png)

**Ghost在Mac下的这一步安装过程**如下：

![install ghost mac](http://huangyang.qiniudn.com/install-ghost-mac.gif)

怎么安装就先写到这儿吧，简单吧！当然真正玩起来肯定不会那么简单，做Geek就免不了折腾。我对Node.js也算是小白一个，可能也是被微博社区什么的热了脑子，但是我觉得，学习总不会错的，动手才是学习最好的老师。

歇了，至于怎么玩、怎么在Ghost上写东西，下次再折腾吧。

（补充：看到网上有个 [Ghost环境一键安装工具](http://bitnami.com/stack/ghost)，自己没有试，有兴趣的可以尝试一下。）