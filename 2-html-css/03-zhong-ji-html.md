# 03 – 中级 HTML

### ★列表元素（List）

[`有序列表`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)和[`无序列表`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)

* [BuzzFeed](https://www.buzzfeed.com/alexandranapoli/things-that-must-have-been-designed-by-geniuses-717?new\_user=true\&newsletter\_modal=true)
* [十大通缉犯 — FBI](https://www.fbi.gov/wanted/topten)
* Unordered List（无序列表）
  * \<ul>\</ul>
    * 列表项（List items）
      * \<li>\</li>（项目符号）
* Ordered List（有序列表）
  * \<ol>\</ol>
    * 列表项（List items）
      * \<li>\</li>（数字）

### ★嵌套和缩进（Nesting and Indentation）

`如何编写好的代码`

可以通过嵌套和缩进来找出问题所在：

```html
<ul>
  <li>A</li>
  <li>
    B
    <ol>
      <li>B1</li>
      <li>
        B2
        <ul>
          <li>
            B2a
            <ul>
              <li>B2aa</li>
              <li>B2ab</li>
            </ul>
          </li>
          <li>B2b</li>
          <li>B2c</li>
        </ul>
      </li>
      <li>
        B3
        <ol>
          <li>B31</li>
          <li>B32</li>
        </ol>
      </li>
    </ol>
  </li>
  <li>C</li>
</ul>
```

### ★[锚点元素（Anchor）](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)

`理解HTML属性`

* HyperLink（超链接）
* 属性之间用空格隔开\<tag attribute=value anotherattribute=value>
  * [`href`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#href): 链接的URL
  * [全局属性](https://developer.mozilla.org/en-US/docs/Web/HTML/Global\_attributes)
    * [`draggable`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global\_attributes/draggable)
    * ...
* 灵感
  * [Product Hunt——科技领域最好的新产品](https://www.producthunt.com/)
  * [Smash The Walls](https://smashthewalls.com/)
  * [Wordle - 纽约时报](https://www.nytimes.com/games/wordle/index.html)
  * [Hacker Typer：伪造编码和黑客模拟器来恶作剧和戏弄你的朋友](https://hackertyper.com/)
  * [Stellarium Web 在线星图](https://stellarium-web.org/)

### ★图像元素（Image）

`将图像添加到我们的网站`

* <mark style="color:red;">\<img /></mark>
* [`src`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img#src):
  * 可以是互联网上的图片URL
  * 可以是页面目录路径中的本地文件
* [`alt`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLImageElement/alt#usage\_notes): 替代文字描述
  * 如果src无法获取图片用于渲染，则显示替代文本
  * 插件：[Silktide 无障碍检查器 - Chrome 网上应用店](https://chromewebstore.google.com/detail/silktide-accessibility-ch/mpobacholfblmnpnfbiomjkecoojakah)

### ★生日邀请项目

`为您下个派对创建网站`

<figure><img src="../.gitbook/assets/goal (7).png" alt=""><figcaption></figcaption></figure>

```html
<!-- 这是一个可能的解决方案 -->
<h1>It's My Birthday!</h1>
<h2>On the 12th May</h2>

<img src="https://raw.githubusercontent.com/appbrewery/webdev/main/birthday-cake3.4.jpeg" alt="purple birthday cake with candles" />

<h3>What to bring:</h3>
<ul>
  <li>Baloons (I love baloons)</li>
  <li>Cake (I'm really good at eating)</li>
  <li>An appetite (There will be lots of food)</li>
</ul>

<h3>This is where you need to go:</h3>
<a href="https://www.google.com/maps/@35.7040744,139.5577317,3a,75y,289.6h,87.01t,0.72r/data=!3m6!1e1!3m4!1sgT28ssf0BB2LxZ63JNcL1w!2e0!7i13312!8i6656">Google map link</a>
```
