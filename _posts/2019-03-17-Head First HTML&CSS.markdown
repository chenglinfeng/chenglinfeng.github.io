---

layout: post
title:  "Head First HTML&CSS"
date:   2019-03-17 20:16:40 +0800
categories: jekyll update
---


#### HTML基本结构

```html
<!doctype html>
<html>
    <head>
          <meta charset="utf-8">
          <title>"标题"</title>
    </head>
    <body>
          <h1>"一级标题"</h1>
          <img src="图像.jpg">
          <p>
              段落内容
          </p>
          <h2>"二级标题"</h2>
          <p>
              段落内容
          </p>
    </body>
</html>
```

#### CSS样式

```css
<style type="text/css">
    body{                                            //对正文部分使用样式
                   background-color: #d2b48c     //设置背景颜色
                   margin-left/right: 20%                //左右外边距
                   border: 2px, dotted black           //边框线宽颜色 
                   padding: 10 px                            //内边距
                   font-family:sans-serif                  //字体
   }
</style>
<link type="text/css" rel="stylesheet" href="lounge.css">       //载入CSS
```

#### 超文本

```html
<a href="../directions.html">detail directions</a>    //同一域名下超链接
<h2 id="Coffee">Coffee</h2>          //使用id链接到元素
<a href="http://wickedlysmart.com/buzz/index.html#Coffee"         //不同域名链接
     title="Read all about caffeine on the Buzz">Caffeine Buzz</a>   //所链接页面的文本描述
<a target="_blank" //打开一个新窗口
     href="http://wickedlysmart.com/buzz/index.html"                 
     title="Read all about caffeine on the Buzz">Caffeine Buzz</a>   //所链接页面的文本描述
```

#### 引用

* q

  ```html
  how about <q>To be or not to be</q>, or <q>Where you go, there you are</q>.
  how about "To be or not to be", or "Where you go, there you are".
  ```

  

* blockquate

```html
<blockquote>
    passing cars,<br>
    When you can't see.<br>
</blockquote>
```



#### 没有内容的元素

* img
* br

#### 列表

```html
<ol>   //有序列表  
    <li>John</li>  
    <li>Mary</li>  
    <li>Bob</li>
</ol>
```

输出：

<ol>  
    <li>John</li>  
    <li>Mary</li>  
    <li>Bob</li>
</ol>

#### 图像 jpg/png/gif

```html
<a href="html/pencil.html">       //链接到图像
     <img src="http://wickedlysmart.com/hfhtmlcss/trivia/pencil.png"
              alt="The typical new pencil can draw a line 35 miles long." //图像未显示，文本代替图像
               width="48" height="100">     //宽和高
</a>
```

#### 类

```html
<p class="greentea">
    Green Tea
</p>
p.greentea {
          color: green;
}
```



####  字体

```css
@fontface {
     font-family: "Emblema One"
     src: url("http://wickedlysmart.com/hfhtmlcss/chapter8/journal/EmblemaOne-Regular.woff"),
            url("http://wickedlysmart.com/hfhtmlcss/chapter8/journal/EmblemaOne-Regular.tff");
}
h1 {
    font-family: "Emblema One", sans-serif;
}
```





#### css中的id

```css
<p id="guarantee">
    Our guarantee: ...
</p>
 #guarantee {
    line-height: 1.9em     //行距1.9倍
}
```



####  同一个css适应多种设备类型（PC、mobile、印刷版本）

* 根据media属性使用适合于指定设备的样式文件

```css
<link href="lounge-mobile.css" rel="stylesheet" media="screen and (max-device-width: 480px)">
<link href="lounge-print.css" rel="stylesheet" media="print>
```

* 或者直接在CSS中增加媒体查询

```css
@media screen and (max-device-width: 480px) {
    #guarantee {
          margin-right: 250px;
    }
}
@media screen and (min-device-width: 481px) {
    #guarantee {
          margin-right: 30px;
    }
}
@media print {
    body {
          font-family: Times, serif;
    }
}
```





#### div 与 span

div容器 ：块元素逻辑分组
span 内联字符和元素的逻辑分组

* 表格布局

```html
<div>
    <div>
         <div>
          ......
          </div>
    </div>
</div>
```



* 绝对布局+float

```html
<header>、<footer>、<aside>、<section>、<article>、<time>、<nav>
<video controls autoplay width="512" height="288"  poster="images/poster.png" id="video">
    <source src="video/tweetsip.mp4">  //safari
    <source src="video/tweetsip.webm>  //chrome、firefox、opera
    <source src="video/tweetsip.ogv>  //chrome、firefox、opera
    <object>...</object>     //flash
</video>
```





#### 实现表格

```html
<table>
    <caption>
         The cities I visited on my Segway'n USA travels     //表名
    </caption>
    <tr>     //行
          <th>City</th>     //第一列名称
          <th>Date</th>     //第二列名称
    </tr>
    <tr>
          <td>Walla Walla</td>     //第一列内容
          <td>June 15th</td>          //第二列内容
    </tr>
</table>
```



#### 远程表单提交（本地表单数据存储可用javascript为submit创建点击函数完成）

```html
<form action="http://wickedlysmart.com/hfhtmlcss/content.php"
            method="post">
    <p>
         Just type in your name to enter the contest: <br>
         First name: <input type="text" name="firstname" value=""> <br>
         Last name: <input type="text" name="lastname" value=""> <br>
      <input type="submit">

    </p>

</form>

```

![](https://raw.githubusercontent.com/chenglinfeng/chenglinfeng.github.io/master/my_pics/2019-03-17-Head%20First%20HTML%26CSS-pic1.png)



```html
<input type="radio/checkbox/number/range" > </input>
<textarea> </textarea> //文本区
<select> </select> //选择框
```





#### 脚本

```html
<script src="lounge.js或者http://maps.google.com/maps/api/js?sensor=true"> </script>
```



#### js通信api

```html
<script src="http://gumball.wickedlysmart.com/?callback=updateSales"> </scripts> //web服务把返回数据包装在updateSales函数调用中
function updateSales(sales) {     //返回js对象sales
     ...
}
```



#### 画布

```html
<canvas id="tshirtCanvas"> ... </canvas>

var canvas = document.getElementById("tshirtCanvas");
var content = canvas.getContext("2d");
context.fillRect(10,10,100,100);  //在画布上画矩形
```

