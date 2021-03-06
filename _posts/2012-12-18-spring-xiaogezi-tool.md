---
layout: post
title: "Spring——批量压缩CSS、图片、代码，批量重命名"
description: "Spring——批量压缩CSS、图片、代码，批量重命名"
category:
 - 前端工具
tags: [tools, 前端工具]
---
{% include JB/setup %}


### 关于 Spring

[Spring][1]是[小鸽子][2]开发的一个给前端开发人员用的工具，用于批量压缩CSS、图片、代码以及批量重命名。

![spring][3]

### 下载Spring

Download: <https://github.com/Linrstudio/Spring/downloads>

### 操作方法

#### 添加文件:
您可以通过以下二种方式添加文件：
<ul>
<li>双击容器空白处添加文件；</li>
<li>从桌面拖入文件到拖拽区域；</li>
<li>您还可以将压缩的文件列表保存为.spring 文件，使用Ctrl+O 打开；</li>
</ul>

#### 设置压缩选项设置输出位置:
<ul>
<li>您可以在“输出到”文本框里设置输出的目标文件夹；</li>
<li>为空时，将在文件所在目录创建_min 文件夹，用来保存压缩过后的文件；</li>
<li>为空且“输出选项”->“在同目录生成.min.css”勾选时，将在文件所在目录生成xxx.min.css</li>
<li>您可以勾选“为 CDN”添加时间戳功能；</li>
</ul>

#### 压缩说明：
<ul>
<li>目前仅对 png、jpg 图片格式进行压缩</li>
<li>图片压缩完后，可以点击 “对比图片”，可视化对比，压缩前后的情况；</li>
<li>CSS、JS 使用的压缩方案： YUI Compressor</li>
<li>在“压缩”按钮上点击鼠标右键，则不压缩，仅对 CSS 文件进行勾选的应用（例如仅中文字体编码、添加时间戳）</li>
</ul>

#### 压缩CSS、JS代码
<ul>
<li>您可以将 CSS 代码 粘贴到 代码区域，并选择压缩类型进行压缩；</li>
</ul>

#### 快速运行源代码
<ul>
<li>您可以将 HTML 代码 粘贴到 代码区域，并点击 “运行HTML”；</li>
<li>您也可以直接在“运行HTML” 按钮上点击鼠标右键，快速预览剪贴板中的 HTML 代码；</li>
</ul>

#### 批量重命名
<ul>
<li>支持 普通/正则 查找替换文件名，默认先备份文件，再处理文件；</li>
<li>使用 正则替换 文件名时，在替换成文本框中输入 $1 代表匹配的文本；</li>
</ul>

#### 项目管理
<ul>
<li>Ctrl+S 保存压缩项目；</li>
<li>Ctrl+O 打开压缩项目；</li>
</ul>

#### 快捷操作
<ul>
<li>在 “输出到”文本框点击 右键，将快捷获取 剪贴板中的目录路径；</li>
<li>在 “输出到”文本框双击，弹出选择文件夹对话框；</li>
<li>在 文件选择框中双击 添加文件要压缩的文件。</li>
</ul>

[1]: https://github.com/Linrstudio/Spring/
[2]: http://xiaogezi.cn/
[3]: http://fefly.github.com/content/20121218/spring.png