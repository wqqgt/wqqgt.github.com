---
layout: post
category : lessons
tagline: "by wqqgt"
tags : [gallery]
---
{% include JB/setup %}

## Overview
MediaSource的实现


### MediaSource中的方法
getPrefix() 得到mPath中的区分协议即(/local/image中的local)，主要包括local, combo, secure等   
findPathByUri(Uri uri, String type) 通过Uri和type得到的Path   
createMediaObject(Path path) 根据findPathByUri中得到的path创建出不同的MediaObject对象。   
pause() 暂停方法activity中OnPause中会调用    
resume()恢复方法activity中OnResume中会调用    
getDefaultSetOf(Path item) PhotoPage中会调用实现默认打开某张图片    
getTotalUsedCacheSize() 用于计算用了缓存的大小    
getTotalTargetCacheSize()目标所有缓存的大小     
mapMediaItems(ArrayList<PathId> list, ItemConsumer consumer)用来进行批量操作的接口     


### 明日再续

next MediaSource中的调用