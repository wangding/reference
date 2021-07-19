# HTML5 资料

HTML5 实战：HTML5 IN ACTION

## 第 1 章：HTML5：从文档到应用的转变

HTML5 是第一个将 Web 作为应用开发平台的 HTML 语言。

HTML5 定义了一系列新元素，用以帮助开发者创建富互联网应用，另外还提供了一些标准 JavaScript API，用来在浏览器内实现类原生应用。`<video>` 元素就是 HTML5 的新元素的一员，有了它，我们就可以在浏览器中播放视频，而无需安装任何额外插件。

ARIA：Accessible Rich Internet Application 可访问的富互联网应用

Web 起初只有文档，接下来 HTML 中增加了表单，接下来增加了 JavaScript。相比起 HTML4 来说，HTML5 最大的改进和差异在于利用 JavaScript 构建浏览器应用的能力。

### 新的语义元素

新的语义元素相当于一系列 `<div>` 元素。默认情况下，它们的作用就像是块元素一样，并且可以使用 CSS 进行样式化。它们的重要性来自于它们所有的标准语义。

HTML4 示例：
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title></title>
</head>
<body>
  <div class="header">
    <h1>My Site Name</h1>
    <h2>My Site Slogan</h2>
    <div class="nav">
      <ul><!-- Main Site Nav here --></ul>
    </div>
  </div>
  <div class="sidebar">
    <h3>Links Heading</h3>
    <ul><!-- Sidebar links --></ul>
  </div>
  <div class="main">
    <h4>Blog Post Title</h4>
    <div class="meta">
      Published by Joe on 01 May 2011 @ 12:30 pm
    </div>
    <div class="post">
      <!-- Actual blog post -->
    </div>
  </div>
  <div class="footer">
    <ul><!-- Footer links --></ul>
    <!-- Copyright info -->
  </div>
</body>
</html>
```

HTML5 示例：
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title></title>
</head>
<body>
  <header>
    <hgroup>
      <h1>My Site Name</h1>
      <h2>My Site Slogan</h2>
    </hgroup>
    <nav>
      <ul><!-- Main Site Nav Here --></ul>
    </nav>
  </header>

  <nav>
    <h1>Links Heading</h1>
    <ul><!-- Sidebar links --></ul>
  </nav>

  <section>
    <article>
      <header>
        <h1>Blog Post Title</h1>
        <div class="meta">
          Published by Joe on
          <time datetime="2012-05-01T12:30+00:00">
            01 May 2012 @ 12:30pm
          </time>
        </div>
      </header>
      <section>
        <!-- Actual blog post -->
      </section>
    </article>
  </section>

  <footer>
    <ul><!-- Footer Links --></ul>
    <!-- Copyright info -->
  </footer>
</body>
</html>
```

`<aside>` 元素来定义一个在页面中独立于主要内容区域的部分。在传统的书籍或杂志中，这部分内容通常表现为边栏。

`<mark>` 元素可以用来展示文档中应被标记或者说突出显示的文本部分，通常用来高亮显示文档的搜索词。

### WAI-ARIA

WAI (Web Accessibility Initiative, Web 可访问性倡议)

WAI-ARIA （无障碍网页应用）规范旨在通过对 HTML 文档作者提供的可访问性信息加以扩展来改善 Web 应用。

一堆 role 和 aria-\* 属性，具体这些属性的用法可以看下面的资料。

参考资料：
- http://www.zhangxinxu.com/wordpress/2012/03/wai-aria-无障碍阅读/

### HTML5 新的表单输入类型

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title></title>
</head>
<body>
  number: <input type="number"><br>
  range: <input type="range"><br>
  search: <input type="search"><br>
  time: <input type="time"><br>
  color: <input type="color"><br>
  date: <input type="date"><br>
  datetime: <input type="datetime"><br>
  datetime-local: <input type="datetime-local"><br>
  week: <input type="week"><br>
  month: <input type="month"><br>
</body>
</html>
```

### 10 种通用属性

autocomplete
multiple
autofocus
pattern
placeholder
list
required
max
step
min

## SVG

- 参考资料1：https://msdn.microsoft.com/zh-cn/library/gg193983(v=vs.85).aspx
- 新司机开车指南：https://zhuanlan.zhihu.com/p/25016633
- kity 核心作者的教学视频：https://link.zhihu.com/?target=http%3A//www.imooc.com/video/2609

## 本地存储

## 移动特性

## 新的语义标签


