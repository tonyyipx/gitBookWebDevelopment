# 06 - CSS 属性

### ★CSS 颜色

`为我们的网站增添色彩`

* Color Properties
  * ```css
    html {
      background-color: red;
    }
    h1 {
      color: blue;
    }
    ```
* Named Colors
  * [\<named-color> - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/named-color)
  * [Color Hunt - The Most Popular Color Palettes of 2024](https://colorhunt.co/palettes/popular)
  * [RGB Mixer - Computer Science Field Guide](https://www.csfieldguide.org.nz/en/interactives/rgb-mixer/)

### ★字体属性

`改变文本的外观`

* Font Properties
  * ```css
    h1 {
      color: blue;
      font-weight: bold;/* 字体粗细 */
      font-size: 20px;/* 字体大小 */
      font-family: sans-serif;/* 字体系列 */
    }
    ```
* Font Size
  * ```css
    h1 {
      font-size: 20px;/* 字体大小 */
    }
    ```
  *   意味什么

      * 1 px（Pixel 像素）: 1/96th inch (0.26mm✖️0.26mm)
      * 1 pt（Point 磅点）: 1/72nd inch(0.35mm✖️0.35mm) 【word文档的字体用pt】
      * 1 em（）: 100% of parent 【相对于HTML元素的父级；文本的动态尺寸，相对于标准的 16px = 1em】
        *

            <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 15.55.11.png" alt=""><figcaption></figcaption></figure>
      * 1 rem（）: 100% of root 【文本的动态尺寸，相对于根元素；优先用于文本】

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 16.02.53.png" alt=""><figcaption><p>px vs. pt vs. em vs. rem</p></figcaption></figure>
* Font Weight
  * ```css
    h1 {
      font-weight: bold;/* 字体粗细 */
    }
    ```
  * 一些方法来改变字体粗细
    * Keywords（关键字）：normal/bold/...
    * Relative to Parent（相对于父级）：lighter/bolder
    * number：100-900（`-100`light or `+100`bold）
* Font Family
  * ```css
    h1 {
      font-family: Helvetica, sans-serif;/* 字体系列 */
    }

    h2 {
      font-family: "Times New Roman", serif;
    }
    ```
  *

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 16.13.46.png" alt=""><figcaption></figcaption></figure>
  * [浏览字体 - Google 字体](https://fonts.google.com/)（寻找免费字体）
    * ```html
      <head>
        <!-- .... -->
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Caveat&display=swap" rel="stylesheet">
      </head>
      ```
    * ```css
       /* Link: https://fonts.google.com/specimen/Caveat */
          h1 {
            font-family: 'Caveat', cursive;
          }
      ```
* Text Align
  * ```css
    h1 {
      text-align: center;/* 文本对齐 left right start end */
    }
    ```
  * [text-align - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)

### ★检查 CSS

`使用 CSS 概览功能`

* [Example HTML Website](https://appbrewery.github.io/just-add-css/)
* Chrome开发者工具：在其所做的任何更改（暂时的，供你观察和尝试）不会影响到你的原始文件
  * 打开
    * More Tools -> Developer Tools
    * 快捷键：`command`+`option`+`i` （windows）：`control`+`shift`+`i` （功能键）`F12`&#x20;
    * 右键 -> Inspect
  *   选择元素

      <div align="left">

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.00.09 (1).png" alt=""><figcaption></figcaption></figure>

      </div>
  *   元素（Element）选项卡的子部分

      *   样式（Styles）部分：显示应用于元素的样式

          * 单击style.css，显示其源码

          <div align="left">

          <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.08.08.png" alt="" width="375"><figcaption><p>单击style.css，显示其源码</p></figcaption></figure>

          </div>

          *   更改CSS工具\
              eg. 选择`h1`，单击“添加”，就可以为这个`h1`添加样式

              <div align="left">

              <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.10.41 (1).png" alt=""><figcaption><p>选择<code>h1</code>，单击“添加”，就可以为这个<code>h1</code>添加样式</p></figcaption></figure>

              </div>
          * 当自己的规则覆盖其他现有的规则

          <div align="left">

          <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.21.52.png" alt=""><figcaption></figcaption></figure>

          </div>
      * 如何知道实际应用到你的CSS元素上的内容呢？\
        计算后的样式（Computerd）部分：用于查看 HTML 元素**最终计算样式**的部分

      <div align="left">

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.26.16.png" alt="" width="563"><figcaption></figcaption></figure>

      </div>
  *   CSS Overview：显示一堆有的东西（颜色、字体...）

      <div align="left">

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.28.48.png" alt="" width="563"><figcaption></figcaption></figure>

      </div>

      <div align="left">

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.30.57.png" alt="" width="563"><figcaption></figcaption></figure>

      </div>

      * [CSS Inspection](https://appbrewery.github.io/css-inspection/)

### ★CSS 盒子模型 - 边距、填充和边框

`Margin（外边距）、Padding（内边距） 和 Border（边框）`

*   盒子模型：有宽度和高度形成的

    <div align="left">

    <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.38.50.png" alt="" width="375"><figcaption></figcaption></figure>

    </div>

    * height width&#x20;
    * `Border`&#x20;
    * ```css
      border: 10px solid black;/* 1边框的厚度 2边框的样式 Dashed 3边框的颜色*/
      /* 注意：html元素的盒子盒子（height width）没有改变 */
      ```



    <div align="left">

    <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.51.40.png" alt="" width="375"><figcaption><p>去除顶部边框</p></figcaption></figure>

    </div>

    <div align="left">

    <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.54.35.png" alt="" width="563"><figcaption></figcaption></figure>

    </div>

    *   `Padding`&#x20;

        <div align="left">

        <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.58.12 (1).png" alt="" width="375"><figcaption><p>无法使用padding获得元素之间的间距</p></figcaption></figure>

        </div>
    *   `Margin`&#x20;

        <div align="left">

        <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 18.00.39 (1).png" alt="" width="375"><figcaption></figcaption></figure>

        </div>
    *   检查器的Box Model &#x20;

        <div align="left">

        <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 18.04.56.png" alt=""><figcaption></figcaption></figure>

        </div>
    * [CSS Box Model](https://appbrewery.github.io/box-model/)
    *   Padding/Margin/Border-width设值&#x20;

        <div align="left">

        <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 18.08.21.png" alt="" width="563"><figcaption></figcaption></figure>

        </div>
* 人造盒子：将不同的内容的内容组合在一起，以便对其设置样式\
  \<div>\</div>（content division Element 内容划分元素）
  * 将一组HTML元素组合成一个盒子
  * 对于组织和划分网页内容非常有用
* [pesticide chrome extension](https://chromewebstore.google.com/detail/pesticide-for-chrome/bakpbgckdnepkmkeaiomhmfcnejndkbi?hl=en)：用于 **调试网页布局** 的 Chrome 浏览器扩展工具

<div align="left">

<figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 18.22.43.png" alt=""><figcaption></figcaption></figure>

</div>

### ★\[项目] 励志海报网站

`制作自己的表情包`

<figure><img src="../.gitbook/assets/goal (1) (1).png" alt=""><figcaption></figcaption></figure>

```html
<!-- 
  TODO: 创建一个励志风格的网页。
  可以根据自己的喜好进行样式设计。
  可以参考目标图片进行灵感设计。
  但网页必须包含以下功能：
1. 主标题 h1 文本应使用 Google Fonts 中的 Regular Libre Baskerville 字体：
  https://fonts.google.com/specimen/Libre+Baskerville
2. 文本应为白色，背景为黑色。
3. 在 assets 文件夹内的 images 文件夹中添加一张自己的图片。图片需有 5px 的白色边框。
4. 文本应居中对齐。
5. 创建一个 div 容器来包含 h1、p 和 img 元素。调整边距，使图片和文本在页面上居中显示。
  提示：可以通过设置 div 宽度为 50%，并设置 margin-left 为 25% 来水平居中 div。
  提示：将图片的宽度设置为 100%，以便图片填满 div 容器。
6. 在 MDN 文档上了解 text-transform 属性，使用 CSS 将 h1 文本转换为大写：
  https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform 
-->
```

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Motivation Meme</title>
  <link rel="stylesheet" href="./solution.css" />
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Libre+Baskerville&display=swap" rel="stylesheet">
</head>

<body>

  <div class="poster">
    <img class="motivation-img" src="./assets/images/daenerys.jpeg" src="daenerys with egg" />
    <h1>That Special Moment</h1>
    <p>When you find the perfect avocado at the supermarket</p>
  </div>
</body>

</html>
```

```css
/* 为整个页面设置黑色背景 */
body {
  background-color: black;
}

/* 将 h1 标题转换为大写字母并设置较大的字体大小 */
h1 {
  text-transform: uppercase;
  font-size: 3rem;
}

/* .poster 类用于包含整个海报内容 */
.poster {
  /* 设置海报宽度为页面的一半 */
  width: 50%;
  /* 将海报居中显示 */
  margin-left: 25%;
  /* 为海报与顶部之间留出空间 */
  margin-top: 100px;
  /* 设置文本颜色为白色 */
  color: white;
  /* 使用 Google 字体 Libre Baskerville */
  font-family: "Libre Baskerville", serif;
  /* 将海报内的文本居中对齐 */
  text-align: center;
}

/* 为图片添加白色边框并调整图片大小 */
.motivation-img {
  /* 添加 5px 的白色边框 */
  border: 5px solid white;
  /* 图片宽度调整为容器的 100% */
  width: 100%;
}
```
