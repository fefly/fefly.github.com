---
layout: post
title: "Media Query在IE低版本(ie<9)的简单实现"
description: "Media Query在IE低版本(ie<9)的简单实现"
category:
 - 真操实战
tags: [真操实战]
---
{% include JB/setup %}

###思路梳理：

####1、在css文件中用注释内容作为钩子
@media screen and (min-width:600px) {
/*mediaMin600*/
.box{background:purple;}
/*mediaMin600*/
}

####2、在js中利用注释，通过split获取各个范围的css内容
xxx.split("/*mediaMin600*/")[1];

####3、根据当前窗口的范围，动态添加上一步获取的对应的css内容到页面。
var _cw = document.documentElement.clientWidth || document.body.clientWidth;
...
if(_cw>600){ css.styleSheet.cssText = _mqs.mediaMin600; }
...


###说明：
<ul>
<li>此方法需要手动调整的参数比较多，但是逻辑比较简单，不需要像css3-mediaqueries-js一样去遍历和重新解析所有相关的CSS代码。
<li>关于media query特性的支持，除了ie9以下的浏览器，大部分现代浏览器都支持，所以才有了demo中的代码逻辑，关于这个特性的检测可以参考paulirish写的matchMedia.js。
<li>window.resize可能会导致ie6奔溃，设置延时来解决；ie6下获取style标签的innerHTML有问题，刷新页面之后正常、在style前面添加script标签也会正常，原因搜寻中。。。
</ul>
