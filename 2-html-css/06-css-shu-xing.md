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

*



### ★CSS 盒子模型 - 边距、填充和边框

`Margin（外边距）、Padding（内边距） 和 Border（边框）`

\




### ★\[项目] 励志海报网站

`制作自己的表情包`











* Tags（标签）
  * 斜体
    * \<em> vs \<i>
      * 使用em优于i，因为i只是用于样式，而em不仅传递给用户，还传递给浏览器更多信息
    * 强调
      * \<em>
      * 对标签进行强调
    * 斜体
      * \<i>
      * 仅用于样式
  * 加粗
    * \<strong> vs \<b>
      * 使用strong优于b，因为strong表示更重要的内容
  * 表格
    * \<table>
      * \<thead>
        * 表头
      * \<tbody>
        * 表体
      * \<tfoot>
        * Table Footer（表脚）
      * \<tr>
        * Table Row（表格行）
      * \<td>
        * Table Data（表格数据单元格）
      * \<th>
        * Table header cell（表格头单元格）
  * 表单
    * \<form>
    * Labels（标签）
      * \<label>
    * 输入
      * \<input>
        * email
        * color
        * password
        * checkbox
        * date
        * range
        * radio
        * …

