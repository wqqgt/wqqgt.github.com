---
layout: post
category : lessons
tagline: "by wqqgt"
tags : [android studio]
---
{% include JB/setup %}

# 关于android studio和ART的思考

##ART和Dalvik
ART 的机制与 Dalvik 不同。在Dalvik下，应用每次运行的时候，字节码都需要通过即时编译器转换为机器码，这会拖慢应用的运行效率，而在ART 环境中，应用在第一次安装的时候，字节码就会预先编译成机器码，使其成为真正的本地应用。这个过程叫做预编译（AOT,Ahead-Of-Time）。这样的话，应用的启动(首次)和执行都会变得更加快速。

##android studio 未来畅想
1. 支持纯java开发， 编译成机器码
2. 支持纯c/c++开发， 编译成机器码
3. 支持js和css开发， 通过浏览器编译成机器码 

