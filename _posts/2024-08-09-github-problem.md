---
layout: post
title: "建立个人博客时遇到的问题"
date: 2024-08-09 12:00:00 +0000
---
在 posts 文件夹中加了 .md 文件，index.md 中写了以下内容：
```
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%Y-%m-%d" }}</small>
    </li>
  {% endfor %}
</ul>
```
但实际上没有列表显示。

问题排查：
- 目录下没有 _layouts 文件夹。*加入该文件夹后 theme:minimal 被覆盖了
