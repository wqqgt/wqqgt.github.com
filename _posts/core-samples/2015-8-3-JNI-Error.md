---
layout: post
category : lessons
tagline: "by wqqgt"
tags : [JNI]
---
{% include JB/setup %}

## JNI开发错误纪录
Fatal signal 11 (SIGSEGV) at 0x00000063 (code=1), thread 29916 (thread-pool-0)

错误原因是申请了内存之后，没有进行memset初始化
