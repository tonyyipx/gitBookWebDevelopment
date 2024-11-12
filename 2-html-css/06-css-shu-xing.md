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
      * 1 em（）: 100% of parent: 相对上一级
        *

            <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 15.55.11.png" alt=""><figcaption></figcaption></figure>
      * 1 rem（）: 100% of root：根据\<html>

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
* Chrome开发者工具
  * 打开
    * More Tools -> Developer Tools
    * 快捷键：`command`+`option`+`i` （windows）：`control`+`shift`+`i` （功能键）`F12`&#x20;
    * 右键 -> Inspect
  * 选择元素
    *

        <div align="left">

        <figure><img src="../.gitbook/assets/Screenshot 2024-11-12 at 17.00.09 (1).png" alt=""><figcaption></figcaption></figure>

        </div>
  * 元素（Element）选项卡的子部分
    * 样式（Styles）部分：显示应用于元素的样式
      * 单击style.css显示源码
      *

          <figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>
      * 更改CSS工具
        * 1
        *



### ★CSS 盒子模型 - 边距、填充和边框

`Margin（外边距）、Padding（内边距） 和 Border（边框）`

\




### ★\[项目] 励志海报网站

`制作自己的表情包`











