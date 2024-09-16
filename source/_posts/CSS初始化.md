---
title: CSS初始化
date: 2024-06-15 12:00:00
aside: true
top_img: true
type: web
# cover: "/img/images/调色/d2.png"
---

# CSS初始化

CSS初始化（CSS Reset）是一种常见的做法，通过将浏览器的默认样式重置为一个一致的基准，来确保在不同浏览器中呈现的网页内容具有一致性。不同浏览器对HTML元素有各自的默认样式，这些默认样式之间可能存在差异，从而导致在不同浏览器中显示时出现不一致的情况。

以下是进行CSS初始化的一些主要原因：

1. **跨浏览器一致性**：不同浏览器对一些HTML元素（如标题、段落、列表等）有不同的默认样式，通过CSS初始化可以使这些默认样式统一，从而在所有浏览器中呈现一致的外观。

2. **消除默认边距和填充**：许多HTML元素（如`<body>`、`<h1>`至`<h6>`、`<p>`、`<ul>`和`<ol>`等）在默认情况下会有边距和填充，通过CSS初始化将它们清零，可以更容易地控制和定义自己的样式。

3. **简化样式管理**：通过重置默认样式，开发者可以从一个已知的、更可控的基准开始设计和编写自己的样式，而不需要先去研究和覆盖浏览器默认的样式。

4. **避免意外的样式冲突**：有些默认样式可能会与自定义样式发生冲突，导致意想不到的显示问题。初始化可以帮助减少此类问题。

5. 举例：

   ```css
   /* 把我们所有标签的内外边距清零 */
   * {
       margin: 0;
       padding: 0
   }
    
   /* em 和 i 斜体的文字不倾斜 */
   em,
   i {
       font-style: normal
   }
    
   /* 去掉 li 的小圆点 */
   li {
       list-style: none
   }
    
   img {
       /* border 0 照顾低版本浏览器，如果图片外面包含了链接会有边框的问题 */
       border: 0;
       /* 取消图片底侧有空白缝隙的问题 */
       vertical-align: middle
   }
    
   button {
       /* 当我们鼠标经过 button 按钮的时候，鼠标变成小手 */
       cursor: pointer
   }
    
   a {
       color: #666;
       text-decoration: none
   }
    
   a:hover {
       color: #c81623
   }
    
   button,
   input {
       /* "\5B8B\4F53" 就是宋体的意思，这样浏览器兼容性比较好 */
       font-family: Microsoft YaHei, Heiti SC, tahoma, arial, Hiragino Sans GB, "\5B8B\4F53", sans-serif
   }
    
   body {
       /* CSS3 抗锯齿形，让文字显示的更加清晰 */
       -webkit-font-smoothing: antialiased;
       background-color: #fff;
       font: 12px/1.5 Microsoft YaHei, Heiti SC, tahoma, arial, Hiragino Sans GB, "\5B8B\4F53", sans-serif;
       color: #666
   }
    
   .hide,
   .none {
       display: none
   }
    
   /* 清除浮动 */
   .clearfix:after {
       visibility: hidden;
       clear: both;
       display: block;
       content: ".";
       height: 0
   }
    
   .clearfix {
       *zoom: 1
   }
   ```

   

> 标　　题：CSS初始化
> 作　　者：皮喆
> 出　　处：https://blog.kunkun.cool/2024/06/15/CSS%E5%88%9D%E5%A7%8B%E5%8C%96/
> 创建时间：2024-06-15 12:00:00
> 关于博主：坐标郑州，喜欢折腾各种东西的工程师，如有问题探讨可以直接下方留言。
> 声援博主：如果您觉得文章对您有帮助，可以评论、订阅、收藏。您的鼓励是博主的最大动力！
