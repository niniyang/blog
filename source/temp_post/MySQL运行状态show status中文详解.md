---
title: MySQL运行状态show status中文详解
date: 2017-06-05 14:45:47
categories: database
tags: MySQL
description: 
---

要优化MySQL运行效率都少不了要运行show status查看各种状态，下面的这个表是参考官方文档及网上资料整理出来的show status中文详细解释，存档方便以后查阅。

<!--more-->

|     状态名     |      作用域    |     详细解释          |
| ------------- | :-------------: | :---------------------: |
| Aborted_clients | Global | 由于客户端没有正确关闭连接导致客户端终止而中断的连接数 |
| Aborted_connects | Global |试图连接到MySQL服务器而失败的连接数 |
| Binlog_cache_disk_use | Global |使用临时二进制日志缓存但超过binlog_cache_size值并使用临时文件来保存事务中的语句的事务数量|
| Binlog_cache_use | Global |使用临时二进制日志缓存的事务数量|
| Bytes_received | Both |试图连接到MySQL服务器而失败的连接数 |
| Bytes_sent | Global |	从所有客户端接收到的字节数。 |
| com* |  |各种数据库操作的数量 |
| Compression | Session |客户端与服务器之间只否启用压缩协议 |
| Connections | Global |试图连接到(不管是否成功)MySQL服务器的连接数 |
| Created_tmp_disk_tables | Both |服务器执行语句时在硬盘上自动创建的临时表的数量 |
| Created_tmp_files | Global |mysqld已经创建的临时文件的数量 |
| Created_tmp_tables | Both |服务器执行语句时自动创建的内存中的临时表的数量。如果Created_tmp_disk_tables较大，你可能要增加tmp_table_size值使临时 表基于内存而不基于硬盘 |
| Delayed_errors | Global |用INSERT DELAYED写的出现错误的行数(可能为duplicate key)。 |
| Delayed_insert_threads | Global |使用的INSERT DELAYED处理器线程数。 |
| Delayed_writes | Global |写入的INSERT DELAYED行数 |
| Flush_commands | Global |	执行的FLUSH语句数。 |
| Handler_commit | Both |	内部提交语句数 |
| Handler_delete | Both |	行从表中删除的次数。 |

待续。。。