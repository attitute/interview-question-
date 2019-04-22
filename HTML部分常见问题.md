# 一、HTML部分常见问题

## 1、怎么让一个不定宽高的 DIV，垂直水平居中

答：1）**使用** **CSS** **方法：**

父盒子设置：display：table-cell； text-align：center；vertical-align：middle；

Div 设置：    display：inline-block；vertical-align：middl；

2）**使用** **CSS3transform**：

父盒子设置：display：relative

Div 设置：  transform： translate(-50%，-50%)；position： absolute；top： 50%；left： 50%；

## 2.  position几个属性的作用？

答：position的常见四个属性值： relative，absolute，fixed，static。一般都要配合"left"、"top"、"right"以及 "bottom"

属性使用。

1）Static：默认位置，设置为 static 的元素，它始终会处于页面流给予的位置（static 元素会忽略任何 top、bottom、left 或 right 声明）。一般不常用。

2）Relative：位置被设置为 relative 的元素，可将其移至相对于其正常位置的地方，意思就是如果设置了 relative 值，那么，它偏移的 top，right，bottom，left 的值都以它原来的位置为基准偏移，而不管其他元素会怎么样。注意 relative 移动后的元素在原来的位置仍占据空间。

3）Absolute：位置设置为 absolute 的元素，可定位于相对于包含它的元素的指定坐标。意思就是如果它的

父容器设置了 position 属性，并且 position 的属性值为 absolute  或者 relative，那么就会依据父容器进行偏移。如

果其父容器没有设置 position 属性，那么偏移是以 body 为依据。注意设置 absolute 属性的元素在标准流中不占位

置。

4）Fixed：位置被设置为 fixed 的元素，可定位于相对于浏览器窗口的指定坐标。不论窗口滚动与否，元素都会留在那个位置。它始终是以 body 为依据的。 注意设置 fixed 属性的元素在标准流中不占位置。

## **3**、px，em，rem 的区别？

答： 1）px 像素（Pixel）。绝对单位。像素 px 是相对于显示器屏幕分辨率而言的，是一个虚拟长度单位，是计算机系统的数字化图像长度单位，如果 px 要换算成物理长度，需要指定精度 DPI。

2）em 是相对长度单位，相对于当前对象内文本的字体尺寸。如当前对行内文本的字体尺寸未被人为设置，则相对于浏览器的默认字体尺寸。它会继承父级元素的字体大小，因此并不是一个固定的值。

