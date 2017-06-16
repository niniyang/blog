---
title: MySQL .sql文件导入导出
date: 2017-05-11 14:14:47
categories: database
tags: MySQL
description: 
---

经常要导入导出数据量庞大的数据，经常要超时！！！身为菜鸟心好累，ORZ...
于是冒着被嘲笑的那啥..从同事那里偷到了一点技艺..嗯~~~ (ˇˍˇ) ～

<font face="微软雅黑" color=Salmon>windows下</font>
<!--more-->
###### 连接数据库

```bash
连接：mysql -h主机地址 -u用户名 －p用户密码 （注:u与root可以不用加空格，其它也一样） 
断开：exit （回车）
```

###### 导入数据库
```bash
常用source 命令
进入mysql数据库控制台，如
mysql -u root -p
mysql>use 数据库
然后使用source命令，后面参数为脚本文件(如这里用到的.sql)
mysql>source d:/dbname.sql
```


