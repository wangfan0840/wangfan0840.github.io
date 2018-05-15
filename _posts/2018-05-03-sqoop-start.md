---
layout: post
title: "Sqoop详解"
date: 2018-05-03
category: sqoop
tags: [Hadoop，命令]
---
## Sqoop详解
- **走自己的路，让别人无路可走！**  


## 1.查询mysql中的数据库
    sqoop list-databases --connect jdbc:mysql://localhost:3306/cdb  --username root --password root 
## 2、连接mysql并列出数据库中的表
    sqoop list-tables --connect jdbc:mysql://localhost:3306/cdb --username root --password root 
