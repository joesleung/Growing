# Sublime下进行FTP配置
2013-07-22 20:43:30

URL: /sublime-sftp.html

## 我的配置环境：

*   操作系统 Windows 8（x32

*   Sublime版本 Sublime Text 2（2.0.2

*   所用插件 [Sublime SFTP](http://wbond.net/sublime_packages/sftp "SFTP")

## 插件安装：

假设你已经安装了[Sublime Text 2](http://www.sublimetext.com/2 "Sublime Text 2")(以下简称ST2)了，并安装好了ST2的扩展管理器（如果不知道如何安装请移步[这里](http://www.iplaysoft.com/sublimetext.html)）。

接下来要安装一款叫做[SFTP](http://wbond.net/sublime_packages/sftp "SFTP")的插件。

打开ST2，按**ctrl+shift+p**(Windows and Linux)或者**cmd+shift+p**（OS X），输入“IP”即可找到**Package Control:Install Package**这一项。输入“FTP”，找到**SFTP**这款插件，选中后回车或双击，等待片刻即可安装完毕。

## 插件配置：

选择左上方的菜单栏 **File-&gt;SFTP/FTP-&gt;Set up Server**，打开。然后选择、填入相关配置参数。主要有主机名（域名地址或IP）、FTP用户名、FTP用户密码、端口号、默认路径等。用过FTP上传软件的应该一看就明白了。有些配置参数默认注释掉了（如：密码），需要去掉注释再该填上自己的配置信息。

配置完成上述信息，然后Ctrl+S，输入一个文件名（最好为字母或数字组合）保存即可。

![SFTP](http://blogimages.u.qiniudn.com/sftp1.png)

![sftp2](http://huangyang.me/wp-content/uploads/2013/07/sftp2.png)

## 使用：

点击 **File &gt; SFTP/FTP &gt; Browse Server**（查看服务器列表），找到需要编辑的文件路径，找到文件，点击**Edit**开始编辑。按Ctrl + S 保存文件时，会自动上传文件到服务器。

![sftp3](http://blogimages.u.qiniudn.com/sftp3.png)

本文作者[黄杨的博客](http://huangyang.me/sublime-sftp.html "黄杨的博客")，转载请保留此段，谢谢