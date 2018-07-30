# web

标签（空格分隔）： web

---

[TOC]

web 全栈指南

### 工具篇
工欲善其事，必先利其器，好的工具能使开发事半功倍，要善于利用工具
#### Git
代码版本管理工具
##### 常用操作
###### 配置用户信息

    git config --global user.name "smyhvae"
    git config --global user.email "smyhvae@163.com"

#### 网页三剑客(逐渐废弃)
Adobe Dreamweaver，Adobe Fireworks(Photoshop)，Adobe Flash.
原型图工具Sketch
#### VS Code
#### Sublime Text
#### WebStorm
##### 主题修改
选择菜单栏“File--settings--apperance--theme”，修改主题
![此处输入图片的描述][1]
或者获取[第三方主题][2]
![此处输入图片的描述][3]
主题下载完成后是一个jar包，将jar包导入即可：File-->Import Settings
##### 字体修改
选择菜单栏“File--settings--Editor--Font”：
![此处输入图片的描述][4]
上图中，点击红框部分，然后弹出如下界面：
![此处输入图片的描述][5]

##### 关闭更新
![此处输入图片的描述][6]

##### 文件编码
![此处输入图片的描述][7]

##### 新建项目
![此处输入图片的描述][8]

##### 快捷键
##### 标签环绕

输入一段字符后，按住`Ctrl+Alt+T`，可以用标签将这段字符环绕：
![此处输入图片的描述][9]

#### ATOM
#### Chrome
#### shell配置
见链接[iTerm2+oh-my-zsh配色][10]
#### icomoon
[链接][11]

#### 常用链接
[资料汇总][12]

### HTML篇
#### web标准

 - w3c:万维网联盟组织，用来制定web标准的机构（组织）
 - 结构标准：HTML
 - 表现标准：CSS
 - 行为标准：JavaScript

#### HTML介绍
**HTML**全称为HyperText Mackeup Language，译为**超文本标记语言**，不是一种编程语言，是一种描述性的标记语言，用于描述超文本中内容的显示方式。比如字体什么颜色，大小等。

 - 超文本：音频，视频，图片称为超文本。
 - 标记：<英文单词或者字母>称为标记，一个HTML页面都是由各种标记组成。
HTML是负责描述文档**语义**的语言，HTML页面直接由浏览器解析执行。
html是一个纯本文文件（就是用txt文件改名而成），用一些标签来描述文字的语义，这些标签在浏览器里面是看不到的，所以称为“超文本”，所以就是“超文本标记语言”了。 所以，接下来，我们肯定要学习一堆html中的标签对儿，这些标签对儿能够给文本不同的语义。

#### HTML历史
![此处输入图片的描述][13]
这里我们需要解释下HTML和XHTML

 - XHTML：Extensible Hypertext Markup Language，可扩展超文本标注语言。 XHTML的主要目的是为了取代HTML，也可以理解为HTML的升级版。 HTML的标记书写很不规范，会造成其它的设备(ipad、手机、电视等)无法正常显示。 XHTML与HTML4.0的标记基本上一样。 XHTML是严格的、纯净的HTML。

了解了HTML，这里对web开发中的一些常用术语做一下解释：

 - 网页 ：由各种标记组成的一个页面就叫网页。
 - 主页(首页) : 一个网站的起始页面或者导航页面。
 - 标记： <p>称为开始标记 ，</p>称为结束标记，也叫标签。每个标签都规定好了特殊的含义。
 - 元素：<p>内容</p>称为元素.
 - 属性：给每一个标签所做的辅助信息。
 - xhtml： 符合XML语法标准的HTML。
 - dhtml：dynamic，动态的。javascript + css + html合起来的页面就是一个dhtml。
 - http：超文本传输协议。用来规定客户端浏览器和服务端交互时数据的一个格式。SMTP：邮件传输协议，ftp：文件传输协议。

#### HTML中的颜色
有三种表示方式：

 - 纯单词表示：red、green、blue、orange、gray等
 - 10进制表示：rgb([0-255],[0-255],[0-255])
 - 16进制表示：#FF0000、#0000FF、#00FF00等

**RGB色彩模式**：
自然界中所有的颜色都可以用红、绿、蓝(RGB)这三种颜色波长的不同强度组合而得，这就是人们常说的三原色原理。
RGB三原色也叫加色模式，这是因为当我们把不同光的波长加到一起的时候，可以得到不同的混合色。例：红+绿=黄色，红+蓝＝紫色，绿+蓝=青
在数字视频中，对RGB三基色各进行8位编码就构成了大约1678万种颜色，这就是我们常说的真彩色。所有显示设备都采用的是RGB色彩模式。
RGB各有256级(0-255)亮度，256级的RGB色彩总共能组合出约1678万种色彩，即256×256×256=16777216。

#### HTML规范

 - HTML是一个弱势语言
 - HTML不区分大小写
 - HTML页面的后缀名是html或者htm(有一些系统不支持后缀名长度超过3个字符，比如dos系统)
 - HTML的结构：
    -  声明部分：主要作用是用来告诉浏览器这个页面使用的是哪个标准。<!doctype html>是HTML5标准。
    -  head部分：将页面的一些额外信息告诉服务器。不会显示在页面上。
    -  body部分：我们所写的代码必须放在此标签內。


#### XHTML规范

 - 所有标记元素都要正确的嵌套，不能交叉嵌套。正确写法举例：`<h1><font></font></h1>`
 - 所有的标记都必须小写。
 - 所有的标记都必须关闭。
     - 双边标记：`<span></span>`
     - 单边标记：`<br>` 转成 `<br />` `<hr>` 转成 `<hr />`，还有`<img src=“URL” />`
 - 所有的属性值必须加引号。`<font color="red"></font>`
 - 所有的属性必须有值。`<hr noshade="noshade">、<input type="radio" checked="checked" />`
 - XHTML文档开头必须要有DTD文档类型定义

 #### HTML语法特性
 **HTML对换行不敏感，对tab不敏感**
 HTML只在乎标签的嵌套结构，嵌套的关系。谁嵌套了谁，谁被谁嵌套了，和换行、tab无关。换不换行、tab不tab，都不影响页面的结构。
 **空白折叠现象**
 HTML中所有的文字之间，如果有空格、换行、tab都将被折叠为一个空格显示。
 **标签要严格封闭**
 
 #### HTML结构
 1、文档声明头
 任何一个标准的HTML页面，第一行一定是一个以
 > `<!DOCTYPE ……`
 
开头，此标签可告知浏览器文档使用哪种 HTML 或 XHTML 规范。
 
首先我们先确定一件事儿，我们现在学习的是HTML4.01这个版本，这个版本是IE6开始兼容的。HTML5是IE9开开始兼容的。但是IE6、7、8这些浏览器还不能过早的淘汰，所以这几年网页还是应该用HTML4.01来制作。如今，手机、移动端的网页，就可以使用HTML5了，因为其兼容性更高。

说个题外话，html1 至 html3 是美国军方以及高等研究所用的，并未对外公开。
2、头标签

头标签都放在头部分之间。包括：`<title>`、`<base>`、`<meta>`、`<link>`

 - `<title>`：指定整个网页的标题，在浏览器最上方显示。
 - `<base>`：为页面上的所有链接规标题栏显示的内容定默认地址或默认目标。
 - `<meta>`：提供有关页面的基本信息
 - `<body>`：用于定义HTML文档所要显示的内容，也称为主体标签。我们所写的代码必须放在此标签內。
 - `<link>`：定义文档与外部资源的关系。

