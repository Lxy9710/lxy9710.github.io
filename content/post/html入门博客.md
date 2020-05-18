---
title: "Html入门博客"
date: 2020-02-07T12:04:25+08:00
draft: false
---

# html 入门博客

超文本标记语言（英语：HyperText Markup Language，简称：HTML）是一种用于创建网页的标准标记语言。HTML 是一种基础技术，常与 CSS、JavaScript 一起被众多网站用于设计网页、网页应用程序以及移动应用程序的用户界面。

## html 历史

1980 年，物理学家蒂姆·伯纳斯-李在欧洲核子研究中心（CERN）在承包工程期间，为使 CERN 的研究人员使用并共享文档，他提出并创建原型系统 ENQUIRE。1989 年，伯纳斯-李在一份备忘录中提出一个基于互联网的超文本系统。他规定 HTML 并在 1990 年底写出浏览器和服务器软件。同年，伯纳斯-李与 CERN 的数据系统工程师罗伯特·卡里奥联合为项目申请资助，但未被 CERN 正式批准。在他的个人笔记中伯纳斯-李列举“一些使用超文本的领域”，并把百科全书列为首位。

## html 起手式

首先输入！后摁 Tab 键，自动生成 html 起手式。

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

## 章节标签

- `<h1></h1>` ：标题标签 h 一般从 h1 写至 h6，其中 h1 一般只写一次，用来表示第一个大标题。

- `<section></section>`：章节

- `<article></article>`：文章

- `<p></p>`：段落

- `<header></header>`：头部标签

- `<footer></footer>`：脚部 底部标签

- `<main></main>`：主要内容

- `<aside></aside>`：旁支内容，一般用来写导航，参考资料等。

## 全局属性

即所有标签都具有的属性。

- `class`：class 的值是一个以空格分隔的元素的类名（classes ）列表。对 class 进行声明时[`class="A"`]会对确切的 A 类对象进行编辑，若是有多个 class 并列则不行。

- `contenteditable`: 该标签使得页面可以直接编辑。

  eg：可实现在页面中直接编辑 style 元素。

  ```html
  <style contenteditable>
  ```

- `hidden`:将元素隐藏，看不见。
- `id`:id 与 class 的区别在于 id 是应用于全页面唯一的，且不报错。所以尽量使用 class 避免 id 的复用。
- `style`:元素包含文档的样式信息或者文档的部分内容。默认情况下，该标签的样式信息通常是 CSS 的格式。
- `tabindex`：将该属性添加在标签中可以替代鼠标来控制响应顺序。可以取值为：1，2，3，4……-1，0.

其中-1 表示永远不会被用 Tab 选中；0 表示最后访问；正数值则顺序访问。

- `title`：定义文档的标题，显示在浏览器的标题栏或标签页上。它只可以包含文本，若是包含有标签，则包含的任何标签都不会被解释。当 title 过长溢出时：

  `whitespace:nowrap`:不换行。

  `text-overflow`:忽略溢出部分。

  `overflow:hidden`:用省略号替代溢出部分。

## 常用的内容标签

- `<a href=""></a>`：其中 href 可以取值网址，路径，伪协议。

- `<em></em>`和`<strong></strong>`:两者都表示强调。em 时语义上的。

- `quote`：引用，blockquote 整段引用。

- `<pre></pre>`:保留源格式。

- `<code></code>`:该标签内字体等宽，可放置代码。
- `<hr>`:水平分割线。
- `<br>`:换行。

未完待续。
