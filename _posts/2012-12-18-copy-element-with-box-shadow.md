---
layout: post
title: "如何利用CSS3的box-shadow属性复制元素"
description: "如何利用CSS3的box-shadow属性复制元素"
category:
 - 真操实战
tags: [css, css3, 真操实战]
---
{% include JB/setup %}

研究过css3的同学都知道box-shadow可是设置多组值，出来多个阴影，利用这个特性，我们可以把一个元素(通常情况下是各种纯色的形状)，复制出多个来，而不用添加额外的标签，直接看代码。

{% highlight css %}
<style type="text/css">  
.circle{    
    width: 100px;    
    height: 100px;    
    background-color: #ccc;    
    border-radius: 50px;    
    box-shadow: 202px 50px 0 31px #f00,  
    101px 134px 0 0px #0f0,  
    109px 212px 0 -33px #00f;  
}    
</style>  
<div class="circle"></div> 
{% endhighlight %}

![copy circle][1]


看了这个之后，那个经典的菊花是不是可以很快的搞定了呢？

* 上面的box-shadow中的第一、二、三、五个参数大家经常用，分别是x轴偏离、y轴偏离、模糊半径、阴影颜色。
* 而第四个参数[spread-radius]是可选的，很少被大家注意到，这个参数可以用来控制阴影的大小：正数则在元素的尺寸基础上增大、负数缩小。
* 贴上完整的参数：{% highlight css %}box-shadow:  none | [inset? && [ <offset-x> <offset-y> <blur-radius>? <spread-radius>? <color>? ] ]{% endhighlight %}


####参考资料：
* box-shadow生成器：http://box-shadow.info/
* 一个标签搞定Loading：http://one-div.com/pictos/ajax-loader/

[1]: http://fefly.github.com/content/20121218/copy-dot.png "copy-dot.png"