如下一段样例：

    <!doctype html>
    <html lang="en">
     <head>
      <meta charset="UTF-8">
      <meta name="Generator" content="EditPlus®">
      <meta name="Author" content="">
      <meta name="Keywords" content="">
      <meta name="Description" content="">
      <title>Document</title>
     </head>
     <body>
    
     </body>
    </html>

（1）字符集 charset
在头标签中，有下面这种标签：

    <meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
    
字符集用meta标签中的charset定义，meta表示“元”。“元”配置，就是表示基本的配置项目。

（2）定义“关键词”

    <meta name="Keywords" content="网易,邮箱,游戏,新闻,体育,娱乐,女性,亚运,论坛,短信" />
    
这些关键词，就是告诉搜索引擎，这个网页是干嘛的，能够提高搜索命中率。

（3）定义“页面描述”
meta除了可以设置字符集，还可以设置关键字和页面描述。

我们把含有meta标签的这一行代码抽象一下：

    <meta name=" " content=" ">

name即“名字”，content即“内容”。
只要设置Description页面描述，那么百度搜索结果，就能够显示这些语句，这个技术叫做SEO（search engine optimization，搜索引擎优化）。

（4）title标签

    <title>网页的标题</title>

title也是有助于SEO搜索引擎优化的。

3、`<body>`标签的属性

 - bgcolor：设置整个网页的背景颜色。
 - background：设置整个网页的背景图片。
 - text：设置网页中的文本颜色。
 - leftmargin：网页的左边距。IE浏览器默认是8个像素。
 - topmargin：网页的上边距。
 - rightmargin：网页的右边距。
 - bottommargin：网页的下边距

#### HTML标签
这是我们学习的重点，也是我们主要书写的东西。
##### 注释标签

    <!-- 注释  -->

##### 段落标签`<p>`

    <p>This is a paragraph</p>
    <p>This is another paragraph</p>
    
属性：

 - align: 对其方式，包括left center right。 例如![此处输入图片的描述][14]HTML标签是分等级的，HTML将所有的标签分为两种：
     - 文本级标签：p、span、a、b、i、u、em。文本级标签里只能放文字、图片、表单元素。（a标签里不能放a和input）
     - 容器级标签：div、h系列、li、dt、dd。容器级标签里可以放置任何东西。
**p标签是一个文本级标签，p里面只能放文字、图片、表单元素。**


##### 块级标签
div：把标签中的内容作为一个块儿来对待(division)。必须单独占据一行。
**`<span>`和`<div>`唯一的区别在于：`<span>`是不换行的，而`<div>`是换行的。**
div在浏览器中，默认是不会增加任何的效果的，但是语义变了，div中的所有元素是一个小区域。 div标签是一个容器级标签，里面什么都能放，甚至可以放div自己。

span也是表达“小区域、小跨度”的标签，但是是一个文本级的标签。 就是说，span里面只能放置文字、图片、表单元素。 span里面不能放p、h、ul、dl、ol、div。

##### 换行标签`<br>`
当你打算结束一行，而又不想开始一个新段落时，`<br>`标签就派上用场了。

##### 水平线标签`<hr>`

##### 内容居中标签 `<center>`
此时center代表是一个标签，而不是一个属性值了。只要是在这个标签里面的内容，都会居于浏览器的中间。

##### 预定义（预格式化）标签
`<pre>`
将保留其中的所有的空白字符(空格、换行符)，原封不动的输出结果

##### 字体标签
标题使用`<h1>`至`<h6>`标签进行定义。`<h1>`定义最大的标题，`<h6>`定义最小的标题。具有align属性，属性值可以是：left、center、right。 

##### 特殊字符

 - `&nbsp;` ：空格
 - `&lt;`：小于号
 - `&gt;`：大于号（greater than）
 - `&amp;`：符号&
 - `&quot;`：双引号
 - `&apos;`：单引号
 - `&copy;`：版权©
 - `&trade;`：商标™

##### 装饰标签

 - `<u>`: 下划线
 - `<s>`/`<del>`：删除线
 - `<i>`/`<em>`：斜体标记
 - `<b>`/`<strong>`：粗体标签
 - `<sup>`：上标
 - `<sub>`：下标

##### 超链接
超链接有三种形式：
1 外部链接

    <a href="http://www.baidu.com" target="_blank">点我点我</a>

2 锚定链接
作用是在本页面或者其他页面的的不同位置进行跳转。 首先我们要创建一个锚点，也就是说，使用name属性或者id属性给那个特定的位置起个名字。

    <a id="name1"></a>

之后在底部设置超链接，点击时将回到锚点

    <a href="#name1"></a>

也可以在不同的页面中进行锚定

    <a href="b.html#name1"></a>

3 邮件链接

    <a href="mailto:smyhvae@163.com">点击进入我的邮箱</a>
超链接的属性：

 - href：目标URL
 - title：悬停文本。
 - name：主要用于设置一个锚点的名称。
 - target：告诉浏览器用什么方式来打开目标页面。target属性有以下几个值：
     - _self：在同一个网页中显示（默认值）
     - _blank：在新的窗口中打开。
     - _parent：在父窗口中显示
     - _top：在顶级窗口中显示

注意a是一个文本标签

##### 图片标签
`<img>`代表的就是一张图片。是单边标签。
src属性：指图片的路径。
1 相对路径

    <img src="..\2.jpg">

2 绝对路径
绝对路径可以是本地路径和网络路径

    <img src="C:\Users\smyhvae\Desktop\html\images\1.jpg">
    <img src="http://img.smyhvae.com/2016040102.jpg">
总结：

 - 我们现在无论是在a标签、img标签，如果要用路径。只有两种路径能用，就是相对路径和绝对路径。
 - 相对路径，就是../ image/ 这种路径。从自己出发，找到别人；
 - 绝对路径，就是http://开头的路径。
 - 绝对不允许使用file://开头的东西，这个是完全错误的！

img的其他属性：

 - width：宽度
 - height：高度
 - Align：指图片的水平对齐方式，属性值可以是：left、center、right
 - title：提示性文本。公有属性。也就是鼠标悬停时出现的文本。
 - border：给图片加边框（描边），单位是像素，边框的颜色是黑色
 - Hspace：指图片左右的边距
 - Vspace：指图片上下的边距
 - Alt：当图片显示不出来的时候，代替图片显示的内容。alt是英语 alternate “替代”的意思。
 
**注意事项**： （1）如果要想保证图片等比例缩放，请只设置width和height中其中一个。 （2）如果想实现图文混排的效果，请使用align属性，取值为left或right。
 

##### 列表标签

###### 无序列表

    <ul>
    	<li>默认1</li>
    	<li>默认2</li>
    	<li>默认3</li>
    </ul>

属性：
type="属性值"，属性值可以选： disc(实心原点，默认)，square(实心方点)，circle(空心圆)。 
列表也可以是嵌套的，如

    <ul>
    	<li><b>北京市</b>
    		<ul>
    			<li>海淀区</li>
    			<li>朝阳区</li>
    			<li>东城区</li>
    
    		</ul>
    	</li>
    
    	<li><b>广州市</b>
    		<ul>
    			<li>天河区</li>
    			<li>越秀区</li>
    		</ul>
    	</li>
      </ul>
ul的实际场景：
![场景1][15]
![场景2][16]
li是一个容器级标签，li里面什么都能放

###### 有序列表

    <ol >
    	<li>呵呵哒1</li>
    	<li>呵呵哒2</li>
    	<li>呵呵哒3</li>
    </ol>
    
