# 05 - CSS 简介

### ★为什么我们需要 CSS

`什么是 CSS？`

* What：**C**ascading **S**tyle **S**heet (**CSS**) **层叠样式表**
  * **C**ascading
    * 在编程中，“cascading” 通常与 **CSS（Cascading Style Sheets）** 相关，即样式会按照优先级从上到下逐层应用。
    * 样式的应用方式如瀑布般层层递进
  * **S**tyle **S**heet
    * 类似于HTML，是一种标记语言
    * 一种允许我们指定网站上的内容的外观
    * 该语言有很多种类型：
      * CSS：最重要的
      * Sass：它在语法上很棒的样式表
      * Less：代表Learner CSS
      * ...
* Why：
  * HTML 3.2 (\[最初只有html时]1997年W3C发布)：引入新的HTML标签
    * font tag：font size/color/face
      * \<center>
      * 已被弃用：因为我们的HTML应该是用于内容的，如果在所有内容中添加大量的样式，那么这将会极大地扰乱你的所有HTML，无法分辨出该网站的结构和内容到底是什么
  * 1996年W3C的Håkon Wium Lie建议
    * 允许附加样式 (eg. fonts, colors and spacing)到HTML文档
      * 这是一个突破：能够将风格与内容分开
        * 模块化：关注点分离，以便有人负责 (like 汽车生产线)
