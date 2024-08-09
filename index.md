---
layout: default
title:  "Home"
---
this is an index file. to implement.

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
      <small>{{ post.date | date: "%Y-%m-%d" }}</small>
    </li>
  {% endfor %}
</ul>

end file
