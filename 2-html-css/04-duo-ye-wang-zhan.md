# 04 - 多页网站

### ★文件路径

`绝对路径`和`相对路径`

* 计算机文件/文件夹的唯一位置
* 查找硬盘(C:/Mac)中的特定位置
  * 绝对路径
    * C: / Macintosh HD
    * 无论是在哪个文件结构中，都可以从最开始的位置导航到目标位置
  * 相对路径
    * 相对于编写代码的位置来指定路径
    * 更短
    * 移动文件夹，仍然有效
    * 在Web开发中，引用特定资源(图像/音频/视频/其他HTML文件)时
    * 特殊字符
      * `../`：上一级目录
      * `./`：当前目录

### ★网页

`构建多页网站`

* 一个Project文件夹：包含整个网站
  * 起始文件：index.html（写代码的地方）
  * 其他辅助文件（Images文件夹/其他文件夹）

### ★HTML模板

`理解HTML结构`

* \<!DOCTYPE html>
  * 文档类型声明：告诉浏览器，文件使用的HTML版本 - HTML5 (最新版本)
* \<html lang="en">
  * 根元素：包含所有元素
  * `lang`：元素内文本内容的语言（对辅助技术的用户很关键）
* \<head>
  * 放置关于网页的重要信息：包括一些帮助网站在浏览器中正确显示的内容，但不包括用户会看到的文本或图片
  * \<meta />
    * 告诉浏览器如何显示HTML网页
    * `charset`="UTF-8"：确保网站上的字符正确显示
      * 指定网页字符编码的 meta 标签
    * `name`="description"
      * 简要描述网页，告知搜索引擎如何显示页面链接
  * \<title>
    * 显示在浏览器的标签栏里
* \<body>
  * 创建和编写网站的所有内容和结构(文本/标题/图片/链接/HTML可以实现的所有内容)
  * \<h1>\</h1>

### ★\[项目] HTML 作品集

```html
<!DOCTYPE html>
<html lang="zh">
  <head>
    <meta charset="UTF-8" />
    <title>Tony的作品集</title>
  </head>

  <body>
    <h1>Tony Yipx 的作品集</h1>
    <h2>我是一个 Web 开发者</h2>
    <hr />
    <h3><a href="./public/movie-ranking.html">电影排名项目</a></h3>
    <img
      src="./assets/images/movie-ranking.png"
      height="200"
      alt="电影排名项目预览"
    />
    <h3><a href="./public/birthday-invite.html">生日邀请项目</a></h3>
    <img
      src="./assets/images/birthday-invite.png"
      height="200"
      alt="生日邀请项目预览"
    />
    <hr />
    <a href="./public/about.html">关于我</a>
    <a href="./public/contact.html">联系我</a>
  </body>
</html>
```

