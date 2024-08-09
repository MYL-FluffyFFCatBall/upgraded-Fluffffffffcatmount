---
layout: post
title: "建立个人博客时遇到的问题"
date: 2024-08-09
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
但实际上**没有列表显示**。

问题排查：
- 目录下没有 _layouts 文件夹。*加入该文件夹后 theme:minimal 被覆盖了
  确认：github 自动加载了 minimal 的配置文件。

⭐确认原因：博文中 date 字段格式错误，导致无法正常加载。
- 正确的 date 格式： `date: 2024-08-09`

**上述代码生成的 url 指向不存在的 .html 文件**

问题排查：
- 检查配置：permalink
- 没有 _site 文件夹被生成
