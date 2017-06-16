---
title: firefox config
date: 2017-05-11 13:39:47
categories: browsers
tags: firefox
description: 
---

火狐打开经常巨慢，网上收集了一些设置，确实快了很多，在火狐地址栏中输入：about:config进入配置：

<font face="微软雅黑" color=Salmon>1.限制页面快进/快退功能中保存的页面总数(默认值是-1表示无限页)</font>

在过滤器栏输入：browser.sessionhistory.max_total_viewers，双击该项，修改值为0。

<!--more-->
<font face="微软雅黑" color=Salmon>2.让火狐在最小化时自动释放内存</font>

右击鼠标－新建－布尔（boolean)项，输入：config.trim_on_minimize,并设置为true。做了这两个设置后火狐速度就快多了，在开了一排页面的情况下，也就23M的内存占用,最小化后只占5M内存。

<font face="微软雅黑" color=Salmon>3.禁用ipv6解析</font>

找到network.http.proxy.pipelining，点击右键，“切换”其值成 true，找到network.dns.disableIPv6 ，右键，切换，值变为true。

<font face="微软雅黑" color=Salmon>4.右键点击FireFox的快捷方式</font>

右键点击FireFox的快捷方式，在“属性”—“快捷方式”—“目标”，加上参数“ /Prefetch:1”。即："C:Program FilesMozilla Firefox\firefox.exe" /Prefetch:1（注意：“/”前有空格）

<font face="微软雅黑" color=Salmon>5.让火狐在后台打开新页面，您继续浏览当前页</font>

找到browser.tabs.loadDivertedInBackground的值切换true。

<font face="微软雅黑" color=Salmon>6.让火狐一次发送多个个请求</font>

找到network.http.pipelining，点击右键，“切换”其值成 true，找到network.http.pipelining.maxrequests并把它的值改的高一些，例如改成30(请求个数)。

<font face="微软雅黑" color=Salmon>7.让火狐快速对网站回复信息反应</font>

点右键，选择 “新建”—“整数”在弹出的对话框中输入 nglayout.initialpaint.delay并将其值改为“0”

<font face="微软雅黑" color=Salmon>8.关闭其他扩展插件法、去掉skin和Theme、取消自动更新等等方法</font>

