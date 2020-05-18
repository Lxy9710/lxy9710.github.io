---
title: "Html重难点标签"
date: 2020-02-07T19:35:53+08:00
draft: false
---

# html 重难点标签

## a 标签的用法

HTML`<a>`元素（或称锚元素）可以创建通向其他网页、文件、同一页面内的位置、电子邮件地址或任何其他 URL 的超链接。

- href 取值

  1. 网址：
     比如 `http：//google.com` or `https：//google.com` or `//google.com`(无协议网址)

  2. 路径：
     比如`/a/b/c` (绝对路径：在文件中为根目录，但在开启 http 服务时，为开启 http 服务的根目录。同时不支持双击打开.)or `a/b/c`（相对路径）

  3. 伪协议:
     `javascript`代码；直接执行 js 用，现在不太常用。但代码留空时可以实现在点击时什么也不做。


       `mailto`： 跳转至发送邮件界面。

       `tel`： 手机号，在手机上可以实现跳转至拨打电话界面。
       `id`：href=xxx即跳到id为xxx的元素。

- target 取值

1. 内置名字

   `blank` ：在全新页面打开。

   `top`：在 iframe 中，在最外围一圈打开。

   `parent`：在父级窗口打开。

   `self`：在当前页面打开。（一般外网默认）

   其中 parent 和 top 的区别是：parent 是上一级窗口，top 是在顶级窗口。

2. 程序员命名
   `window`及`iframe`的 name。

## img 标签的用法

HTML img 元素将一份图像嵌入文档。主要格式为`<img src="" alt="">`:

1. src 属性是必须的，它包含了你想嵌入的图片的文件路径。

2. alt 属性包含一条对图像的文本描述，这不是强制性的，但对可访问性而言，它难以置信地有用——屏幕阅读器会将这些描述读给需要使用阅读器的使用者听，让他们知道图像的含义。如果由于某种原因无法加载图像，普通浏览器也会在页面上显示 alt 属性中的备用文本：例如，网络错误、内容被屏蔽或链接过期时。

   还有很多其他属性，可以实现各种不同的目的：

3. 使用 width、height 和 intrinsicsize 设置 原始分辨率：这将设置图像应占用的空间，以确保图像被加载之前页面的布局是稳定的。
4. 在 style 中设置 max-width="100%"设置响应式。

## table 标签的用法

HTML 的 table 元素表示表格数据 — 即通过二维数据表表示的信息。基本格式如下：包含`thead`（表头） `tbody`（表内容） `tfoot`（底部）三个标签。

```html
<table>
  <thead>
    <tr>
      <th colspan="2">The table header</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>The table body</td>
      <td>with two columns</td>
    </tr>
  </tbody>
</table>
```

- 其中：tr 表示 table 中的一行，td 包裹文字内容，th 用于表头中。
- 相关样式：
  1. table-layout： auto 为自动设置，fixed 为设置成等宽。
  2. border-collapse： 合并边框。

## 其他感想

html 标签很多，与要常常复习，翻看笔记巩固。
