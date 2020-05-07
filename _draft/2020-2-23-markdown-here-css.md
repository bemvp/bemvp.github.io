---
layout: post
title: markdown here CSS
categories: [cate1, cate2]
description: some word here
keywords: markdown排版
changelog: 2020年2月23日19:47:59
---

.markdown-here-wrapper {/*markdown here 的全局配置*/
  font-size: 16px;  
  line-height: 1.8em;   
  /*em指的是相对单位，当前对象内字体的尺寸，默认浏览器16px*/
  /*http://www.w3school.com.cn/cssref/css_units.asp*/
  letter-spacing: 0.1em;
}

pre, code {   /*,逗号连接是并集选择器*/
  font-size: 14px;
  font-family: Roboto, 'Courier New', Consolas, Inconsolata, Courier, monospace;
  margin: auto 5px;
}
/*设置pre 和code的整体属性，pre可以把div中的/r/n保存下来显示，而code则用浏览器的方式渲染*/
code {
  white-space: pre-wrap;
  border-radius: 2px;
  display: inline;
}
/*display 的属性为指定元素框的类型*/
/*margin： 0为默认值，auto为浏览器自动计算的外边距，外边距属性*/
/*border-radius: div元素的圆角框*/
/*write-space:如何处理元素内空白行，回车or忽略,nowrap不换行，pre-wrap换行*/
/*http://www.w3school.com.cn/cssref/pr_text_white-space.asp*/


pre {  /*pre 元素可定义预格式化的文本。被包围在 pre 元素中的文本通常会保留空格和换行符。而文本也会呈现为等宽字体。*/
  font-size: 15px;
  line-height: 1.4em;
  display: block; !important;  /*在ie6以上的浏览器中，设置优先级，覆盖预先设置的属性 !important*/
}

pre code {  /*空格连接是后代选择器，外层在前内层在后； >连接是子元素选择器*/
  white-space: pre;
  overflow: auto;   /*内容益处元素框时候的行为*/
  border-radius: 3px;
  padding: 1px 1px;
  display: block !important;
}

/*各种选择器：https://blog.csdn.net/m0_38070602/article/details/69950795*/

/*pre code 的解释：http://www.cnblogs.com/lizonghui/archive/2012/09/18/2692355.html*/
strong, b{  /*strong表示强调，用<b>粗体显示，也可以自定义自己的强调方式*/
  color: #BF360C;
}

em, i {  /*em表示强调，用<i>标签斜体显示，也可以自定义自己的强调方式*/
  color: #009688;
}

hr {   /*水平线分割---*/
  border: 1px solid #BF360C;
  margin: 1.5em auto;
}

p {  /*段落选择器*/
  margin: 1.5em 5px !important;
  /*颜色*/
  color:#1F1F1F;   
  /*字体*/
  font-family:'微软雅黑';
  /*字号*/
  font-size:15px;
  /*行间距，可用百分比，数值倍数，像素设置，还包括text-indent缩进、letter-spacing字间距、*/
  line-height:100%  2  100px;
  /*段间距，一般用margin属性调整*/
  margin-bottom:20px;
  /*页边距用padding属性调整*/
}

/*表格和*/
table, pre, dl, blockquote, q, ul, ol {
  margin: 10px 5px;
  /*并集选择器：表格、预格式化、定义列表、块引用、短引用、无序列表、有序列表*/
}

ul, ol {  /*无序、有序列表*/
  padding-left: 15px;
}

li {  /* 定义列表中的项目*/
  margin: 10px;
}

li p {  /*li列表元素中的后代选择器，包含选择器，应用于li中的p*/
  margin: 10px 0 !important;
}

ul ul, ul ol, ol ul, ol ol {    /*各个后代选择器一起添加属性*/
  margin: 0;
  padding-left: 10px;
}

ul {
  list-style-type: circle;
}
/*无序列表的前缀，circle,square,好多种,同样有序列表ol也可以设置不同的标记*/
/*http://www.w3school.com.cn/cssref/pr_list-style-type.asp*/

dl {
  padding: 0;
}

dl dt {
  font-size: 1em;
  font-weight: bold;  /*加粗  意大利斜体*/
  font-style: italic;
}

dl dd {
  margin: 0 0 10px;
  padding: 0 10px;
}
/*各种表格的包含选择器定义，用空格连接*/


