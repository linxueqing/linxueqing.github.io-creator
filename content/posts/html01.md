---
title: "HTML入门笔记1"
date: 2020-02-22T17:54:06+08:00
draft: false
---

## HTML 入门笔记 1

1. HTML 是谁发明的

   HTML 的英文全称是 Hypertext Marked Language，即超文本标记语言。HTML 是由 Web 的发明者 Tim Berners-Lee 和同事 Daniel W. Connolly 于 1990 年创立的一种标记语言，它是标准通用化标记语言 SGML 的应用。

2. HTML 起手应该写什么

```
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>标题</title>
</head>
<body>

</body>
</html>
```

3. 常用的表章节的标签有哪些，分别是什么意思（h1~h6、section、article、main、aside 等等）
   - `h1~h6` 标题
   - `section` 章节
   - `article` 文章
   - `main` 页面主要内容
   - `aside` 页面次要内容
4. 全局属性有哪些?

   所有标签都有的属性

   - `class` 的值是一个以空格分隔的元素的类名（classes ）列表，它允许 CSS 和 Javascript 通过类选择器 (class selectors) 或 DOM 方法( document.getElementsByClassName)来选择和访问特定的元素。
   - `contenteditable` 是一个枚举属性，表示元素是否可被用户编辑。 如果可以，浏览器会修改元素的部件以允许编辑。
   - `hidden` 是一个布尔属性，表示一个元素尚未或者不再相关。例如，它可以被用来隐藏一个页面元素直到登录完毕。如果一个元素设置了这个属性，它就不会被显示。
   - `id` 定义了一个全文档唯一的标识符 (ID)。它用于在链接（使用片段）、脚本和样式（通过 CSS）中辨识元素。
   - `style` 包含应用到元素的 CSS 样式声明。要注意样式最好定义在单独的文件中。这个属性以及 <style> 元素的主要目的是快速装饰。
   - `tabindex` 指示其元素是否可以聚焦，以及它是否/在何处参与顺序键盘导航（通常使用 Tab 键，因此得名）
   - `title` 包含了表示咨询信息文本，和它属于的元素相关。这个信息通常存在，但绝不必要，作为提示信息展示给用户。设置了这个属性鼠标移入会显示设置内容。

5) 常用的内容标签有哪些，分别是什么意思（a、strong、em、code、pre 等等）
   - `a` <a> 元素（或称锚元素）可以创建通向其他网页、文件、同一页面内的位置、电子邮件地址或任何其他 URL 的超链接。
   - `strong` <strong> 元素表示文本十分重要，一般用粗体显示。
   - `em` <em> 元素标记出需要用户着重阅读的内容
   - `code` <code> 元素呈现一段计算机代码. 默认情况下, 它以浏览器的默认等宽字体显示.
   - `pre` <pre> 元素表示预定义格式文本。
