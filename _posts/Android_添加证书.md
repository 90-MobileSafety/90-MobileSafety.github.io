---
layout: post
title: "Android将https证书导入系统目录"
date: 2020-05-21
description: "将证书导入系统"
tag: Android安全
---
记录

用途:抓手机的流量包

这里以burp 为例将证书添加到android 系统证书目录中(system/etc/security/cacerts)
1 获取Burp证书
![](/images/posts/Android_add_证书/1.png)
2 下载openssl(自行百度下载)
3 使用openssl 将der证书生成一个pem文件 
![](/images/posts/Android_add_证书/2生成pem文件.png)
4 将pem文件使用subject_hash_old 生成一个十六进制的数 将其改成文件名 文件格式 十六进制数.0
![](/images/posts/Android_add_证书/3push.png)
5 adb push 9a5ba575.0 /sdcard/
6 重新挂载system 获取读写权限 将9a5ba575 移动到系统证书目录中(system/etc/security/cacerts) 开始正常抓包

