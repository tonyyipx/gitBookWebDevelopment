# 02 - HTML 简介

### ★HTML是什么

* HyperText Markup Language（超文本标记语言）
  * HyperText（超文本）：链接到网站中其他文档的文本片段
    * [第一个网站](https://info.cern.ch/hypertext/WWW/TheProject.html)
  *   Markup Language（标记语言）：类似编辑英文文稿标记

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-09 at 19.30.44.png" alt=""><figcaption><p>标签（Tags）</p></figcaption></figure>

### ★[标题元素](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading\_Elements)（Heading）

`<h1>` to `<h6>`

* 表示等级水平
* 标签 vs. 元素
  * 标签：尖括号里的所有内容
    * 开始标签，结束标签
    * 区别：/
  * 元素：开始标签、内容、结束标签
* 注意⚠️文件结构
  * 只有一个`h1`
    * 因为`h1`是最顶级的标题，如同书的名字一样
  * 不要直接从`h1`跳到`h3`
* [Web开发文档](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/Heading\_Elements)

### ★段落元素（Paragraph）

`<p>`

* 新段落
* 在线生成占位文本（placeholder text）器
  * [Lorem Ipsum Generator](https://www.lipsum.com/)
  * [Bacon Ipsum](https://baconipsum.com/)
  * [Bro Ipsum](https://www.broipsum.com/)

### ★空元素（自闭合标签）

`<hr />` 和 `<br />`

* 水平线元素（Horizontal Rule）
  * \<hr />
  * 划分内容，表明内容不相关
* 换行元素（Break）
  * \<br />
  * 将一段内容分成几行，才能得到它真正的含义
    * 如诗歌、地址
* [Diffchecker - 在线比较文本以查找两个文本文件之间的差异](https://www.diffchecker.com/)
* 注意⚠️新行
  * 可访问性：不要使用`<br />`来添加新行，而是要用`<p>`来添加新行
* `<hr>` 与 `<hr />`都可以，建议使用`<hr />`，这样会更容易看到这是一个空元素

### ★\[项目] 电影排名

`一个展示您收藏夹的的网站`

<figure><img src="../.gitbook/assets/goal (6).png" alt=""><figcaption></figcaption></figure>

```html
<h1>The Best Movies According to Tony</h1>
<h2>My top 3 movies of all-time.</h2>
<hr />
<h3>Spirited Away</h3>
<p>This is my favourite anime. I love the beautiful images.</p>
<h3>Ex Machina</h3>
<p>Really cool sci-fi movie.</p>
<h3>Drive</h3>
<p>Super beautiful film. Really artistic.</p>
```