属性：
type="属性值"，属性值可以是：1(阿拉伯数字，默认)、a、A、i、I。结合start属性表示从几开始。

    <ol type="i" start="4">
    	<li>哈哈</li>
    	<li>哈哈</li>
    	<li>哈哈</li>
    </ol>

有序列表同样可以嵌套

##### 定义列表
`<dl>`英文单词：definition list，没有属性。dl的子元素只能是dt和dd。

    <dl>
    	<dt>第一条</dt>
    	<dd>你若是觉得你有实力和我玩，良辰不介意奉陪到底</dd>
    	<dd>我会让你明白，我从不说空话</dd>
    	<dd>我是本地的，我有一百种方式让你呆不下去；而你，无可奈何</dd>
    	<dt>第二条</dt>
    	<dd>良辰最喜欢对那些自认能力出众的人出手</dd>
    	<dd>你可以继续我行我素，不过，你的日子不会很舒心</dd>
    	<dd>你只要记住，我叫叶良辰</dd>
    	<dd>不介意陪你玩玩</dd>
    	<dd>良辰必有重谢</dd>
    </dl>

定义列表表达的语义是两层：

 - （1）是一个列表，列出了几个dd项目
 - （2）每一个词儿都有自己的描述项。

备注：dd是描述dt的。
案例：
![dl案例][17]
dt、dd都是容器级标签，想放什么都可以。

#### 表格标签
一个表格`<table>`是由每行`<tr>`组成的，每行是由每个单元格`<td>`组成的。

    <table>
    		<tr>
    			<td></td>
    			<td></td>
    			<td></td>
    			<td></td>
    		</tr>
    </table>

表格的属性

 - border:边框，像素为单位。
 - style="border-collapse:collapse;"：单元格的线和表格的边框线合并（表格的两边框合并为一条）
 - width：宽度。像素为单位。
 - height：高度。像素为单位。
 - bordercolor：表格的边框颜色。
 - align：表格的水平对齐方式。属性值可以填：left right center。 注意：这里不是设置表格里内容的对齐方式，如果想设置内容的对齐方式，要对单元格标签<td>进行设置）
 - cellpadding：单元格内容到边的距离，像素为单位。默认情况下，文字是紧挨着左边那条线的，即默认情况下的值为0。 注意不是单元格内容到四条边的距离哈，而是到一条边的距离，默认是与左边那条线的距离。如果设置属性dir="rtl"，那就指的是内容到右边那条线的距离。
 - cellspacing：单元格和单元格之间的距离（外边距），像素为单位。默认情况下的值为0
 - bgcolor="#99cc66"：表格的背景颜色。
 - background="路径src/..."：背景图片。 背景图片的优先级大于背景颜色。
 - bordercolorlight：表格的上、左边框，以及单元格的右、下边框的颜色
 - bordercolordark：表格的右、下边框，以及单元格的上、左的边框的颜色 这两个属性的目的是为了设置3D的效果。
 - dir：公有属性，单元格内容的排列方式(direction)。 可以 取值：ltr：从左到右（left to right，默认），rtl：从右到左（right to left） 既然说dir是共有属性，如果把这个属性放在任意标签中，那表明这个标签的位置可能会从右开始排列。

`<tr>`:行
行属性：

 - dir：公有属性，设置这一行单元格内容的排列方式。可以取值：ltr：从左到右（left to right，默认），rtl：从右到左（right to left）
 - bgcolor：设置这一行的单元格的背景色。 注：没有background属性，即：无法设置这一行的背景图片，如果非要设置，可以用css实现。
 - height：一行的高度
 - align="center"：一行的内容水平居中显示，取值：left、center、right
 - valign="center"：一行的内容垂直居中，取值：top、middle、bottom

**单元格合并**
如果要将两个单元格合并，那肯定就要删掉一个单元格。 单元格的属性： - `colspan`：横向合并。例如`colspan="2"`表示当前单元格在水平方向上要占据两个单元格的位置。 - `rowspan`：纵向合并。例如`rowspan="2"`表示当前单元格在垂直方向上要占据两个单元格的位置。 


`<th>`：加粗的单元格。相当于`<td>`+`<b>`
表格标题：
使用时和`tr`标签并列 - 属性：`align`，表示标题相对于表格的位置。属性取值可以是：left、center、right、top、bottom 

**表格的`<thead>`标签、`<tbody>`标签、`<tfoot>`标签**

这三个标签有与没有的区别：

 1. 如果写了，那么这三个部分的代码顺序可以任意，浏览器显示的时候还是按照thead、tbody、tfoot的顺序依次来显示内容。如果不写thead、tbody、tfoot，那么浏览器解析并显示表格内容的时候是从按照代码的从上到下的顺序来显示。
 2. 当表格非常大内容非常多的时候，如果用thead、tbody、tfoot标签的话，那么数据可以边获取边显示。如果不写，则必须等表格的内容全部从服务器获取完成才能显示出来。

#### 框架标签
`<frame>`框架:一个框架显示一个页面
属性：

 - scrolling="no"：是否需要滚动条。默认值是true。
 - noresize：不可以改变框架大小。默认情况下，单个框架的边界是可以拖动的，这样的话，框架大小就不固定了。如果用了这个属性值，框架大小将固定。`<frame src="top.html" noresize></frame>`
 - bordercolor="#00FF00"：给框架的边框定义颜色。这个属性在框架集合<frameset>中同样适用。
 - frameborder="0"或frameborder="1"：隐藏或显示边框（框架线）。
 - name：给框架起一个名字。 利用name这个属性，我们可以在框架里进行超链。例如：![此处输入图片的描述][18]效果：![此处输入图片的描述][19]

`<iframe>`内嵌框架
内嵌框架inner frame：嵌入在一个页面上的框架,效果![此处输入图片的描述][20]
属性：

 - src="subframe/the_second.html"：内嵌的那个页面
 - width=800：宽度
 - height=“150：高度
 - scrolling="no"：是否需要滚动条。默认值是true。
 - name="mainFrame"：窗口名称。公有属性。

`<frameset>`框架集合：一个框架集合可以包括多个框架或框架的集合。
属性：

 - row:水平分割，将框架分为上下部分。写法有两种： 1、绝对值写法：rows="200,*" 其中*代表剩余的。这里其实包含了两个框架：上面的框架占200个像素，下面的框架占剩下的部分。 2、相对值写法：rows="30%,*" 其中*代表剩余的。这里其实包含了两个框架：上面的框架占30%，下面的框架占70%。 注：如果你想将框架分成很多行，在属性值里用逗号隔开就行了。
 - cols:垂直分割，将框架分为左右部分。写法有两种： 1、绝对值写法：cols="200,*" 其中*代表剩余的。这里其实包含了两个框架：左边的框架占200个像素，右边的框架占剩下的部分。 2、相对值写法：cols="30%,*" 其中*代表剩余的。这里其实包含了两个框架：左边的框架占30%，右边的框架占70%。 注：如果你想将框架分成很多列，在属性值里用逗号隔开就行了。

![框架][21]

#### 表单标签
表单标签用`<form>`表示，用于与服务器的交互。表单就是收集用户信息的，就是让用户填写的、选择的。

属性：

 - name：表单的名称，用于JS来操作或控制表单时使用；
 - id：表单的名称，用于JS来操作或控制表单时使用；
 - action：指定表单数据的处理程序，一般是PHP，如：action=“login.php”
 - method：表单数据的提交方式，一般取值：get(默认)和post

