---
layout: post
title: 教你怎么使用Markdown在Windows上愉快地写博文
---

	既然要开始写博文，那么就应该简单介绍一下我写博文所使用的工具啦，首当其冲的就是写博文需要用到的语法。

	下面就简单的来介绍Windows下比较好用的工具，还有一些简单的Markdown语法。

![是](http://img-storage.qiniudn.com/15-11-3/36900713.jpg)
##一、什么是Markdown
Markdown是一种轻量级的标记语言，可以很方便的进行排版，通过它，基本可以不使用鼠标就能够插入文本、链接、图片，这些统统用键盘就可以搞定了！很多网站都支持Markdown的文本输入。
##二、基本语法介绍
因为网络上有很多关于这个语言的教程，所以我就简单介绍一下一些基本语法吧，更加具体的用法大家可以[点击这里](http://wowubuntu.com/markdown/#list)
###1.标题
你可以很方便的设置文章的各级标题，仅仅通过「#」这个字符。如果你想要定义一个一级标题，只需要在其前面加上一个#号即可！

就像下面这样：

> \# 一级标题


> \## 二级标题


> \### 三级标题

他们所对应的效果是这样的：
![](http://ww1.sinaimg.cn/large/74311666jw1exo8ordku5j206205vt8v.jpg)

以此类推，一共有六级标题。

###2.插入图片或链接
两者的语法很接近，差别只有一个！号

插入链接：
> \[链接显示的文字](http://example.com)

插入图片：
> \!\[图片名](http://example.com/avatar.png)

这样就能够将图片和链接插进文章里面了。

由于图片需要图床，在这里推荐使用[极简图床](http://yotuku.cn/)来上传自己的图片，可以一键复制Mrakdown粘贴到自己的文章去，实在是很方便。
###3.引用
引用的效果如下：
> 这里是引用文

要做到这样的效果也很简单，只需要在文本面前加一个「>」号就好了，例如这样：

\> 这里是引用文
###4.加粗和斜体
想要给文字加粗和斜体非常简单，在文本两端用「\*\*」号包裹就是粗体，用「\*」来包裹一段文本则是斜体。

效果如下：
**粗体文本** *斜体文本*
##三、在Windows下有什么好用的Markdown编辑器吗？
首先请允许我安利一个非常好用的文本编辑器，[Sublime Text](http://www.sublimetext.com/3)，这是一个超好用的文本编辑器，可以用于阅读许多格式的代码文本，支持语法高亮和代码提示（虽然很弱=-=），甚至还可以直接用它来编译程序！此外还支持安装各种自定义主题，简直不能再好用了。

下面是我的Sublime Text的样子
![](http://ww2.sinaimg.cn/large/74311666jw1exo9amox7uj211x0ki0yk.jpg)

我用的主题是[Spacegray](http://kkga.github.io/spacegray/)，有兴趣的同学也可以去安装这个主题哟。
###1. 怎么用Sublime text写Markdown？
Sublime text有着非常丰富的插件以拓展功能，而全新安装的Sublime text是不能够很好的写MarkDown的，因此我们需要安装一个插件。
###2. 安装Package Control（如果已经安装则可以省略）
安装插件之前你首先需要安装一个Package Control用来管理你所安装的插件。

如果你是**Sublime Text 3**用户，按下Ctrl+\`呼出控制台（注意这个「\`」在键盘的左上角，有些同学可能找不到=-=），输入以下代码后**回车**

`import urllib.request,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)`



如果你是**Sublime Text 2**用户，同样也是按下Ctrl+\`呼出控制台，输入以下代码后**回车**

`import urllib2,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')`

在此之后Sublime text会联网下载需要的东西，你可以根据状态栏了解当前是否已经成功安装了Package Control。
###3. 安装Omni​Markup​Previewer
1. 打开命令面板（Command Palette），快捷键是Ctrl+Shift+P(Windows and Linux), ⌘+⇧+P(OS X)，也可以通过菜单栏找到Tools->Command Palette打开。

2. 输入"Install"，选择"Package Control: Install Package"

3. 输入"OmniMarkupPreviewer"，找到后回车选择，等待所需文件下载完成后即可使用！

###4. 怎么使用Omni​Markup​Previewer？
在Preferences->Packages Settings->Omni​Markup​Previewer->Settings可以找到Omni​Markup​Previewer的设置选项，当然通常情况下不需更改，如果你打算更改其中的配置建议参考[这篇文章](http://blog.leanote.com/post/54bfa17b8404f03097000000)。
在配置完成之后我们就可以开始写自己的文章啦！

打开新标签页，在右下角选择格式为Mrakdown，使用快捷键Ctrl+Alt+O,可以开启浏览器即时预览当前的文章，也就是说你每次的输入都会被马上渲染显示到浏览器中，是不是很方便？

好了，关于Markdown的相关内容暂时就这么多，因为我也是在学习当中，没办法写得很完美，如果我以后找到了更加好用的技巧我会继续分享的，大家也可以去网上找更多的教程继续学习！
