# 07 – 中级 CSS

### ★The Cascade - Specificity and Inheritance 层叠 - 特指性与继承

`如何解决竞争样式`

* Cascading：只有当我们考虑多个不同的冲突CSS规则时Cascading才有意义
  * 这种确定哪些规则真正得到应用、哪些规则被忽略的方法是我们的级联是如何形成的
  *   一旦完成级联：

      <div align="left">

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-16 at 19.58.54.png" alt="" width="375"><figcaption></figcaption></figure>

      </div>
*   确定总体重要性时，我们会考虑四大类：位置、特异性、类型、重要性。\
    每个级联中几乎都有一个迷你级联级别，你可以确定哪一个时重要的？

    <figure><img src="../.gitbook/assets/Screenshot 2024-11-16 at 20.15.46.png" alt=""><figcaption></figcaption></figure>
*   goal

    <figure><img src="../.gitbook/assets/goal (1).png" alt=""><figcaption></figcaption></figure>
*   css

    ```css
    #outer-box {
      background-color: purple;
    }

    .box {
      background-color: blue;
      padding: 10px;
    }

    .inner-box {
      background-color: red;
    }

    p {
      color: yellow;
      margin: 0;
      padding: 0;
    }

    .white-text {
      color: white;
    }
    ```
*   html

    ```html
    <!DOCTYPE html>
    <html lang="en">

    <head>
      <meta charset="UTF-8">
      <title>CSS Cascade</title>
      <link rel="stylesheet" href="./solution.css">
    </head>
    <body>
      <div id="outer-box">
        <div class="box">
          <p>Yellow Text</p>
          <div class="box inner-box">
            <p class="white-text">White Text</p>
          </div>
        </div>
        <div class="box">
          <p>Yellow Text</p>
          <div class="box inner-box">
            <p class="white-text">White Text</p>
          </div>
        </div>
      </div>
    </body>

    </html>
    ```

### ★Combining CSS Selectors 组合CSS选择器

`如何选择特定元素进行样式设置`

*

    <figure><img src="../.gitbook/assets/Screenshot 2024-11-17 at 21.58.33.png" alt=""><figcaption></figcaption></figure>
* 一些规则：
  *   组（Group）：使用`,`隔开

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-17 at 22.02.48.png" alt=""><figcaption></figcaption></figure>
  *   子项（Child）：使用`>`来选择另一个选择器的子项

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-17 at 22.09.09.png" alt=""><figcaption></figcaption></figure>
  *   后代（Descendant）：

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-17 at 22.17.27.png" alt=""><figcaption></figcaption></figure>
  *   链接（Chaining）：

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-17 at 22.27.51.png" alt=""><figcaption></figcaption></figure>
  *   组合组合器（Combining Combiners）：

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-17 at 22.32.20.png" alt=""><figcaption></figcaption></figure>

### ★CSS Positioning CSS定位

`相对（Relative）、绝对（Absolute）、固定（Fixed）和静态（Static）定位`

*   [CSS Positioning Demo](https://appbrewery.github.io/css-positioning/)

    <figure><img src="../.gitbook/assets/Screenshot 2024-11-18 at 19.32.56.png" alt=""><figcaption></figcaption></figure>
* [Pesticide for Chrome - Chrome Web Store](https://chromewebstore.google.com/detail/pesticide-for-chrome/bakpbgckdnepkmkeaiomhmfcnejndkbi?hl=en)
* 静态定位（Static Positioning）- `HTML的默认流动性`
  *   无论添加任何属性，它都不会执行任何操作

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-18 at 19.47.02.png" alt=""><figcaption></figcaption></figure>
* 相对定位（Relative Positioning）- `相对于默认位置定位`&#x20;
  * 1![](<../.gitbook/assets/Screenshot 2024-11-18 at 19.49.43.png>)
  *

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-18 at 19.49.00.png" alt=""><figcaption></figcaption></figure>
* 绝对定位（Absolute Positioning）- `相对于最近的定位祖先元素或网页左上角定位`&#x20;
  *   Z轴索引 `z-index` （默认z-index: 0），当你设置Absolute时，即使z-index: 0，它实际上会把元素取出来，并将其放在另一层上

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-18 at 19.59.29.png" alt=""><figcaption></figcaption></figure>
* 固定定位（Fixed Positioning）- `相对于浏览器窗口左上角定位`&#x20;
  * 即使你在网页上上下滚动，它仍会相对于浏览器位于相同的位置
  *

      <figure><img src="../.gitbook/assets/Screenshot 2024-11-18 at 20.10.29.png" alt=""><figcaption></figcaption></figure>
  *

      <figure><img src="../.gitbook/assets/goal.png" alt=""><figcaption></figcaption></figure>
  *

      ```html
      <!DOCTYPE html>
      <html>

      <head>
        <title>CSS Positioning Exercise</title>
        <style>
          .red-circle {
            width: 200px;
            height: 200px;
            background-color: red;
            border-radius: 50%;
            position: absolute;
            top: 150px;
            left: 250px;
          }
          
          .blue-box {
            background-color: blue;
            width: 500px;
            height: 300px;
            position: relative;
            top: 200px;
            left: 200px;
          }

        </style>
      </head>

      <body>
        <div class="blue-box">
          <div class="red-circle"></div>
        </div>
      </body>

      </html>
      ```

### ★\[Project] CSS Flag \[项目] CSS旗帜

`用CSS制作老挝国旗`