blockquote, q {
  border-left: 2px solid #009688;
  padding: 0 10px;   /*上右下左的排序，可输入四个值*/
  color: #777;
  quotes: none;
  margin-left: 1em;
}
/*块引用和短引用的样式*/

blockquote::before, blockquote::after, q::before, q::after {
  content: none;
}
/*before 和after属于css伪元素，:before在元素之前插入相应。：after在之后插入*/
/*伪元素用::，伪类用：参考ref。。https://blog.csdn.net/qq_25292481/article/details/52577320*/


/*--------同时设置六级标题的属性，其中！important用于指定优先级>ie6--------------*/
h1, h2, h3, h4, h5, h6 {
  margin: 20px 0 10px;
  padding: 0;
  font-style: bold !important;
  color: #009688 !important;
  text-align: center !important;
  margin: 1.5em 5px !important;
  padding: 0.5em 1em !important;
}

h1 {
  font-size: 24px !important;
  border-bottom: 1px solid #ddd !important;
}

h2 {
  font-size: 20px !important;
  border-bottom: 1px solid #eee !important;
}

h3 {
  font-size: 18px;
}

h4 {
  font-size: 16px;
  /*可以针对自己的标题做出个性化设置*/
  color:#d6a841   /*16进制颜色*/
  font-style: bold /*加粗？倾斜*/
  /*---------各种居中方式---------*/
  margin: 0, auto;        /*块级元素居中*/
  text-align: center;    /*行内居中*/
  justify-content: center;  /*对齐*/
  vertical-align: middle;  /*垂直居中*/
  /*ref:   https://www.jianshu.com/p/61c431fd924a*/

}

/*-------------表格元素的设置-----------------*/
table {
  padding: 0;
  border-collapse: collapse;  /*合并边框属性*/
  border-spacing: 0;  
  font-size: 1em;
  font: inherit;
  border: 0;
  margin: 0 auto;
}

tbody {
  margin: 0;
  padding: 0;
  border: 0;
}

table tr {
  border: 0;
  border-top: 1px solid #CCC;
  background-color: white;
  margin: 0;
  padding: 0;
}

table tr:nth-child(2n) {
  background-color: #F8F8F8;
}

table tr th, table tr td {
  font-size: 16px;
  border: 1px solid #CCC;
  margin: 0;
  padding: 5px 10px;
}

table tr th {  /*表格。tableraw，tableheader*/
  font-weight: bold;
  color: #eee;
  border: 1px solid #009688;
  background-color: #009688;
}


----------
可根据markdown的实现自己的**个性化**标记
@strong-char: "**";  /*可以将着重符号替换为自己的个性化符号*/
strong:before, strong:after {
    content: @strong-char;
    display: inline;
}
@em-char: "*";   
em:before, em:after {
    content: @em-char;
    display: inline;
}
/*https://github.com/mrcoles/markdown-css/blob/master/markdown.less*/
/*http://www.jb51.net/css/357685.html*/




/*<span>行内封装，<div>块级封装*/
/*copy from jianshu*/
/*source code:https://www.jianshu.com/p/7bda360950ce*/

李笑来的markdownhere.css
.markdown-here-wrapper {
  font-size: 16px;
  line-height: 1.8em;
  letter-spacing: 0.1em;
}


pre, code {
  font-size: 14px;
  font-family: Roboto, 'Courier New', Consolas, Inconsolata, Courier, monospace;
  margin: auto 5px;
}

code {
  white-space: pre-wrap;
  border-radius: 2px;
  display: inline;
}

pre {
  font-size: 15px;
  line-height: 1.4em;
  display: block; !important;
}

pre code {
  white-space: pre;
  overflow: auto;
  border-radius: 3px;
  padding: 1px 1px;
  display: block !important;
}

strong, b{
  color: #BF360C;
}

em, i {
  color: #009688;
}

hr {
  border: 1px solid #BF360C;
  margin: 1.5em auto;
}

p {
  margin: 1.5em 5px !important;
}

table, pre, dl, blockquote, q, ul, ol {
  margin: 10px 5px;
}

ul, ol {
  padding-left: 15px;
}

li {
  margin: 10px;
}

li p {
  margin: 10px 0 !important;
}

