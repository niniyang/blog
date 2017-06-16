---
title: Windows中cmd操作mysql
date: 2017-05-11 14:10:47
categories: database
tags: MySQL
description: 
---

打开CMD
将工作目录切换到MySQL的bin下
mysql -u root -p
输入密码即可登陆MySQL
问号可以查看帮助
首先需要选择操作的数据库use database_name
然后可以进行select等操作
需要注意的是，<font color=red>操作要记得分号结尾</font>
如果忘记输入分号可以用\c来结束命令输入
常见的操作如下表
<!--more-->
-------------------------------------------------------------------------------------

连接：mysql -h主机地址 -u用户名 －p用户密码 （注:<font color=Salmon>u与root可以不用加空格，其它也一样</font>） 
断开：exit （回车） 

创建授权：grant select on 数据库.* to 用户名@登录主机 identified by \"密码\" 
修改密码：mysqladmin -u用户名 -p旧密码 password 新密码 
删除授权: revoke select,insert,update,delete om *.* from test2@localhost; 


显示数据库：show databases; 
显示数据表：show tables; 
显示表结构：describe 表名; 


创建库：create database 库名; 
删除库：drop database 库名; 
使用库：use 库名; 


创建表：create table 表名 (字段设定列表); 
删除表：drop table 表名; 
修改表：alter table t1 rename t2 
查询表：select * from 表名; 
清空表：delete from 表名; 
备份表: mysqlbinmysqldump -h(ip) -uroot -p(password) databasename tablename > tablename.sql 
恢复表: mysqlbinmysql -h(ip) -uroot -p(password) databasename tablename < tablename.sql（操作前先把原来表删除） 


增加列：ALTER TABLE t2 ADD c INT UNSIGNED NOT NULL AUTO_INCREMENT,ADD INDEX (c); 
修改列：ALTER TABLE t2 MODIFY a TINYINT NOT NULL, CHANGE b c CHAR(20); 
删除列：ALTER TABLE t2 DROP COLUMN c; 


备份数据库：mysql\bin\mysqldump -h(ip) -uroot -p(password) databasename > database.sql 


