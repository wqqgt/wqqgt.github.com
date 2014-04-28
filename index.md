---
layout: page
title: Welcome to wqqgt Page
tagline: Supporting tagline
---
{% include JB/setup %}

## 历史背景

这个网站受益于jekyll和github,所以把这两个文档放到这个上面

Read [Jekyll Quick Start](http://jekyllbootstrap.com/usage/jekyll-quick-start.html)

Complete usage and documentation available at: [Jekyll Bootstrap](http://jekyllbootstrap.com)
    
## 最近的更新文档

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


