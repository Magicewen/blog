# HTML 常用标签

### 根元素
元素 | 描述
-------|-------
&#60;html> | HTML `<html>` 元素 表示一个HTML文档的根（顶级元素），所以它也被称为根元素。所有其他元素必须是此元素的后代。

#### HTML
##### 属性
元素包含 [全局属性](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes)。

#####实例
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

##### link




 