ul ul, ul ol, ol ul, ol ol {
  margin: 0;
  padding-left: 10px;
}

ul {
  list-style-type: circle;
}

dl {
  padding: 0;
}

dl dt {
  font-size: 1em;
  font-weight: bold;
  font-style: italic;
}

dl dd {
  margin: 0 0 10px;
  padding: 0 10px;
}

blockquote, q {
  border-left: 2px solid #009688;
  padding: 0 10px;
  color: #777;
  quotes: none;
  margin-left: 1em;
}

blockquote::before, blockquote::after, q::before, q::after {
  content: none;
}

h1, h2, h3, h4, h5, h6 {
  margin: 20px 0 10px;
  padding: 0;
  font-style: bold !important;
  color: #009688 !important;
  text-align: center !important;
  margin: 1.5em 5px !important;
  padding: 0.5em 1em !important;
}

h1 {
  font-size: 24px !important;
  border-bottom: 1px solid #ddd !important;
}

h2 {
  font-size: 20px !important;
  border-bottom: 1px solid #eee !important;
}

h3 {
  font-size: 18px;
}

h4 {
  font-size: 16px;
}


table {
  padding: 0;
  border-collapse: collapse;
  border-spacing: 0;
  font-size: 1em;
  font: inherit;
  border: 0;
  margin: 0 auto;
}

tbody {
  margin: 0;
  padding: 0;
  border: 0;
}

table tr {
  border: 0;
  border-top: 1px solid #CCC;
  background-color: white;
  margin: 0;
  padding: 0;
}

table tr:nth-child(2n) {
  background-color: #F8F8F8;
}

table tr th, table tr td {
  font-size: 16px;
  border: 1px solid #CCC;
  margin: 0;
  padding: 5px 10px;
}

table tr th {
  font-weight: bold;
  color: #eee;
  border: 1px solid #009688;
  background-color: #009688;
}

#### 我的自定义
/*自定义样式，实时生效*/

/* 全局属性
 * 页边距 padding:30px;
 * 全文字体 font-family:ptima-Regular;
 * 英文换行 word-break:break-all;
 */
#nice {
  font-family:PingFangSC-Light;
}

/* 段落，下方未标注标签参数均同此处
 * 上边距 margin-top:5px;
 * 下边距 margin-bottom:5px;
 * 行高 line-height:26px;
 * 词间距 word-spacing:3px;
 * 字间距 letter-spacing:3px;
 * 对齐 text-align:left;
 * 颜色 color:#3e3e3e;
 * 字体大小 font-size:16px;
 * 首行缩进 text-indent:2em;
 */
#nice p {
  margin:10px 10px;
  line-height:1.75;
  letter-spacing:0.2em;
  font-size: 15px;
  word-spacing:0.1em;
}

/* 一级标题 */
#nice h1 {
  border-bottom: 2px solid #0e88eb;
  font-size: 1.4em;
  text-align: center;
}

/* 一级标题内容 */
#nice h1 .content {
  font-size: 1.4em;
  display:inline-block;
  font-weight: bold;
  //background: #0e88eb;
  color:#ffffff;
  color: #0e88eb;
  padding:3px 10px 1px;
  border-top-right-radius:3px;
  border-top-left-radius:3px;
  margin-right:3px;
}

/* 一级标题修饰 请参考有实例的主题 */
#nice h1:after {
}
 
/* 二级标题 */
#nice h2 {
  text-align:left;
  margin:20px 10px 0px 0px;
}

/* 二级标题内容 */
#nice h2 .content {
  font-family:STHeitiSC-Light;
  font-size: 22px;
  color:#0e88eb;
  font-weight:bolder;
  display:inline-block;
  padding-left:10px;
  border-left:5px solid #0e88eb;
}

/* 二级标题修饰 请参考有实例的主题 */
#nice h2:after {
}

/* 三级标题 */
#nice h3 {
	font-size: 18px;
 	color: #0e88eb;
}

/* 三级标题内容 */
#nice h3 .content {
  font-size: 18px;
  color: #0e88eb;
}

/* 三级标题修饰 请参考有实例的主题 */
#nice h3:after {
}

/* 无序列表整体样式
 * list-style-type: square|circle|disc;
 */
#nice ul {
}

