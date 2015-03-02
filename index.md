---
layout: page
title: WQQGT BLOG
tagline: If you do not think about your future, you cannot have one.– John Galsworthy
---
{% include JB/setup %}

## 历史背景
关于图册浏览的问题和建议，请加群219464081   
大家可以讨论需要什么功能，还有需要什么地方改进等  

## 最近的更新文档

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


