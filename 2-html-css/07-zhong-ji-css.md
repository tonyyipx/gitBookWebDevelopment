# 07 – 中级 CSS

### ★





### 中级CSS

* \<div>
  * 将一组HTML元素组合成一个盒子
  * 对于组织和划分网页内容非常有用
* \<span>
  * 一个内联元素，可用于选取HTML元素的某个子部分，从而应用样式
* 盒模型 (Box Model)
  * 宽度 (Width)
  * 高度 (Height)
  * 内边距 (Padding)
  * 边框 (Border)
    * 边框大小
    * 实线, 虚线, …
  * 外边距 (Margin)
* 显示属性 (Display Property)
  * 可以修改任何HTML元素的显示属性
    * 例如： display : inline;
  * 块级元素 (Block)
    * 占据一整行，宽度占满整个屏幕
  * 内联元素 (Inline)
  * 内联块 (Inline-Block)
    * 允许其他元素在其左右两侧显示
  * 隐藏 (None)
    * 隐藏HTML元素，像它从未存在过
    * 替代方案： visibility : hidden
      * 元素不可见，但仍占据原始大小的位置
* CSS静态与相对定位
  * 1\. 内容决定一切
  * 2\. 内容的顺序来自代码
  * 3\. Parent - Children 关系
    * 子元素层叠在父元素上
  * 定位 (Position)
    * 改变元素布局位置的四种方法
      * 静态 (Static)
        * 所有HTML元素默认是静态的
      * 相对 (Relative)
        * **相对于静态** 位置进行调整
        * position : static;
        * 仅当改变坐标值时才会看到变化
          * top, bottom, left, right
        * 相对定位独立作用于HTML元素
      * 绝对 (Absolute)
        * **相对于父** 元素进行移动
          * 添加相对于父元素的边距
        * 绝对定位依赖于HTML元素
      * 固定 (Fixed)
        * 即使用户滚动页面，元素也固定在原位
        * 常用于导航栏
* 使用CSS居中元素
  * text-align : center
    * 居中所有没有设置宽度的元素
  * margin : top right bottom left
    * auto - 用于居中元素
* 字体样式
  * font-family
    * serif
    * sans-serif
  * 注意，不同浏览器和操作系统支持的字体有所不同。因此在为网站选择字体时，需考虑用户的可用性。
  * em
    * 例如：
      * font-size: 2rem;
    * 1 em = 16px = 100%
    * 文本的动态尺寸，相对于标准的 16px = 1em
    * 文本的动态尺寸，相对于HTML元素的父级
  * rem
    * 文本的动态尺寸，相对于根元素
    * 优先用于文本
* CSS浮动与清除
  * float
    * HTML元素 “floats”，其他元素可以环绕它
  * clear
    * 与float相反，HTML元素不允许其他元素环绕
