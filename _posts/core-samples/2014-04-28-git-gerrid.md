---
layout: post
category : lessons
tagline: "Supporting tagline"
tags : [intro, beginner, jekyll, tutorial]
---
{% include JB/setup %}

## Overview

### 为什么需要版本管理？

在公司的开发中，总也离不开版本仓库的管理。有的用svn，有的用git，当然还有其他的。
如果个人开发，需要版本管理吗？我的回答是需要。版本管理主要可以干什么呢？协同开发&&同步备份
我认为这两个是核心功能，目前大部分的版本管理软件都支持这两个。我重点向表述一下协同开发中
使用git来管理版本的问题

### Git 初步管理版本

当年从学校刚毕业到公司工作，大概是2011年初吧，就接触到了Git，当然还有chrome（后面在重点说chrome），
这两个高大上的工具，当时最简单的做法就是用git搭的局域网服务器，采用ssh协议通信。
git clone ssh://[<username>@]<server>:/path/to/repos/myrepo.git  当时采用的是口令认证，每次连接还
需要输入密码


### Git && Gerrit

后来一次机会接触到了(gerrit<https://code.google.com/p/gerrit/>),这个东西竟然可以让提交到git中的代码
转换成web版，然后提交进去。经过折腾，终于搞定了。

### 明日再续

next gerrit