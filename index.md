---
layout: page
title: Welcome to wqqgt Page
tagline: Supporting tagline
---
{% include JB/setup %}

## 历史背景

这个网站受益于jekyll和github,所有文章都是自己的理解，如果有不对的地方，欢迎指正   
联系方式:   
邮箱wangguo0315@163.com   
QQ:451810304    

## 最近的更新文档

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