**get提交和post提交的区别**：
GET方式： 将表单数据，以"name=value"形式追加到action指定的处理程序的后面，两者间用"?"隔开，每一个表单的"name=value"间用"&"号隔开。 特点：只适合提交少量信息，并且不太安全(不要提交敏感数据)、提交的数据类型只限于ASCII字符。
POST方式： 将表单数据直接发送(隐藏)到action指定的处理程序。POST发送的数据不可见。Action指定的处理程序可以获取到表单数据。 特点：可以提交海量信息，相对来说安全一些，提交的数据格式是多样的(Word、Excel、rar、img)。
 
##### 输入标签

    <input type="text" />

属性：

 - type="属性"：属性值可以是
     - text
     - passowrd:密码类型
     - radio:单选按钮，名字相同的按钮作为一组进行单选（单选按钮，天生是不能互斥的，如果想互斥，必须要有相同的name属性。name就是“名字”。 ）。非常像以前的收音机，按下去一个按钮，其他的就抬起来了。所以叫做radio。
     - checkbox:多选按钮，名字相同的作为一组进行选择
     - checked:将单选按钮或多选按钮默认处于选中状态。当<input>标签的type="radio"时，可以用这个属性。属性值也是checked，可以省略。
     - hidden:隐藏框，在表单中包含不希望用户看见的信息
     - button:按钮
     - submit:提交按钮，传送当前表单的数据给服务器或其他程序处理。这个按钮不需要写value自动就会有“提交”文字。这个按钮真的有提交功能。点击按钮后，这个表单就会被提交到form标签的action属性中指定的那个页面中去。
     - reset:重置按钮，清空当前表单的内容，并设置为最初的默认值
     - image:图片按钮，和提交按钮的功能完全一致，只不过图片按钮可以显示图片。
     - file:文件选择框。
 - value="内容"：文本框里的默认内容（已经被填好了的）
 - size="50"：表示文本框内可以显示五十个字符。一个英文或一个中文都算一个字符。
 - readonly：文本框只读，不能编辑。因为它的属性值也是readonly，所以属性值可以不写
 - disabled：文本框只读，不能编辑，光标点不进去。属性值可以不写。

举例：

    <form>
    	姓名：<input value="呵呵" >逗比<br>
    	昵称：<input value="哈哈" readonly=""><br>
    	名字：<input type="text" value="name" disabled=""><br>
    	密码：<input type="password" value="pwd" size="50"><br>
    	性别：<input type="radio" name="gender" value="male" checked="">男
    		  <input type="radio" name="gender" value="female" >女<br>
    	爱好：<input type="checkbox" name="love" value="eat">吃饭
    		  <input type="checkbox" name="love" value="sleep">睡觉
    		  <input type="checkbox" name="love" value="bat">打豆豆
    </form>

##### 下拉列表
`<select>`标签里面的每一项用`<option>`表示。select就是“选择”，option“选项”。

select标签的属性：

 - multiple：可以对下拉列表中的选项进行多选。没有属性值。
 - size="3"：如果属性值大于1，则列表为滚动视图。默认属性值为1，即下拉视图。

option标签的属性：

 - selected：预选中。没有属性值。

##### 多行文本输入框
`<textare>`就是文本多行区域
属性：

 - value：提交给服务器的值。
 - rows="4"：指定文本区域的行数
 - cols="20"：指定文本区域的列数
 - readonly：只读

##### 表单语义化
比如我们要对表单进行分组

    <form>
    	<fieldset>
    	<legend>账号信息</legend>
    	姓名：<input value="呵呵" >逗比<br>
    	密码：<input type="password" value="pwd" size="50"><br>
    	</fieldset>
    	<fieldset>
    	<legend>其他信息</legend>
    	性别：<input type="radio" name="gender" value="male" checked="">男
    		  <input type="radio" name="gender" value="female" >女<br>
    	爱好：<input type="checkbox" name="love" value="eat">吃饭
    		  <input type="checkbox" name="love" value="sleep">睡觉
    		  <input type="checkbox" name="love" value="bat">打豆豆
    	</fieldset>
    </form>

##### label标签
通过label可以把input和汉字包裹起来作为整体。

    <input type="radio" name="sex" id="nan" /> <label for="nan">男</label>
    <input type="radio" name="sex" id="nv"  /> <label for="nv">女</label>
    
input元素要有一个id，然后label标签有一个for属性，和id相同，那么这个label和input就有绑定关系了。


#### 多媒体标签
略



### CSS篇



### Javacsript篇
前端工程化 
#### 浏览器内核
Chrome：Webkit(v8引擎)
firefox：Gecko
Opera：Presto
IE：Trident
**浏览器内核**：
浏览器内核就是识别页面代码并绘制页面的东西称为内核或者渲染引擎。
**浏览器兼容性**：
由于各个浏览器对W3C规范实现程度不同，或者各个浏览器有自己的特殊实现，会导致同样的代码在不同的浏览器上有不同的效果，也就是浏览器兼容性问题。

#### 导入js的三种方式
1、 内嵌导入

```html
<script>
    ....
</script>
```

2、外链式

```html
<script src="/path/to/your/js"></script>
    
```
3、行内导入(不推荐)
```html
<div onclick="your code"></div>
```
**注意内嵌导入和外链导入不能混合使用，如果混合使用了，只有内嵌代码块不会执行**

通常把script标签放在body的末尾，这样js会在其他东西加载完成了之后在进行加载，但不是必须的，也可以把script标签放在别的地方，通过一些方式可以设置其在最后进行加载：
a. window.onload()=function(){};
b. $(document).ready(function(){})

#### js中的输出
1、alert

    alert("hello")

2、confirm

    confirm("are you ok!")

3、prompt

    prompt("are you sure?")

#### 控制台输出
方便开发人员输出调试
右键-->检查 或者F12

    console.info()
    console.dir()
    console.table()

![console][22]

#### js组成
ECMAScript：包含了js的基础语法(变量、数据类型、语法规范、操作语句)，ES3/5, ES6/7
DOM(文档对象模型):属性和方法，可以方便我们操作页面中的元素
BOM：浏览器对象模型，提供了属性和方法，可以方便我们操作浏览器

#### 常量/变量/数据类型

```javascript
//var varName = varValue;
var num = 12;
var str = 'hello';
var b = true;
//ES6中使用let
let a = 12;
let b = false;
let c = 'abcd';

//常量 const A = VA
const PI = 3.14;
PI = 3.1415 //错误，不能重新赋值
```

变量命名规范：
>1 JS中严格区分大小写、
>2 可以使用$,_,数字,字母，但数字不能开头
>3 不能使用关键字和保留字来命名
>4 一般遵循驼峰命名法
>>对于变量，由几个单词的组合而成，首单词首字母小写，剩余的单词首字母大写

js中的数据类型有：
```js
//基本数据类型
//数字类型
var n = 12;
var m = 12.34;
//字符串
var s = 'hello';
var ss = "hello";
//布尔类型
var a = true;
var b = false;
//null
var n = null;
//undefined
var u = undefined;
//引用数据类型
//object类型
var o = {};
var a = [];
//function类型
var f = function(){};

//判断数据类型
var a;
typeof a;//返回的结果是字符串
//typeof null返回的是object，此外，对object，typeof也无法给出更详细的结果
//instanceof(a);
//constructor(a);
//Object.prototype.toString.call()
```

布尔类型：
```js
//工厂函数
var t = Boolean(1);
var t = Boolean('hello');
//0，NaN， '', null, undefined这几个转化为boolean类型时为false,其余的均为true
```
字符串类型
```js
//在js中，单引号和双引号括起来的均是字符串
var s = 'hello';
var ss = "Hello";
//常用方法
//charAt charCodeAt
//substr substring slice
//toUpperCase toLowerCase
//indexOf lastIndexOf
//split
//replace
//match
```

