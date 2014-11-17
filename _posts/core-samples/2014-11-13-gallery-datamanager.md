---
layout: post
category : lessons
tagline: "by wqqgt"
tags : [gallery]
---
{% include JB/setup %}

## Overview
先扯一下为什么要开始写这个blog，主要是因为工作需要，看了google的源代码之后，
自叹不如，所以需要现在开始研究gallery源码，分析清楚逻辑关系。今天主要说一下DataManager


### DataManager
DataManager是什么呢，从google的设计上来说， DataManager主要负责MediaSource的管理。并且在
GalleryContext中实现了接口 public DataManager getDataManager();这样方便所有的activity直接调用

### DataManager 增加source源
主要实现public MediaObject createMediaObject(Path path)
通过path参数的不同，返回不同的MediaObject，主要有LocalAlbum 和 LocalImage
gallery 中所有的参数都是通过path进行传递的，再通过实现
Path findPathByUri(Uri uri, String type)根据代码中的uri返回Uri对应的path

### 明日再续

next DataManager