/* 有序列表整体样式
 * list-style-type: upper-roman|lower-greek|lower-alpha;
 */
#nice ol {
}

/* 列表内容，不要设置li
 */
#nice li section {
  font-size: 15px;
}

/* 引用
 * 左边缘颜色 border-left-color:black;
 * 背景色 background:gray;
 */
#nice blockquote {
  font-style:normal;
  border-left:none;
  padding:10px;
  position:relative;
  line-height:1.8;
  border-radius:0px 0px 10px 10px;
  color: #0e88eb;
  background:#fff;
  box-shadow:#84A1A8 0px 10px 15px;
}
#nice blockquote:before {
  content:"★ ";
  display:inline;
  color: #0e88eb;
  font-size:4em;
  font-family:Arial,serif;
  line-height:1em;
  font-weight:700;
}

/* 引用文字 */
#nice blockquote p {
  color: #0e88eb;
  font-size:15px;
  display:inline;
}
#nice blockquote:after {
  content:"”";
  float:right;
  display:inline;
  color:#0e88eb;
  font-size:3em;
  line-height:1em;
  font-weight:500;
}

/* 链接 
 * border-bottom: 1px solid #009688;
 */
#nice a {
  color: #0e88eb;
  border-bottom: 0px solid #ff3502;
  font-family:STHeitiSC-Light;
}

/* 加粗 */
#nice strong {
  font-weight: border;
  color: #0e88eb;
}

/* 斜体 */
#nice em {
  color: #0e88eb;
  letter-spacing:0.3em;
}

/* 加粗斜体 */
#nice em strong {
  color: #0e88eb;
  letter-spacing:0.3em;
}

/* 删除线 */
#nice del {
}
 
/* 分隔线
 * 粗细、样式和颜色
 * border-top:1px solid #3e3e3e;
 */
#nice hr {
  height:1px;
  padding:0;
  border:none;
  border-top:medium solidid #333;
  text-align:center;
  background-image:linear-gradient(to right,rgba(248,57,41,0),#0e88eb,rgba(248,57,41,0));
}

/* 图片
 * 宽度 width:80%;
 * 居中 margin:0 auto;
 * 居左 margin:0 0;
 */
#nice img {
  border-radius:0px 0px 5px 5px;
  display:block;
  margin:20px auto;
  width:85%;
  height:100%;
  object-fit:contain;
  box-shadow:#84A1A8 0px 10px 15px;
}

/* 图片描述文字 */
#nice figcaption {
  display:block;
  font-size:12px;
  font-family:PingFangSC-Light;
}

/* 行内代码 */
#nice p code, #nice li code {
  color:/*自定义样式，实时生效*/
}

/* 非微信代码块
 * 代码块不换行 display:-webkit-box !important;
 * 代码块换行 display:block;
 */
#nice pre code {
}

/*
 * 表格内的单元格
 * 字体大小 font-size: 16px;
 * 边框 border: 1px solid #ccc;
 * 内边距 padding: 5px 10px;
 */
#nice table tr th,
#nice table tr td {
  font-size: 15px;
}

/* 脚注文字 */
#nice .footnote-word {
  color: #2d59b3;
}

/* 脚注上标 */
#nice .footnote-ref {
  color: #6a88c5;
}

/* 非微信代码块
 * 代码块不换行 display:-webkit-box !important;
 * 代码块换行 display:block;
 */
#nice pre code {
}

/* 脚注文字 */
#nice .footnote-word {
  color: #0e88eb;
}

/* 脚注上标 */
#nice .footnote-ref {
  color: #0e88eb;
}

/*脚注链接样式*/
#nice .footnote-item em {
  color: #082a71;
  font-size:12px;
}

/* "参考资料"四个字 
 * 内容 content: "参考资料";
 */
#nice .footnotes-sep:before {
}

/* 参考资料编号 */
#nice .footnote-num {
}

/* 参考资料文字 */
#nice .footnote-item p { 
}

/* 参考资料解释 */
#nice .footnote-item p em {
}

/* 行间公式
 * 最大宽度 max-width: 300% !important;
 */
#nice .block-equation svg {
}

/* 行内公式
 */
#nice .inline-equation svg {  
}

/* 滑动图片
 */
#nice .imageflow-img {
  display: inline-block;
  width:100%;
  margin-bottom: 0;
}