3）rem是[CSS3](http://www.html5cn.org/portal.php?mod=list&catid=16)新增的一个相对单位（rootem，根 em），使用 rem 为元素设定字体大小时，仍然是相对大小，但相对的只是 HTML 根元素。

4）区别：IE 无法调整那些使用 px 作为单位的字体大小，而 em 和 rem 可以缩放，rem 相对的只是 HTML 根元素。这个单位可谓集相对大小和绝对大小的优点于一身，通过它既可以做到只修改根元素就成比例地调整所有字体大小，又可以避免字体大小逐层复合的连锁反应。目前，除了 IE8 及更早版本外，所有浏览器均已支持 rem。

## 4、什么是BFC？

答： 1）定义：

BFC(Block formatting context)直译为"块级格式化上下文"。它是一个独立的渲染区域，只有Block-level box 参与， 它规定了内部的Block-level Box 如何布局，并且与这个区域外部毫不相干。

布局规则：

A.  内部的 Box 会在垂直方向，一个接一个地放置。

B. Box 垂直方向的距离由 margin 决定。属于同一个 BFC 的两个相邻 Box的margin 会发生重叠。

C.  每个元素的 margin box 的左边， 与包含块 border box 的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。

D. BFC 的区域不会与 float box 重叠。

E.  BFC 就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也如此。

F.  计算 BFC 的高度时，浮动元素也参与计算。

3）哪些元素会生成 BFC：

A.  根元素

B. float 属性不为 none

C. position 为 absolute 或 fixed

D. display 为 inline-block， table-cell，table-caption， flex， inline-flex F. overflow 不为visible

## 5、表格自动换行怎么实现？

答：word-break：normal 使用浏览器默认的换行规则；

break-all允许单词内换行；

keep-all只能在半角空格或连字符处换行

word-wrap：normal 是用浏览器默认的换行规则；break-word 在长单词或 URL 地址内部进行换行。

## 6、box-sizing、transition、translate分别是什么？

答：Box-sizing： 用来指定盒模型的大小的计算方式。主要分为boreder-box（从边框固定盒子大小）、content-box（从内容固定盒子大小）两种计算方式。

transition： 当前元素只要有“属性”发生变化时，可以平滑的进行过渡。通过 transtion-propety 设置过渡属性；

transtion-duration 设置过渡时间；

trantion-timing-function 设置过渡速度；

trantion-delay 设置过渡延时

translate：通过移动改变元素的位置；有 x、y、z 三个属性

## 7、选择器优先级是怎样的？

答：！important>行内样式>id 选择器>类选择器>标签选择器>通配符>继承

权重算法：

（0，0，0，0）==》第一个 0 对应的是 important 的个数，第二个 0 对应的是 id 选择器的个数，第三个 0 对

应的类选择器的个数，第四个 0 对应的是标签选择器的个数，就是当前选择器的权重。

比较：

先从第一个 0 开始比较，如果第一个 0 大，那么说明这个选择器的权重高，如果第一个相同，比较第二个，依次类推



## 8、Iframe的作用？

答：用法：

Iframe是用来在网页中插入第三方页面，早期的页面使用 iframe 主要是用于导航栏这种很多页面都相同的部分，这样可以在切换页面的时候避免重复下载。

优点：便于修改，模块分离，像一些信息管理系统会用到。但现在基本上不推荐使用。除非特殊需要，一般不推荐使用。

缺点 :

（1）iframe 的创建比一般的 DOM 元素慢了 1-2 个数量级

（2）iframe 标签会阻塞页面的加载，如果页面的onload 事件不能及时触发，会让用户觉得网页加载很慢，用户体验不好.在 Safari 和 Chrome 中可以通过 js 动态设置 iframe 的 src 属性来避免阻塞.

（3）iframe 对于 SEO 不友好，替代方案一般就是动态语言的 Incude 机制和 ajax 动态填充内容等.

## 9、有一个导航栏在 chrome  **里面样式完好？在** **IE** 里文字都聚到一起了，是哪个兼容性问题？

答：用了 display：flex 属性，在 ie10 以下都是无效的。

## 10、xhtml 和 **html** **有什么区别？**

答：HTML是一种基本的 WEB 网页设计语言，XHTML 是一个基于 XML 的置标语言最主要的不同：

XHTML元素必须被正确地嵌套。

XHTML元素必须被关闭。

标签名必须用小写字母。

XHTML文档必须拥有根元素。

## 11、标签上 title 与 **alt** 属性的区别是什么?

答：Alt 当图片不显示时，用文字代表。Title为该属性提供信息。

## 12、改变元素的外边距用什么属性？改变元素的内填充用什么属性？

答：改变元素的外边距用 margin，改变元素的内填充用 padding。

## 13、在新窗口打开链接的方法是？

答：target：_blank。

## 14、合理的页面布局中常听过结构与表现分离，那么结构是什么？表现是什么？

答：结构是 html，表现是 css。

## 15、简述对 Web 语义化的理解？

答：就是让浏览器更好的读懂你写的代码，在进行 HTML 结构、表现、行为设计时，尽量使用语义化的标签，使程序代码简介明了，易于进行Web 操作和网站 SEO，方便团队协作的一种标准，以图实现一种“无障碍”的  Web 开发。

## 16、每个 HTML  文件里开头都有个很重要的东西，Doctype，知道这是干什么的吗？

答：DOCTYPE 是一种标准通用标记语言的文档类型声明，它的目的是要告诉标准通用标记语言解析器，它应该使用什么样的文档类型定义来解析文档。只有确定了一个正确的文档类型，超文本标记语言或可扩展超文本标记语言中的标签和层叠样式表才能生效，甚至对 javascript 脚本都会有所影响。

## 17、display：none；与 visibility： **hidden** 的区别是什么？

答：display：none； 使用该属性后，HTML 元素（对象）的宽度、高度等各种属性值都将“丢失”；

visibility：hidden； 使用该属性后，HTML 元素（对象）仅仅是在视觉上看不见（完全透明），而它所占据的空间位置仍然存在，也即是说它仍具有高度、宽度等属性值。