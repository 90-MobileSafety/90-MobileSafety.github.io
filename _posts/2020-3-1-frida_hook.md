---
layout: post
title: "frida hook"
date: 2020-03-1
description: "frida"
tag: Android安全
---

一、frida简介
frida是一款基于python + java 的hook框架，可运行在androidioslinuxwinosx等各平台，主要使用动态二进制插桩技术

1、插桩技术
插桩技术是指将额外的代码注入程序中以收集运行时的信息，可分为两种：
(1)源代码插桩[Source Code Instrumentation(SCI)]：额外代码注入到程序源代码中。
(2)二进制插桩（Binary Instrumentation）：额外代码注入到二进制可执行文件中。
●静态二进制插桩[Static Binary Instrumentation(SBI)]：在程序执行前插入额外的代码和数据，生成一个永久改变的可执行文件。
●动态二进制插桩[Dynamic Binary Instrumentation(DBI)]：在程序运行时实时地插入额外代码和数据，对可执行文件没有任何永久改变。
2、你能用DBI做些什么呢
（1）访问进程的内存
（2）在应用程序运行时覆盖一些功能
（3）从导入的类中调用函数
（4）在堆上查找对象实例并使用这些对象实例
（5）Hook，跟踪和拦截函数等等
