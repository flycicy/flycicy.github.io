---
title: 使用Github搭建自己的博客
---


如果你也经历过Myspace、Blogbus的式微，就会有所感触：写个博客需要不停搬家，哪都不能久留。GoogleReader停止服务更是让本不坚定的作者转向流量较高的微博与微信公众账号。但不可否认的是，文字和思考是需要沉淀的，Blog lovers永远在寻找一个可以栖息的博客之家。

本篇文章希望能帮助到想要用有逼格的方式来搭建个人博客的你。关键词搜索就能发现，不少大牛已经总结了Github搭建博客的要点，但即使只是简单的代码，但对于小白来说都稍显晦涩——很多人都只是有“写作”的需求而已，不想深入学习代码怎么码。与之前的攻略文不同的是，本篇文章没有”Ruby“，没有”命令“，不需安装任何看上去很可怕的软件，所有操作面向小白用户描述，只需要你有耐心与细心。

## 工具：Github + Jekyll + Markdown

### Github

>如果你对互联网的热门产品有所了解，你一定听说过Github。Github是面向开发者的社区，开发人员可以在个人页面中发布自己的代码，并允许别人Fork（合法的copy）与修改，并合并成更好的版本。它开放式的开发与协作方式广受好评。

Github本身就很Geek，而且博客的建立与维护在同一个地方，方便管理。Github还有Commit功能，能记录每次迭代的内容（甚至还有前后对比！），强迫症们可以反复修改并选择自己满意的版本发布。

### Jekyll
>Jekyll是很棒的网页生成工具，它能将文本转化为静态的网站和博客，你不需要关心数据库、版本，只需要专注于网站维护。

Jekyll的官方网站[http://jekyllrb.com/](http://jekyllrb.com/)，这里有高阶利用Gem包使用Jekyll命令的教学，懂Git的同学可深入阅读。小白同学只要知道我们会用到这个叫Jekyll(/'dʒiːk əl/)很棒的搭建方法就好了。

### Markdown

>Markdown是一种流行的标记语言，它可以让文字赋予格式，用简洁的语法来标注层级与链接等，并在多个平台内可识别。Markdown语法可以让人在书写时专注于文字本身而不是排版。现在许多作家都会使用Markdown语法来撰写文章，而很多编辑器也支持Markdown语法。

Markdown语法非常简单，只需学习10分钟就可上手。可以参考这篇文章：[Markdown——入门指南](http://www.jianshu.com/p/1e402922ee32/)

Markdown可以直接打开“记事本”直接开写，当然也可以利用合适的**编辑器**来高亮语法获得更好的书写体验：

- MAC OS X下推荐：[Ulysses](http://www.ulyssesapp.com/)
- Windows系统下推荐：[Sublime](http://www.sublimetext.com/)

## 思路：盖房子
可以用一个房子从无到有的过程来比喻我们的博客搭建思路，即：“搭建好空房子-复制别人的样板房-按自己的风格做软装-日常维护”.

1. 搭好空房子：在Github里建立自己的空间；
2. 照搬别人的样板房：选择别人搭配好的Jekyll主题模板；
3. 按自己的风格做软装：在Github中更换属于自己的标题与文章，甚至皮肤。
4. 日常维护：新增或修改文章

### 第一步：在Github上搭建自己的空间
![注册](http://ww2.sinaimg.cn/large/623478fegw1evgexkdnfpj20dn0g6ju3.jpg)
这一步非常简单，注册一个Github账号即可。Github会为用户保留一个username.github.io的二级域名，我们就是在这里存放博客文件的。接下来我们会使用**username**来替代你的用户名。

### 第二步：选择并Fork一个Jekyll模板

Jekyll的模板很多，Google关键词"Jekyll Theme"即可得到一大堆结果。这里我们选择[http://jekyllthemes.org/](http://jekyllthemes.org/)来做示例。

>**如何挑选模板**？
请考虑一下博客使用的场景——如果您的博客大部分是文字，请选择文字间距大、以文字为主题的博客；如果您的博客主要用来展示您的摄影作品，请设想一下哪个模板对展示多图片有很好的效果。挑好模板就像定了家居的风格，请按照博客定位来选择合适的模板。	

这里选择[**Tiffany**](http://jekyllthemes.org/themes/tiffany/)这个模板

![选择Tiffany模板](http://ww3.sinaimg.cn/large/623478fegw1evgfe9dor5j20kh06st9r.jpg)

- 选择模板后，点击"Homepage"跳转到作者的Github主页中。

- 点击“Fork”来复制一份项目文件到你自己的Github库中
![Fork](http://ww1.sinaimg.cn/large/623478fegw1evgewvbl95j20sb09jtaq.jpg)

- **这一步非常重要：**请把这个项目的名称改为“**username**.github.io”才能在页面上显示。先找到Settings，

![修改名称](http://ww1.sinaimg.cn/large/623478fegw1evgf0yynspj20s407xwge.jpg)

然后将项目的名称改为“**username**.github.io”

![Rename](http://ww3.sinaimg.cn/large/623478fegw1evgf1xxzf1j20jx079t9h.jpg)

这一步我们就完成了“复制样板房”的工作，你可以在username.github.io这个地址里随时预览你的装修。接下来将进入需要**考验耐性**的软装阶段。

### 第三步：在你的Repository中修改模板

修改模板通常会做的事包括：修改Ttitle、头像、主题、颜色、链接等等……如果你不知道在哪里修改，下面是一个简单的方法：

1. 首先Google CSS样式名称，如“字体修改 CSS”，找到属性名称为为“font-family”。

2. 在自己的repository中搜索关键词“font-family”找到存放样式的位置。
![搜索](http://ww2.sinaimg.cn/large/623478fegw1evgez4xvvuj20ql07bt9l.jpg)
3. 找到“font-family”所在行，可以通过简单学习W3C中的方法来修改字体。值得注意的是，不能直接点击文件修改，因为搜索结果是Fork作者的文件，需要再自己的库中同样的路径找到存放的文件。
![结果](http://ww2.sinaimg.cn/large/623478fegw1evgezwhybdj20qc0awmzj.jpg)
当然也可以更换模板的背景与图片及删减及新增功能。这一步很难但写的比较潦草，首先因为每个模板情况都不同不可一概而论，另外的确需要静下心来现学现用学习一些html知识，小白嘛只能反复试错得到正确的答案。
[使用 GitHub, Jekyll 打造自己的免费独立博客](http://blog.csdn.net/on_1y/article/details/19259435)这篇文章有详细介绍核心的文件及其包含的内容。如_layouts中包含模板，index.html是首页等。

### 第四步：新增或修改文章
找到Post文件夹就会发现里面是作者原来存放的文章，在这里只要选择删除旧文章，增添自己的新文章就好。
新文章的命名与撰写都需要按照格式来，很方便的一点是在原作者的一篇文章中选择“edit”然后复制作者前部分的格式，粘贴在新文章里在对应的位置做修改就ok啦。
访问**username**.github.io来预览你的个人博客。

>由于Github每次更新都需要遍历所有文件，所以需要等一会才能在页面呈现你的修改。

### 有自己的域名？
可以使用新建CNAME文件将你的域名与Github博客绑定，这种文章很多也很易懂，详情咨询度娘。

##成果展示

如果你成功按照本文方法在Github上搭建了自己的窝，欢迎回复地址秀一下~
>博客搭建感谢最帅气最可爱的@汤煲粥。
本文博客地址：xxxxxxxxxxxx
