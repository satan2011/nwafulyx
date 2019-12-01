# 自用西北农林科技大学LyX模板 #

* 1、本模版主要参考中科院USTCLyx模版修改而来，根据西北农林科技大学博士论文撰写要求进行了修改，主要添加了双语标注、修改目录的间距和字体格式、修改各级标题的标题样式及标注格式，已基本满足使用需求。
* 2、关于论文封面，由于时间和技术限制未能实现首页的编译。首页采用cover.word输出PDF文档后，通过Lyx嵌套PDF实现。
* 3、文档中的“西农模版说明.pdf”主要是引用西农耿老师latex模版编改指南；“西北农林科技大学模版要求.docx”是西农的论文格式要求。

“中科院大学模版说明.pdf”和“中国科学院大学模版要求.pdf”是USTClyx模版的编改指南和中科院大学USTC的论文格式要求。

提供上面四个文件，方便进行比较和修改。

* 耿楠老师的latex模版
https://github.com/registor/nwafuthesis



## 目的 ##

西北农林科技大学博士论文LyX模板，方便西农博士研究生编辑学位论文。

* 底层了调用[ustcthesis latex模板](https://github.com/ustctug/ustcthesis)，目前只支持博士论文。
* 包含了各种环境、格式实例，根据需求，直接在Lyx中复制粘贴即可。

## 下载 ##

* 下载最新发布版本，压缩文件 https://github.com/satan2011/nwafulyx/releases , 解压即可使用。

* 此外，还可以使用git克隆项目，从而下载最新版，或者参与项目开发。

  
## 使用 ##

* 下载安装 Texlive， 参考 [ustcthesis 新手指南](https://github.com/ustctug/ustcthesis/wiki/新手指南)。

  USTCer 推荐校内在线安装, 注意选择 “Change default repository”，并且选择中国科大的 mirror：

  * Windows系统：

     <http://mirrors.ustc.edu.cn/CTAN/systems/texlive/tlnet/install-tl-windows.exe>

  * 其他系统：

    <http://mirrors.ustc.edu.cn/CTAN/systems/texlive/tlnet/install-tl-unx.tar.gz>

* 下载最新版[LyX](https://www.lyx.org/Download). LyX 版本要求 >= 2.3。

  注意先安装texlive，再安装LyX， LyX可以自动识别latex路径，并配置。 如果后安装texlive, 需要在LyX中设置，菜单： 工具->重配置LyX。重启LyX。

* 选择学位论文类型：

  打开Main.lyx文档，菜单 文档->首选项->文档类->文档类选项。填写文档类选项，默认为doctor。

  * doctor	  博士模版


* 编译：

  Main.lyx文档中点击👀[查看]图标，编译可获得整篇论文的pdf；在子章节文件中，点击👀[查看]图标，获得单独章节的pdf。

* 创建新文件：

  请copy Introduction.lyx, 然后重命名。如果直接新建文档，需要按照Introduction.lyx的文档属性重新设置，采用拷贝重命名的方法可以避免这个问题。

* 更具体技巧见模板中Introduction.yx 和 skill.lyx


## 为何LyX 

1. 可视化地编辑Tex。
2. 与latex一样，可以结构化包含文档。并且编辑器提供的目录、导航、标签等功能，可以快速方便地定位、显示内容。编撰比较大的工程，例如书籍类工程， 这个功能会很重要。
3. 存在与Word类似的修订模式，方便多人编辑。
4. 方便的自动编译过程，只需要一次按键即可。
5. 内部许多文件转换器，支持较多的文件格式。
6. 与其他工具有很好的接口（Jabref， Inkscape，Zotero）。

　　. . . . . 

主要前两点，引入latex优点的同时，克服了编辑文本不友好、不直观问题。避免反复编译文档，因此可以极大提高撰写论文的效率。设计本论文模版的目的就是为了方便广大USTCer攥写学位论文，将写作精力放在论文内容上。

## 模版原理

本LyX模版的latex底层使用ustcthesis模版，[github链接](https://github.com/ustctug/ustcthesis)。感谢众多USTCer的努力，这个模版已经是研究生院认可的学位论文模版[学位论文模版](https://gradschool.ustc.edu.cn/ylb/xw.html)。本模版主要在ustcthesis模版上加了一个Lyx layout层 (USTCtheisis.layout文件)，在此基础上定义了一些常用的命令，以方便编辑文档。

ustcthesis中模版选项：

````
% 学位论文类选项
doctor|master|bachelor [academic|professional] [chinese|english] [print|pdf]
% 参考文献选项
[super|numebers|authoryear]
````

详细说明参考[ustcthesis](https://github.com/ustctug/ustcthesis)。
