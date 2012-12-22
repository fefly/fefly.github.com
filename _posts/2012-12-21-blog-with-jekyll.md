---
layout: post
title: "如何利用github快速创建个人博客"
description: "如何利用github快速创建个人博客"
category:
 - 前端工具
tags: [tools, 教程, Jekyll, blog]
---
{% include JB/setup %}


##一、开通网站
1. 登录github.com，有帐号的登录，无帐号的注册 [https://github.com/][17]
2. Fork项目jekyll-bootstrap（[https://github.com/plusjade/jekyll-bootstrap][15]）<br>![fork][1]
3. 进入setting，重命名项目名为 xxx.github.com（xxx是你在github注册的用户名）<br>![setting][2]<br>![rename][3]
4. 访问你的网站 xxx.github.com，恭喜你，现在你已经有了自己的网站，完全免费的。

##二、配置网站
找到_config.yml，点击右上角的edit，找到并修改以下内容，以下（）中的为说明文字，请不要放到文件中去：<br>
{% highlight text %}
......
title : Jekyll（你的网站名）
tagline: Jekyll your Site（你的网站slogan）
author :
  name : Jekyll（你的名字）
  email : Jekyll@Jekyll.com（你的邮件）
  github : Jekyll（你的github帐号）
  twitter : Jekyll
  feedburner : Jekyll
......
production_url : http://username.github.com（你的网站地址，可添加cname文件绑定域名）
......
comments :
  provider : disqus（利用第三方的留言系统，请登录[http://disqus.com/][14]，注册帐号之后，注册一下刚才开通的网站，表单中有一个Shortname的字段）
  disqus :
    short_name : jekyllbootstrap（这里填你在上一步填写Shortname）
......
analytics :
  provider : google （利用google提供的统计代码，在google统计帐号里添加刚才开通的网站）
  google : 
      tracking_id : 'UA-xxx-xxx'（这里填上一步生成的ID号）
......
{% endhighlight %}<br>![edit][4]

##三、修改文章模版
1. 修改首页，找到根目录下的index.md文件，点击右上角的edit，以下（）中的为说明文字，请不要放到文件中去。<br>![home][9] 
2. 文章很多需要翻页的时候可以用这个项目的分页代码 [https://github.com/mojombo/jekyll/wiki/Pagination][16]
3. 修改tagline，文章页面的标题后面会跟一个Supporting tagline<br><br>![tagline][10] <br>
   找到这个文件_includes/themes/twitter/post.html，将原来的![tagline][18] 改成![tagline][19]

##四、发布文章
1. 所有的都放在_posts下，是md后缀的markdown文件，可以点击文件路径后面的加号新增文件<br>![addapost][5]
2. 文件名以为时间开头，年月日用中划线分隔，后接标题，标题中的空格用中划线代替<br>文件内容包括2部分：元数据和文章正文<br>![layout][8]
3. 文章内容为[markdown格式][6]，语法简单，上手快
4. 文章写好之后，点击Commit New File按钮，网站马上就会更新。<br>
![post][7]


##五、定制页面内容
1.每个页面是一个对象，里面包含页面相关的各种数据，比如文章的标题，直接在页面输出![title][11]即可；
2.所有的数据都存在一个大的对象里面，任何页面都可以获取对象里的数据，比如全站文章按目录分类的数据![cats][12]；
3.具体可以查看官方文档 [http://jekyllbootstrap.com/api/template-data-api.html][13]

<br><br>
##一个能够正常发文的博客网站就这样搞定了，后面的高级定制功能在github的网站上点击实现比较麻烦，需要按照客户端或者命令行工具。
<br><br>


##六、个性化网站 换肤等
1. 预览各种皮肤效果，目前有7个可以预览[http://themes.jekyllbootstrap.com/][20]
2. 找到你想要的皮肤的代码，预览的时候会有一个install theme的按钮，点击之后会出来一个类似的地址git://github.com/sodabrew/theme-dinky.git
3. 把皮肤中的模版文件目录部署到_includes/themes/xxx（xxx为皮肤名），相关的静态资源部署到assets/themes/xxx
4. 启用新的皮肤，找到_layouts/default.html，把theme name改成xxx
<br>{% highlight text %}
theme :
  name : twitter（twitter改成新的xxx）
{% endhighlight %}
<br><br>

[1]: http://fefly.github.com/content/20121221/fork.png
[2]: http://fefly.github.com/content/20121221/setting.png
[3]: http://fefly.github.com/content/20121221/rename.png
[4]: http://fefly.github.com/content/20121221/edit.png
[5]: http://fefly.github.com/content/20121221/addpost.png
[6]: http://wowubuntu.com/markdown/
[7]: http://fefly.github.com/content/20121221/post.png
[8]: http://fefly.github.com/content/20121221/layout.png
[9]: http://fefly.github.com/content/20121221/home.png
[10]: http://fefly.github.com/content/20121221/tagline.png
[11]: http://fefly.github.com/content/20121221/title.png
[12]: http://fefly.github.com/content/20121221/cats.png
[13]: http://jekyllbootstrap.com/api/template-data-api.html
[14]: http://disqus.com/
[15]: https://github.com/plusjade/jekyll-bootstrap
[16]: https://github.com/mojombo/jekyll/wiki/Pagination
[17]: https://github.com/
[18]: http://fefly.github.com/content/20121221/tagi.png
[19]: http://fefly.github.com/content/20121221/tagii.png
[20]: http://themes.jekyllbootstrap.com/
