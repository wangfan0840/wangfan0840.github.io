---
layout: post
title: "Hadoop 命令"
date: 2018-05-03
category: hadoop
tags: [Hadoop，命令]
---
## Hadoop常用命令
- **走自己的路，让别人无路可走！**  
## 1.hadoop fs （hdfs dfs）  文件操作
### 1）ls 显示目录
    hadoop fs -ls [uri形式目录] 
### 2） cat 查看文件内容   
    hadoop fs cat URI [URI …]
### 3） mkdir 创建目录  
    hadoop fs -mkdir [uri形式目录] 
## 2、hdfs dfsadmin 管理命令
### 1）-report
    hdfs dfsadmin -report 
    
 ##hive删除id为2的记录
 insert overwrite table A select * from A where id !=2;