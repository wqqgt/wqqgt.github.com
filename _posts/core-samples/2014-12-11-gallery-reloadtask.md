---
layout: post
category : lessons
tagline: "by wqqgt"
tags : [gallery]
---
{% include JB/setup %}

## ReloadTask机制
RelaodTask主要是实现了异步加载数据，实现了界面和数据进行了分层结构


### ReLoadTask的调用时机
1. ActivityState 在onResume的时候初始化ReloadTask   
2. 监听的数据改变的时候， 会调用notifyContentChanged， 从而调用ReloadTask   
3. setContentWindow之后，会调用 notifyDirty方法进行RelaodTask

## ReloadTask的实现机制
ReloadTask Start 之后，就只有一个while循环，整个线程都在等待   
可以调用notifyDirty()和terminate()实现数据的更新和ReloadTask的中止    
ReloadTask的实现机制主要分为两个部分    
第一个部分主要是GetUpdateInfo   
第二个部分是UpdateContent   

### GetUpdateInfo
GetUpdateInfo 主要的工作是判断Reload之后的数据和新的数据是不是有变化   
通过Version控制每条数据的变化。如果有变化的话，返回了新的数据信息


### UpdateContent
UpdateContent 主要是通知UI线程进行更新操作，数据已经更新完成，就通知UI   
线程进行重新绘制，刷新整个屏幕


next MediaSource中的调用