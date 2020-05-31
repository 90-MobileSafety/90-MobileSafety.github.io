---
layout: post
title: "android-加固-inlinehook"
date: 2020-05-27 00.23
description: "使用inlinehook进行伪装函数"
tag: android
---

对loadmethod 进行inline hook 获取当前artmethod 是否等于xxx(methodID) 如个等于 就替换成为其他的methodid的函数   
这样当运行到指定函数后进行替换为其他函数,就影响了判断,算是一种修改偏移地址的函数抽取