数字类型
```js
//NaN
typeof NaN // ‘number’
NaN == NaN // false,注意NaN和任意值都不相同
var a = 0;
var s = '12';
var n = NaN;
isNaN(a) //false
isNaN(n) //true
isNaN(s) //false,这里s会转化为number类型，所以是false
Number() //数字类型工厂函数
var a = Number('23');
var b = Number('12s'); //NaN,出现了非有效数字，转换为NaN
var t = Number(true); // 1
var f = Number(false); // 0
var n = Number(null); // 0
var u = Number(undefined); // NaN
var a = Number([]); //0， 引用数据类型会先转化为string，在由string转化为Number,isNaN判断引用类型的转换过程相同
var aa = Number([12]); //12
var aaa = Number([12,11]); //NaN

//parseInt,与Number的区别在于处理字符串
parseInt('12px');//12
parseInt('12px13');//12, 第一个非有效字符后面的被丢弃
parseInt('ox12');//NaN
parseInt('12.7px');//12

//parseFloat, 在parseInt的基础上可以识别小数点
parseFloat('12.5px');//12.5

//拓展
/*
parseInt还可以接受两个参数
parseInt(string, radix)
radix	
可选。表示要解析的数字的基数。该值介于 2 ~ 36 之间。

如果省略该参数或其值为 0，则数字将以 10 为基础来解析。如果它以 “0x” 或 “0X” 开头，将以 16 为基数。

如果该参数小于 2 或者大于 36，则 parseInt() 将返回 NaN。
/*
```

`null`和`undefined`的区别

 - null表示赋值为一个空对象
 - undefined表示没有进行对象赋值