* How：[Example HTML Website](https://appbrewery.github.io/just-add-css/)
* 网页中的每个元素本质上都是由一系列盒子组成的

### ★ 如何添加 CSS

内联样式 `Inline CSS` 内部样式 `Internal CSS` 外部样式 `External CSS`

* 内联CSS
  * CSS属性可以放在HTML文件中，直接位于各个HTML标签内，为页面提供样式
* 内部CSS
  * 在 \<head> 标签中使用 \<style> 标签定义样式
* 外部CSS
  * 使用 \<link rel=”stylesheet” href=”css\_file”> 在HTML文件的 \<head> 中链接到.css文件
  * rel: relationship - 指的是所链接的东西的作用是什么
  * href: located - 位于哪里

### ★CSS 选择器

`选择应用 CSS 的位置`

* CSS语法结构：选择器 { 属性 : 值; }
  * Property: Value
    * ```css
      color: red;
      ```
* CSS Selector（选择器）：是选择HTML的部分，以便应用花括号之间的任何规则
  * 元素（Element）选择器：选择一个特定的HTML标签
    * 例如： h1, img, body
    * ```css
      h1 {
        color: red;
      }
      ```
  * 类（Class）选择器  - 需要特殊符号`.`：将不同元素分组为一类
    * 在HTML中，HTML标签包含 class=" "
      * ```html
        <h2 class="red-text">Red heading</h2>
        <p class="red-text">Red paragraph</p>html
        ```
    * 在CSS中，选择类时，在前面加一个 .
      * .class\_identifier { 属性 : 值; }
      * ```css
        .red-text {
          color: red;
        }
        ```
  * ID选择器 - 需要特殊符号`#`：
    * 在HTML中，HTML标签包含 id=" "
      * 在CSS中，选择ID时，在前面加一个 #
        * \#id\_identifier { 属性 : 值; }
  * ID vs 类选择器
    * ID - 只用于想修改单个HTML标签的样式
      * 每个HTML文件只能有一个特定的 id\_identifier
      * Class - 用于一组HTML标签，以便为该组提供一致的样式
        * 一个HTML标签可以有多个类
  * 属性（Attribute）选择器：选择具有特定属性/**Value**(**属性值**)的元素
    * 能让你在复杂的 HTML 结构中更精确地选择元素，特别适合根据属性条件应用样式，例如 `target`、`href`、`title`、`type` 等。
    *   #### 1. 基本属性选择器

        选择带有某个属性的元素，不考虑属性值。

        ```css
        css
        /* 选择所有带有 `title` 属性的元素 */
        [title] {
          color: blue;
        }
        ```

        **示例：**

        ```html
        html
        <p title="hello">带有 title 属性的段落。</p>
        <p>没有 title 属性的段落。</p>
        ```
    *   #### 2. 精确匹配属性值

        选择属性值**完全匹配**的元素。

        ```css
        css
        /* 选择所有 `type` 为 `button` 的输入元素 */
        input[type="button"] {
          background-color: #4caf50;
          color: white;
        }
        ```

        **示例：**

        ```html
        html
        <input type="button" value="点击我">
        <input type="text" placeholder="输入文本">
        ```
    *   #### 3. 包含值的属性选择器 (`*=`)

        选择属性值中**包含某个子字符串**的元素。

        ```css
        css
        /* 选择 `title` 中包含 `hello` 的元素 */
        [title*="hello"] {
          font-weight: bold;
        }
        ```

        **示例：**

        ```html
        html
        <p title="say hello">包含 'hello' 的段落。</p>
        <p title="greetings">不包含 'hello' 的段落。</p>
        ```
    *   #### 4. 以某个值开头的属性选择器 (`^=`)

        选择属性值**以某个字符串开头**的元素。

        ```css
        css
        /* 选择 `href` 以 `https` 开头的链接 */
        a[href^="https"] {
          color: green;
        }
        ```

        **示例：**

        ```html
        html
        <a href="https://example.com">安全链接</a>
        <a href="http://example.com">非安全链接</a>
        ```
    *   #### 5. 以某个值结尾的属性选择器 (`$=`)

        选择属性值**以某个字符串结尾**的元素。

        ```css
        css
        /* 选择 `src` 以 `.jpg` 结尾的图片 */
        img[src$=".jpg"] {
          border: 2px solid #000;
        }
        ```

        **示例：**

        ```html
        html
        <img src="photo.jpg" alt="图片">
        <img src="image.png" alt="图片">
        ```
    *   #### 6. 匹配空格分隔的值 (`~=`)

        选择属性值中**包含完整单词**的元素。

        ```css
        css
        /* 选择包含 `button` 类的元素 */
        [class~="button"] {
          padding: 10px;
        }
        ```

        **示例：**

        ```html
        html
        <div class="button primary">按钮样式</div>
        <div class="primary">普通样式</div>
        ```
    *   #### 7. 匹配用连字符分隔的值 (`|=`)

        选择属性值中**以某个字符串开头，并且后面跟着连字符或为空**的元素。

        ```css
        css
        /* 选择 `lang` 属性为 `en` 或 `en-US` 的元素 */
        [lang|="en"] {
          font-style: italic;
        }
        ```

        **示例：**

        ```html
        html
        <p lang="en">This is in English.</p>
        <p lang="en-US">This is in American English.</p>
        <p lang="fr">Ceci est en français.</p>
        ```

        #### 属性选择器的优先级

        * 属性选择器的优先级与类选择器相同（优先级为 **0, 1, 0**）。
          * 如果同时使用 `id`、类选择器、伪类等，优先级会根据标准规则决定。
  * 通用（Universal）选择器
    *   &#x20;CSS 中的一个选择器，用于选择文档中**所有的元素**。通用选择器使用星号（`*`）表示，简单且功能强大，可以用于为整个页面设定默认样式或进行全局操作。

        #### 基本用法

        ```css
        * {
          margin: 0;
          padding: 0;
        }
        ```

        这段代码会将页面上所有元素的 `margin` 和 `padding` 设置为 `0`，通常用于**CSS 重置**，确保不同浏览器的默认样式一致。

        #### 常见用途

        1.  **CSS 重置**：通过设置全局的 `margin` 和 `padding` 为 `0`，可以避免浏览器默认样式对页面布局的影响。

            ```css
            * {
              margin: 0;
              padding: 0;
              box-sizing: border-box;
            }
            ```

            使用 `box-sizing: border-box` 让元素的宽度和高度包含 `padding` 和 `border`，便于布局。

            1.  **默认字体、颜色设置**：可以用通用选择器设置整个页面的默认字体或颜色。

                ```css
                * {
                  font-family: Arial, sans-serif;
                  color: #333;
                }
                ```
            2.  **全局动画效果**：为所有元素添加过渡效果，常用于页面的动画。

                ```css
                * {
                  transition: all 0.3s ease;
                }
                ```
            3.  **特定范围内的全局样式**：可以结合其他选择器，用通配符选择某个范围内的所有元素。例如，在 `#container` 元素内应用默认样式。

                ```css
                #container * {
                  color: #555;
                  font-size: 16px;
                }
                ```

        #### 性能注意事项

        * **高性能需求场景中谨慎使用**：因为通用选择器会作用于页面中的所有元素，可能会影响页面渲染速度。通常建议在小范围或初始化样式时使用。
        * **结合其他选择器**：将通用选择器与其他选择器（如类或 `id`）结合使用，可以限定应用范围，减少性能负担。例如：`.card *` 或 `#main-content *`。

        #### 示例：通用选择器的使用

        ```html
        <!DOCTYPE html>
        <html lang="en">
        <head>
          <meta charset="UTF-8">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>通用选择器示例</title>
          <style>
            /* 使用通用选择器进行 CSS 重置 */
            * {
              margin: 0;
              padding: 0;
              box-sizing: border-box;
            }

            /* 限定范围内的通用选择器 */
            .container * {
              font-family: Arial, sans-serif;
              color: #333;
            }

            /* 全局设置的默认背景色 */
            * {
              background-color: #f9f9f9;
            }
          </style>
        </head>
        <body>
          <div class="container">
            <h1>标题</h1>
            <p>这是段落内容，带有通用选择器设置的样式。</p>
          </div>
        </body>
        </html>
        ```

        #### 总结

        | 使用场景      | 示例                     | 说明           |
        | --------- | ---------------------- | ------------ |
        | 全局重置      | `* { margin: 0; }`     | 初始化所有元素的默认样式 |
        | 全局默认设置    | `* { color: #333; }`   | 设置默认字体颜色、大小等 |
        | 限定范围的通用样式 | `.container * { ... }` | 在特定范围应用全局样式  |

        **通用选择器**适用于全局设置，但需要在性能和需求之间权衡，避免不必要的渲染负担。

### ★  \[项目] 颜色词汇网站

`学习西班牙语的网站`&#x20;

<figure><img src="../.gitbook/assets/goal (2).png" alt=""><figcaption></figcaption></figure>

```html
<!-- 
TODOs
重要提示：**不需要对 index.html 文件做任何修改**
所有的代码都应写在你的 CSS 文件中。

1. 创建一个 CSS 文件，并将其作为外部样式表引入。
2. 使用 CSS 为每个颜色标题设置样式，使其符合颜色含义。
   提示：如果不理解西班牙语单词，可以利用元素的 id 辅助判断。
3. 使用 CSS 将所有颜色标题的字体样式改为 "font-weight: normal;"。
4. 使用 CSS（而非 HTML）将所有图片的高度和宽度设置为 200px。
   提示：
   https://developer.mozilla.org/en-US/docs/Web/CSS/height
   https://developer.mozilla.org/en-US/docs/Web/CSS/width
-->
```

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Spanish Vocabulary</title>
  <link rel="stylesheet" href="./style.css" />
</head>

<body>
  <h1>Colors</h1>
  <h2>Learn the colors in Spanish!</h2>
  <h2 class="color-title" id="red">Rojo</h2>
  <img class="color" src="./assets/images/red.png" alt="red" />

  <h2 class="color-title" id="blue">Azul</h2>
  <img src="./assets/images/blue.png" alt="blue" />

  <h2 class="color-title" id="orange">Anaranjado</h2>
  <img src="./assets/images/orange.png" alt="orange" />

  <h2 class="color-title" id="green">Verde</h2>
  <img src="./assets/images/green.png" alt="green" />

  <h2 class="color-title" id="yellow">Amarillo</h2>
  <img src="./assets/images/yellow.png" alt="yellow" />
</body>

</html>
```

```css
/* 设置所有图片的尺寸 */
img {
  height: 200px; /* 图片高度为 200 像素 */
  width: 200px;  /* 图片宽度为 200 像素 */
}

/* .color-title 类样式 */
/* 适用于所有 class 为 "color-title" 的 <h2> 元素 */
.color-title {
  font-weight: normal; /* 设置字体为正常粗细（非默认粗体） */
}

/* 特定颜色的样式设置 */
/* 为每种颜色的 <h2> 标题设置对应的文本颜色 */

/* 红色标题 "Rojo" */
#red {
  color: red; /* 文本颜色为红色 */
}

/* 蓝色标题 "Azul" */
#blue {
  color: blue; /* 文本颜色为蓝色 */
}

/* 橙色标题 "Anaranjado" */
#orange {
  color: orange; /* 文本颜色为橙色 */
}

/* 绿色标题 "Verde" */
#green {
  color: green; /* 文本颜色为绿色 */
}

/* 黄色标题 "Amarillo" */
#yellow {
  color: yellow; /* 文本颜色为黄色 */
}
```
