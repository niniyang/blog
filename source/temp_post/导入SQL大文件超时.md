---
title: 导入SQL大文件超时
date: 2017-04-29 16:17:16
categories: database
tags: database
---

### .sql文件太大，导入时报错如下：

<font color=red>Error Code: 2006 - MySQL server has gone away.</font>

原因：配置文件中的max_allowed_packet不够大。

解决：
``` bash
# 直接用SQL语句：
SET GLOBAL  max_allowed_packet=67108864;
```