引用数据类型
由大括号包起来，以key:value的形式定义属性和值，属性可以有多个：

    {
      key1:value1,
      key2:value2,
    {
    属性描述这个对象的特点特征
    
```js
var obj = {
            name: 'sjl',
            age: 18,
            best-friend: '习近平'，
            0: 0//这样也是可以的
        }
alert(obj.name);
alert(obj['name']);
alert(obj['best-friend']);//只能通过中括号的方式获取
alert(obj[0]);//只能通过中括号获取

obj.name = 'song';
obj.sex = 'male';

delete obj[0];//删除属性
```
基本数据类型和引用数据类型的区别

 - 基本数据类型是按值操作
 - 引用数据类型是按照引用地址来操作(变量中保存的是一个引用地址)


函数类型
函数类型是一种引用数据类型

    function 函数名() {
        //函数体
    }
    函数名() //调用
    函数执行时浏览器创建一个供函数执行的私有环境，称为私有作用域
    函数可以定义多个形参，可以理解为函数的入口：
    function 函数名(arg1, arg2, ...) {
        //函数中定义的为形参
    }
    函数名(v1, v2, ...)//实际传入的值为实参


#### 控制结构
##### If

    单条件判断
    if(条件表达式){
        //如果条件表达式成立，便执行
    }
    双条件判断
    if(条件表达式){
        //如果条件表达式成立，便执行
    }else{
        //如果条件表达式不成立，便执行
    }
    多条件判断
    if (condition) {
        //如果条件表达式1成立，便执行
    } else if (condition) {
        //如果条件表达式2成立，便执行
    } else {
        //如果条件表达式都不成立，便执行
    }
    
    
条件表达式
 - ==, !=, ===(**===会先进行类型转换，再比较**)
 - >, >=
 - <, <=
 - 单变量，先把变量转化为bool类型,再判断
 - && 条件与
 - || 条件或
 - ! 条件取反

```js
var num = parseFloat('width:12.5px');//NaN
if (num == 12.5) {
    alert(12.5);
} else if(num==NaN) {
    alert(NaN);
} else if(typeof num == 'number') {
    alert(0);
} else {
    alert('其余都不是');
}
//alert 0
```

三元运算符

    //条件成立a = value1,不成立a = value2
    var a = (条件) ? value1 : value2

##### switch 
适用于一些离散值的判断

    var n;
    switch (n) {
        case v1://值取v1时
            
            break;//防止出现条件穿透
        case v2://值取v2时
            
            break;
        case v3://值取v3时
            
            break;
        default://取其他值时，防止出现一些意外情况
            break;//这个可以不加
    }

注意：

 - switch中比较使用的是===

==和===的区别：

 - ==比较时，如果两边值类型不一样，浏览器会默认转换为一样的类型再比较
 - ===,如果两边的类型不一样，直接返回false

##### For
循环的三种格式：

    for (let index = 0; index < array.length; index++) {
        const element = array[index];
        //。。。
    }
    注意：初始条件声明也可以用var，但var存在变量提升的问题，在循环结束后，循环变量仍然可以操作，这可能出现一些问题，let可以避免这种情况。
    
    for (const key in object) {
        if (object.hasOwnProperty(key)) {
            const element = object[key];
            
        }
    }
    
    for (const iterator of object) {
        
    }

continue和break

 - continue：结束本轮循环，开始下一次
 - break：结束整个循环

```js
for (var i = 0; i < 10; i++) {
    if(i<5){
        i++;
        continue;
    }else{
        i+=3;
        break;
    }
}
```
 
举例（li隔行变色）：
```js
//css隔行变色
var box = document.getElementById('box');
var list = box.getElementsByTagName('li');

for (let i = 0; i < list.length; i++) {
    if(i%2==0){
        list[i].backgroundColor='#EEE';
    }
    
}
```
举例（选项卡）：
```javascript
var tabBox = document.getElementById('tabbox');
var oList = tabBox.getElementsByTagName("li");
var oDivList = tabBox.getElementsByTagName("div");

for (var i = 0; i < oList.length; i++) {
    //这里只是执行了函数绑定，函数并没有真正执行，i也没有真正赋值
    //oList[i].onclick = function () {
        //change(i);
    //}
    //ES6中可以将循环变量的定义由var改为let可克服该问题
    oList[i].myIndex = i;
    oList[i].onclick = function () {
        change(this.myIndex);
    }
}

function change(index) {
    //清除样式
    for (var i = 0; i < oList.length; i++) {
        oList[i].className = '';
        oDivList[i].className = ''
        
    }

    oList[i].className = 'select';
    oDivList[i].className = 'select';
}
```
 
##### Forin
forin主要用来遍历对象键值对

    for(var key in obj) {
        //通常还要加上hasOwnProperty判断
        ......
    }

 
 #### 数据类型转换
 1、其他数据类型-->number类型
 > + isNaN,Number,parseInt,parseFloat
 > + 在进行加减乘除数学运算的时候
 > + true->1 false->0
 > + ''->0, 'abc'->NaN
 > + null->0
 > + undefined->0
 > + 引用类型先转化为string,再由string转化为字符串
 
 
 2、其他类型转化为字符串
 > + 调用toString方法
 > + `+`进行字符串拼接时
 > + 基本数据类型转化为字符串时直接将字面值转化为字符串
 > + 引用数据类型转化为字符串时调用toString方法，需要根据toString方法来确定

 
 3、其他数据类型转化为布尔类型
 > + Boolean,!,!!,条件表达式中会转化为布尔类型
 > + 0,'',NaN, null,undefined转化为false，其余的转化为true
 > + 引用类型进行`==`判断时，判断的是引用数据的内存地址，只有是同一个对象是才相等
 > + 其他类型比较时两边先转化为数字再比较(例外，null==undefined为true，null,unfined和其他任何值都不相等)
 > + NaN和任何类型都不相等，包括自身
 
#### 常用类库和方法
##### Math
1、abs
取绝对值
```javascript
Math.abs(12);
Math.abs(-12.9);
```
2、ceil/floor
ceil向上取整
floor向下取整
```javascript
Math.ceil(12.6);//13
Math.floor(12.9);//12
```
3、round
四舍五入
```javascript
Math.round(12.6);//13
Math.round(12.2);//12
```
4、random
0到1的随机数
```javascript
Math.random();
```
5、max/min
```javascript
Math.max(12,6,8);
Math.max(1,2,12,5);
Math.min(12,6,8);
Math.min(1,2,12,5);
```
6、pow/sqrt
幂运算/开方运算
```javascript
Math.pow(2,4);//2^4
Math.pow(3,3);//3^3
Math.sqrt(4);
Math.sqrt(9);
```
##### string
如果字符串指定的索引不存在，结果为undefined。查看字符串的方法：console.dir(String.prototype)
```javascript
// charAt
var s = 'hello';
s.charAt(0); // 'h'
s.charAt(10); // ''

//charCodeAt 返回该字符对应的ascii码值
s.charCodeAt(0);// 104

//fromCharCode 返回ascii码值对应的字符
String.fromCharCode(104);//'w'

//substr 实现字符串截取
s.substr(1,3);//'ell'

//substring
s.substring(1,3);//'el'

//slice 支持负数索引
s.slice(-3,-1);//'ll'

// toUpperCase 
s.toUpperCase();//HELLO
// toLowerCase
s.toLowerCase();//hello

// indesOf
s.indexOf('l'); //2
// lastIndexOf
s.lastIndexOf('l'); //3

//split, 分割，支持正则表达式
s.split('')'// ['h','e','l','l','o']

// replace 实现替换
s.replace('ll','LL');//heLLo

//trim
var s = '  hello   ';
s.trim();//'hello'

//trimLeft
s.trimLeft();///'hello   '

//trimRight
s.trimRight();//'  hello'

```

案例：验证码
```javascript
var codeBox = document.getElementById('codeBox');

var areaStr = '0123456789qwertyuiopasdfghjklzxcvbnm';

var result = '';
for(var i = 0; i<4; i++){
    var ran = Math.raound(Math.random()*61);
    var char = areaStr.charAt(ran);
    result += char;
}
codeBox.innerHTML = result;
```
#### DOM
DOM: Document object model 文档对象模型，提供一些属性和方法以方便我们操作DOM元素。

##### 获取dom元素
`document.getElementId`:根据id获取一个元素
`[context].getElementsByTagName`:根据标签名获取元素集合
`[context].getElementsByClassName`:根据样式类名获取元素集合
`document.getElementsByName`:根据name属性获取节点集合
`document.documentElement`:获取整个HTML对象
`document.body`:获取整个body对象
`document.head`:获取整个head对象
`[context].querySelector`:根据选择器获取一个元素对象
`[context].querySelectorAll`:获取元素集合
```html
<!--getElementById 此方法的上下文只能是document-->
<div id="box1"></div>
<script>
    //如果有多个相同id，但是只能获取到一个，在IE7及更低版本中会把name属性当做id使用，所以需要考虑兼容性
    var box = document.getElementById('box1');
    //获取某个id的所有属性
    //先获取所有的节点，再遍历查找某个id的节点
    var all = document.getElementsByTagName('*');
</script>

<!-- getElementsByTagName 
获取的结果是元素集合
-->
<div>2<div>
<div>1<div>
<script>
    var boxes = document.getElementsByTagName('div');
</script>

<!-- getElementsByClassName
获取的结果是特定样式的元素集合，注意在IE6-8中该方法不兼容
-->

<!-- getElementsByName
获取的结果是特定name的节点集合(NodeList)，上下文只能是document，注意IE浏览器只能识别表单元素的name属性，所以该方法一般用于操作表单元素
-->


<!-- document.documentElement/document.body 获取HTML/body-->
<script>
    // 获取当前浏览器窗口的可视区域的宽度
    document.documentElement.clientWidth;
    // or
    document.body.clientWidth
</script>


<!-- querySelector/querySelectorAll 
在IE下不兼容，使用较少，一般常用于移动端, 支持大部分的css选择器
-->
<div id="box1" class="big black"><div>
<div id="box2" class="medium blue"><div>
<div id="box3" class="small black"><div>
<script>
    var box = document.querySelector('#box1');
    var boxes = document.querySelectorAll('.black');
</script>

```

#####DOM中的节点
节点(node): html中的所有内容都是节点，包括标签，注释，文本，是用来描述页面中每一部分之间的关系的

 - 元素节点：HTML标签
 - 文本节点：文字内容
 - 注释节点：注释内容
 - document文档节点：document

```html
<div id="box">
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
    <div></div>
    <div></div>
    <div></div>
</div>
<script>
    //元素节点：nodeType为1，nodeName是大写的标签名(部分浏览器下为小写),nodeValue为null
    //文本节点：nodeType为3，nodeName为#text，nodeValue为文本内容
    //注释节点：nodeType为8，nodeName为#comment，nodeValue为注释内容
    //文档节点：nodeType为9，nodeName为#document，nodeValue为null
</script>
```
#####DOM节点操作
节点之间的关系：

 - `childNodes`: 当前节点的所有的子节点(包括元素、文本、注释等节点)
 - `children`:当前节点的所有的元素子节点(IE中会将注释节点当元素节点)
 - `parentNode`:当前元素的父节点(元素对象)
 - `previousSibling`:当前节点的上一个哥哥节点(不一定是元素节点)
 - `nextSibling`:当前节点的下一个弟弟节点(不一定是元素节点)
 - `previousElementSibling`:当前节点的上一个哥哥元素节点
 - `nextElementSibling`:当前节点的下一个弟弟元素节点
 - `firstChild`:当前元素的第一个子节点
 - `lastChild`:当前元素的最后一个子节点
 - `firstElementChild`:当前元素的第一个子元素节点
 - `lastElementChild`:当前元素的最后一个子元素节点

DOM节点的操作：

 - `document.createElement()`:创建一个HTML标签(只是在JS中创建，还没有放在页面中)
 - `appendChild(元素对象)`:将当前新元素添加到容器的末尾
 - `insertBefore(新元素,老元素)`:在当前容器中将新元素增加到老元素之前
 - `removeChild(元素)`:在当前容器中把某一元素移除掉
 - `replaceChild(新元素,老元素)`:在当前容器中将老元素替换为新元素
 - `cloneNode(true/false)`:把元素克隆一份一模一样的，false：只克隆当前元素本身，true：深度克隆，把当前元素本身及元素后代都进行克隆
 - `[set/get/remove]Attribute`:给当前元素设置/获取/移除属性
 - 
> 使用xxx.index = 0和xxx.setAttribute('index', 0)这两种自定义属性的区别，前者为把当前操作的元素当做一个普通对象,为其设置一个属性名，和页面中的HTML标签没关系，后者则是把元素当做特殊对象来处理，设置的自定义属性和页面结构的DOM元素映射在一起
> JS 中获取的元素对象，我们可以把它理解为两种角色：1. 与页面HTML结构无关的普通对象 2. 与页面HTML结构存在映射关系的元素对象
> 元素对象中的内置属性，大部分都和页面标签存在映射关系，例如，xxx.style.backgroundColor='xxx'，此时也会映射到页面的HTML标签上(元素样式会发生改变)
> 元素对象中的自定义属性：xxx.index=0，这种仅仅是把JS对象中增加了一个属性名，和页面中的HTML结构没有关系
> xxx.setAttribute:通过这种方式设置的自定义属性和上面的内置属性差不多，都和HTML结构存在映射关系(设置的自定义属性可以呈现在结构上)

```javascript
var div = document.getElementById('box1');
var oDiv = document.createElement('div');
oDiv.id = 'div1';
oDiv.className = 'box';

document.body.appendChild(oDiv);
//document.body.insertBefore(oDiv, div);

```

```javascript
function queryURLParameter(url) {
  var link = document.createElement('a');
  link.href = url;
  
  var serarch = link.search;
  var obj = {};
  if(serarch.length === 0) return;
  search = serarch.substr(1).split(/(&|=)/g);
  for(var i = 0; i < serarch.length; i+=2){
    var key = search[i];
    var value = search[i+1];
    obj[key]=value;
  }
  link = null;
  return obj;
  
}
```

案例：获取上一个哥哥元素节点(兼容浏览器)
```javascript
//jquery中的实现原理
function prev(curEle) {
    var previous = curEle.previousSlibling;
    while(p && p.nodeType != 1){
        p = p.previousSibling;
    }
    return p;
}
```

#### Date
日期操作
```javascript
//获取当前客户端本机时间
var date=new Date();
//获取四位整数年
date.getFullYear()
//获取月份，从0开始
date.getMonth()
//获取日
date.getDate()
//获取星期，0-6
date.getDay()
//获取小时
date.getHours()
//获取分钟
date.getMinutes()
//获取秒
date.getSeconds()
//获取毫秒
date.getMilliseconds()
//获取当前时间距离1970-1-1的毫秒数
date.getTime()
//设置当前时间距离1970-1-1的毫秒数
date.setTime(num)
```

```javascript
//将字符串转化为时间
var date = new Date('2018-01-01');

//传递毫秒数 
var date = new Date(1238128934);
```

案例：倒计时
```javascript
var timeBox = document.getElementById('timeBox');
function computed() {
    var date = new Date();
    var targetDate = new ('2018-01-01 12:00:00');
    var spanTime = targetDate - date;//两个时间的毫秒差
    if(spanTime <= 0) {
        timeBox.innerHTML = '开始';
        clearInterval(timer);
        return;
    }
    var hour = Math.floor(spanTime / (1000 * 60 * 60));
    hour = (hour < 10) ? '0' + hour : hour;
    spanTime -= hour * 60 * 60 * 1000;
     var minute = Math.floor(spanTime / (1000 * 60));
     minute = (minute < 10) ? '0' + minute : minute;
     spanTime -= minute * 60 * 1000;
     var second = Math.floor(spanTime / 1000);
     second = (second < 10) ? '0' + second : second;
     timeBox.innerHTML = hour + ':' + minute + ':' + second;
     
}
var timer = setInterval(computed, 1000);
```
#### 数组
##### 数组循环

    for(var i = 0; i < array.length; i++){
        //array[i]
    }

    for(var key in array){
        //array[key]
    }

**for循环只能遍历到数组私有的一些属性，而forin循环可以遍历到定义的公共属性**
##### 常用方法
1、push/unshift
```javascript
var array = [1,2,3,4,5,6];
//push：向数组末尾追加新内容
array.push(7);
array.push(8);
//unshift：向数组开头追加新内容
array.unshift(0);
array.unshift(-1);
```
2、pop/shift
```javascript
var array = [1,2,3,4,5,6];
//pop：删除数组最后一项
array.pop();
array.pop();
//shift：删除数组第一项
array.shift();
array.shift();
```
** 注意：用delete删除指定数组元素，会直接把索引删除且length属性不会变，不推荐使用，使用上述方法删除元素后会重排索引 **
3、splice
```javascript
var array = [1,2,3,4,5,6,7,8];
//删除
//从索引n开始删除m个,m不写删除到末尾,n为0表示清空数组
//array.splice(n, m);
array.splice(3, 2);
//修改
//在原有删除的基础上，用x代替删除的内容，
//splice(n, m, x)
//在修改的基础上，把x插入到索引n的前面
//splice(n, 0, x)
//向数组开头追加新的内容
//array.splice(0,0,x)
array.splice(1,2, 12)
```
4、slice
```javascript
var array = [2,3,4,5,6,7,8];
//从索引n开始找到索引m处，不包括m，如果m不提供，则查到末尾
//支持负数索引
//slice(n, m)

array.slice(2,6);
```
5、concat
```javascript
var array = [1,2,3,5,4,6,7,9,8];
//将多个数组进行拼接,将新数组返回，原数组不变
array.concat(['a','b','c','d']);

//concat()
//上面相当于把原有数组克隆一份
```
6、join
```javascript
//以指定的分隔符将数组元素拼接起来
var array = [1,2,3,4];
array.join('-');
```
7、toString
```javascript
//把数组转化为字符串
var array = [1,2,3,4,5,6,7];
array.toString();
```
8、sort/reverse
```javascript
var array = [1,2,3,4,5,6,7,8];
//将数组逆序排列
array.reverse();

//将数组按照字典序排序
array.sort();
//按照自定义方式进行排序，传递一个回调函数
// 回调函数返回值
// 1 元素1大于元素2
// 0 元素1等于元素2
// -1 元素1小于元素2
array.sort(function(a, b){
    return a - b;
});

```
9、indexOf/lastIndexOf
```javascript
var array = [1,2,3,4,5,6,7,8,9,0];
//当前元素中第一次出现的索引
array.indexOf(2);
//当前元素最后一次出现的索引
array.lastIndexOf(4);
//如果没有这一项，返回-1
```

10、forEach/map
```javascript
var array = [1,2,3,4,5,6,7];

//forEach:遍历数组中的每一项
array.forEach( 
    (value, index) => {
        //value就是遍历的数组的每一项，index就是遍历每一项的索引
    }
)
//map:在forEach的基础上，可以修改每一项的值,同时会将修改后的数组返回
array.map(
    item => {
        //
    }
)

//filter

//find

//reduce
```

##### 数组排序
1、冒泡排序
依次让数组中的当前项和后一项进行比较，如果当前项大于后一项则交换位置
```javascript
/**
 * bubbld: 冒泡排序
 * @parameter: [array] array  需要实现排序的数组
 * @return: [array] 排序后的数组
 */
function bubbleSort(array){
    // 冒泡排序
    // 外层控制的是比较的轮数
    for(var i = 0; i < array.length - 1; i++) {
        // 里层控制的是每一轮比较的次数
        for(var j = 0; j < array.length - i - 1; j++) {
            if(array[j] > array[j+1]) {
                var tmp = array[j];
                array[j] = array[j+1];
                array[j+1] = tmp;
            }
        }
    }
    return array;
}
```
2、快速排序
递归：自身调用自身
```javascript
//递归中一定要设置退出条件，否则容易出现死循环
function fn(num) {
    if(num<=0){
        return 0;
    } else {
        return num + fn(num-1);
    }
}
fn(10);
```

在原有数组中找到中间的一项，把剩余项中的每一个值和中间项进行比较，比中间项小的放左边，比中间项的放右边，对分出来的数组同样这样处理即可(类似于二叉树中的处理，大的放左边，小的放右边)
![此处输入图片的描述][23]

```javascript
function quickSort(array) {
    if(array.length <= 1){
        return array;
    }
    // 获取中间项的索引，在原有数组中删除中间项
    var middle = Math.ceil(array.lenth / 2);
    middleValue = array.splice(middle, 1);
    //用剩余数组中的每一项和中间项进行比较
    var left = [];
    var right = [];
    
    for(var i = 0; i < array.length; i++){
        if(array[i] < middleValue){
            left.push(array[i]);
        }else{
            right.push(array[i]);
        }
        
    }
    quickSort(left).concat(middleValue, quickSort(right));
}
quickSort([1,4,2,7,9,1,3,6]);

```

3、插入排序
原理如下：
![此处输入图片的描述][24]

```javascript
function(array) {
    // 先从数组中取出一个值
    var arraySort = [];
    arraySort.push(array[0]);
    
    // 依次处理数组剩余的元素
    for(var i = 1; i < array.length; i++) {
        var item = array[i];
        //将取出的元素和排序数组进行比较
        for(var j = arraySort.length - 1; j >= 0; j--){
            if(arraySort[j]<item){
                arraySort.splice(j+1, 0, item);
                break;
            }
            if(j === 0){
                //该元素比所有元素都小
                arraySort.unshift(item);
            }
        }
    }
    return arraySort;
}
```

#### 函数
一段在一起的、可以做一件事的程序，称为函数

    function funcName(parameters){
        //body
    }
    //调用
    funcName()

> 函数作为一种引用数据类型，也是按照引用地址来操作的。定义函数也就是在全局作用域中定义了一个变量名为funcName的数据，类型为函数类型，变量中实际存放的是指向函数的地址。

> 函数执行时浏览器会先为其开辟一个新的私有作用域，把函数中的代码放到私有作用域中，然后作为JS表达式从上到下执行(需要先经过形参赋值和变量提升)

> 函数执行完毕，需要判断是否进行作用域销毁

> 函数执行会形成一个私有的作用域，让里面的私有变量和外界互不影响(相互不干扰,外面的无法直接获取里面的变量值),此时我们可以理解为私有作用域把私有变量保护起来，我们把这种机制称之为“闭包”。


> `栈内存`：又称作用域，提供一个JS代码的执行环境
> `堆内存`：所有的引用数据类型，需要存储的内容都在堆内存中



##### 形参和实参

```javascript

function funcName(parameters){//这里定义的是形参

}
funcName(1,2,3,4);//这里传递了实参，是实际传进去的值

```
注意：

 - 定义了形参，但是执行的时候可以不传，此时默认实参的值是undefined
 - 传递的实参可以比形参多，多传的值不处理
 - 所有的形参存储在一个集合变量arguments中，当我们不知道会具体传递几个值时，无法设置形参的个数，此时就可以使用arguments，这是函数内置的变量，注意该变量不需要显式的写在函数定义中，不管是否定义了形参，arguments中均存储了所有的实参信息
 - arguments是一个类数组集合，以数字作为索引，从0开始，有length属性，存储的是当前集合的长度，也就是当前实参的个数，此外，还有一个属性callee，表示当前函数自身，而arguments.callee.caller则表示当前函数在哪执行的(宿主函数，全局作用域下为null)
 - 严格模式下，arguments，callee，caller等属性无法使用("use strict")

```javascript
function sum() {
    var total = null;
    for(var i = 0; i < arguments.length; i++){
        var item = arguments[i];
        item = Number(item);
        if(!isNaN(item)){
            total += item;
        }
        
    }
}

sum(1,2,3,4,5,6);

```
 
##### 












































































#####
 



 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 


  [1]: https://camo.githubusercontent.com/390d5a409361baafd47198f4cb8b81579b254bc3/687474703a2f2f696d672e736d79687661652e636f6d2f32303138303131385f313630302e706e67
  [2]: http://color-themes.com/
  [3]: https://camo.githubusercontent.com/1d740b2745037e0e35c670b452863a248f5b36c0/687474703a2f2f696d672e736d79687661652e636f6d2f32303138303131385f313633362e706e67
  [4]: https://camo.githubusercontent.com/8ff0a5c4d1bba832ea99a9d64f1c88ad8225aab4/687474703a2f2f696d672e736d79687661652e636f6d2f32303138303131385f313632372e706e67
  [5]: https://camo.githubusercontent.com/73f8ab52e211460041bc47f1f68dff84458a2954/687474703a2f2f696d672e736d79687661652e636f6d2f32303138303131385f313632382e706e67
  [6]: https://camo.githubusercontent.com/2ef16e662feb4095689963e5e4f2ad8a37d59c64/687474703a2f2f696d672e736d79687661652e636f6d2f32303138303131385f313634362e706e67
  [7]: https://camo.githubusercontent.com/35fc1ce1a02886da041dbb56c194aea79f1c6fba/687474703a2f2f696d672e736d79687661652e636f6d2f32303138303132345f313835362e706e67
  [8]: https://camo.githubusercontent.com/d04d2e69c687d8ce9922a30d441dc01d1112ddcd/687474703a2f2f696d672e736d79687661652e636f6d2f32303138303131385f313732302e706e67
  [9]: https://camo.githubusercontent.com/21100a84fc072faa752a4adb4f57b4eaa07bf55c/687474703a2f2f696d672e736d79687661652e636f6d2f32303138303131385f313731392e676966
  [10]: https://www.jianshu.com/p/246b844f4449
  [11]: https://icomoon.io/app/#/select.
  [12]: https://github.com/jawil/blog/issues/4
  [13]: https://camo.githubusercontent.com/de087fe8aa6b5bd48e355d5a3077374734bfa156/687474703a2f2f3773627937722e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f323031352d31302d30312d636e626c6f67735f68746d6c3136363434302d356237383062646336623830613566622e706e67
  [14]: https://camo.githubusercontent.com/56613e432307c4c4e5fba5f78746598612dc39ac/687474703a2f2f3773627937722e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f323031352d31302d30312d636e626c6f67735f68746d6c3136363434302d316463643261643665363335333535392e706e67
  [15]: https://camo.githubusercontent.com/5079b518161f744c0ea7595347ff9ff5679c1539/687474703a2f2f696d672e736d79687661652e636f6d2f32303137303730345f313731372e706e67
  [16]: https://camo.githubusercontent.com/903be8f3166b1ae5289c0d5b0a30e9e562e02b60/687474703a2f2f696d672e736d79687661652e636f6d2f32303137303730345f313731392e706e67
  [17]: https://camo.githubusercontent.com/56af4a4849587ebbefafa3e8d754aac8f0303dcf/687474703a2f2f696d672e736d79687661652e636f6d2f32303137303730345f313732372e706e67
  [18]: https://camo.githubusercontent.com/306032539413aca979e7efe49ff9dbf78b1434db/687474703a2f2f3773627937722e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f323031352d31302d30322d636e626c6f67735f68746d6c5f32382e706e67
  [19]: https://camo.githubusercontent.com/c8e0f61dec736ab3eabc32032b105d82c4e3fb66/687474703a2f2f3773627937722e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f323031352d31302d30322d636e626c6f67735f68746d6c5f676966332e676966
  [20]: https://camo.githubusercontent.com/88e2039769a98c6c7689bcb87f6d40229283503d/687474703a2f2f3773627937722e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f323031352d31302d30322d636e626c6f67735f68746d6c5f32392e706e67
  [21]: https://camo.githubusercontent.com/e9c847955aa9409eae0226b85aee9b759843b7be/687474703a2f2f3773627937722e636f6d312e7a302e676c622e636c6f7564646e2e636f6d2f323031352d31302d30322d636e626c6f67735f68746d6c5f32362e706e67
  [22]: http://chuantu.biz/t6/342/1531493797x-1404817455.png
  [23]: http://chuantu.biz/t6/350/1532870663x-1376440198.png
  [24]: http://chuantu.biz/t6/350/1532872267x1822611227.png