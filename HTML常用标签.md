# HTML 常用标签

### 根元素
元素 | 描述
-------|-------
&#60;html> | HTML `<html>` 元素 表示一个HTML文档的根（顶级元素），所以它也被称为根元素。所有其他元素必须是此元素的后代。

#### HTML
##### 属性
元素包含 [全局属性](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes)。

##### 示例
> &#60;!DOCTYPE html><br>
  &#60;html lang="zh"><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&#60;head>...&#60;/head><br>
   &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&#60;body>...&#60;/body><br>
&#60;/html>


##### 注意事项
* 尽管在HTML里&#60;html>元素不是必需的，可以是隐含的，但是在XHTML里必须明确给出它的开标签和闭标签。
* 严格意义上，标签是指开始标签（例如 &#60;p> 标签）或结束标签（例如 &#60;/p> 标签）；元素（例如 p 元素或者称为<p>元素）则包括开始标签（自然也包括标签中定义的属性）、结束标签以及中间的内容（Content）。

### 文档元数据
元数据（Metadata）含有页面的相关信息，包括样式、脚本及数据，能帮助一些软件 (如搜索引擎，浏览器等等）更好地运用和渲染页面。对于样式和脚本的元数据，可以直接在网页里定义，也可以链接到包含相关信息的外部文件

元素 | 描述
-------|-------
&#60;link> | **HTML中`<link>`元素**规定了外部资源与当前文档的关系。 这个元素可用来为导航定义一个关系框架。这个元素最常于链接[样式表](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS)。
&#60;meta> | **HTML`<meta>`元素**表示那些不能由其它HTML元相关元素 ([`<base>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/base "HTML <base> 元素 指定用于一个文档中包含的所有相对URL的基本URL。一份中只能有一个<base>元素。"), [`&#60;link>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/link "HTML 中&#60;link>元素规定了外部资源与当前文档的关系。 这个元素可用来为导航定义一个关系框架。这个元素最常于链接样式表。"), [`<script>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/script "HTML <script> 元素用于嵌入或引用可执行脚本。"), [`<style>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/style "HTML的<style>元素包含文档的样式信息或者文档的部分内容。默认情况下，该标签的样式信息通常是CSS的格式。") 或 [`<title>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/title "HTML <title> 元素 定义文档的标题，显示在浏览器的标题栏或标签页上。它只可以包含文本，若是包含有标签，则包含的任何标签都不会被解释。")) 之一表示的任何元数据信息。
&#60;style> | **HTML的`<style>`元素**包含文档的样式信息或者文档的部分内容。默认情况下，该标签的样式信息通常是[CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)的格式。
&#60;title> | **HTML`&#60;title>` 元素** 定义文档的标题，显示在浏览器的标题栏或标签页上。它只可以包含文本，若是包含有标签，则包含的任何标签都不会被解释。

#### link

##### 示例
> &#60;link href="style.css" rel="stylesheet">


##### 注意事项
* &#60;link> 标签只能出现在head元素中，然而可以出现多个<link>标签。
* HTML 3.2只为link元素定义了href, methods, rel，rev，title，和urn属性。
* HTML 2为link标签定义了 href, methods，rel，rev，title，和 urn 属性，methods 和 urn随后从规范中移除。
* HTML和XHTML规范为link定义了事件处理，但是并不清楚它们将会怎样被使用。
* 在XHTML 1.0中，空元素link要求有尾随斜线，像这样&#60;link />。

#### meta

##### 属性
###### charset
此特性声明当前文档所使用的字符编码，但该声明可以被任何一个元素的 lang 特性的值覆盖。此特性的值必须是一个符合由IANA所定义的字符编码首选MIME 名称（preferred MIME name ）之一。尽管标准不要求必须使用某些特定的字符编码，但它还是给出了一些建议：

* 鼓励使用 UTF-8；
* 不应该使用不兼容ASCII的编码规范， 以避免不必要的安全风险：浏览器不支持他们(这些不规范的编码)可能会导致浏览器渲染html出错. 比如JIS_C6226-1983, JIS_X0212-1990, HZ-GB-2312, JOHAB,ISO-2022 系列,EBCDIC系列 等文字。

#### style
##### 属性
###### type
该属性以MIME类型（不应该指定字符集）定义样式语言。如果该属性未指定，则默认为 text/css。

###### title
指定可选的样式表。

#### 示例

> &#60;style type="text/css"><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;body {<br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;color:red;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}<br>
&#60;/style>

#### title

##### 示例
>  &#60;title>Awesome page title &#60;/title>


### 内容分区
内容分区元素允许你将文档内容从逻辑上进行组织划分。使用包括页眉(header)、页脚(footer)、导航(nav)和标题(h1~h6)等分区元素，来为页面内容创建明确的大纲，以便区分各个章节的内容。

元素 | 描述
-------|-------
&#60;address> | **HTML 的`<address>`元素**可以让作者为它最近的<article>或者<body>祖先元素提供联系信息。在后一种情况下，它应用于整个文档。
&#60;article> | **`&#60;article>`元素**表示文档、页面、应用或网站中的独立结构，其意在成为可独立分配的或可复用的结构，如在发布中，它可能是论坛帖子、杂志或新闻文章、博客、用户提交的评论、交互式组件，或者其他独立的内容项目。
&#60;aside> | **`<aside>` 元素**表示一个和其余页面内容几乎无关的部分，被认为是独立于该内容的一部分并且可以被单独的拆分出来而不会使整体受影响。其通常表现为侧边栏或者嵌入内容。他们通常包含在工具条，例如来自词汇表的定义。也可能有其他类型的信息，例如相关的广告、笔者的传记、web 应用程序、个人资料信息，或在博客上的相关链接。
&#60;footer> | **HTML `<footer>` 元素**表示最近一个章节内容或者根节点（sectioning root ）元素的页脚。一个页脚通常包含该章节作者、版权数据或者与文档相关的链接等信息。
&#60;header> | **`<header>`元素**表示一组引导性的帮助，可能包含标题元素，也可以包含其他元素，像logo、分节头部、搜索表单等。
&#60;h1> ~ &#60;h6> | **HTML `<h1>–<h6>` 标题(Heading)元素**呈现了六个不同的级别的标题，`<h1>` 级别最高，而 `<h6>` 级别最低。一个标题元素能简要描述该节的主题。标题信息可以由用户代理可以使用，例如，自动构造某个文档中的内容表（就像本文档右边浮动栏一样）。
&#60;main> | **HTML `<main>`元素**呈现了文档<body>或应用的主体部分。主体部分由与文档直接相关，或者扩展于文档的中心主题、应用的主要功能部分的内容组成。这部分内容在文档中应当是独一无二的，不包含任何在一系列文档中重复的内容，比如侧边栏，导航栏链接，版权信息，网站logo，搜索框（除非搜索框作为文档的主要功能）。
&#60;nav> | **HTML导航栏`<nav>`元素**描绘一个含有多个超链接的区域，这个区域包含转到其他页面，或者页面内部其他部分的链接列表。
&#60;section> | **HTML`<section>`元素**表示文档中的一个区域（或节），比如，内容中的一个专题组，一般来说会有包含一个标题（heading）。一般通过是否包含一个标题 (`<h1>-<h6>`) 作为子节点 来 辨识每一个`<section>`。