---
layout: page
title: "Sqoop详解"
---
## Sqoop详解
- **探索尝试，发现未知可能！**  
- **走自己的路，让别人无路可走！**  


## 1.查询mysql中的数据库
    sqoop list-databases --connect jdbc:mysql://drds1pouikzz3j49.drds.aliyuncs.com:3306  --username cdb --password Gp30fTtj50blGXke 
## 2、连接mysql并列出数据库中的表
    sqoop list-tables --connect jdbc:mysql://drds1pouikzz3j49.drds.aliyuncs.com:3306/cdb  --username cdb --password Gp30fTtj50blGXke  
## 3、导入数据到HDFS
    sqoop import --connect jdbc:mysql://drds1pouikzz3j49.drds.aliyuncs.com:3306/cdb --username cdb --password Gp30fTtj50blGXke --table subject  --target-dir /data/up/student --num-mappers 1
## 3、直接导入数据到HIVE

    sqoop import  --connect jdbc:mysql://drds1pouikzz3j49.drds.aliyuncs.com:3306/cdb  --username cdb  --password Gp30fTtj50blGXke   --table student   --target-dir /data/up/subject   --num-mappers 1  --fields-terminated-by '\0001'  --delete-target-dir  --hive-import  --hive-overwrite  --hive-database default  --hive-table cdb_student --direct
    sqoop import  --connect jdbc:mysql://drds1pouikzz3j49.drds.aliyuncs.com:3306/cdb  --username cdb  --password Gp30fTtj50blGXke   --table subject   --target-dir /data/up/subject   --num-mappers 1  --fields-terminated-by '\0001'  --delete-target-dir  --hive-import  --hive-overwrite  --hive-database default  --hive-table cdb_subject
    sqoop import  --connect jdbc:mysql://drds1pouikzz3j49.drds.aliyuncs.com:3306/cms  --username cms  --password hdv6HZ3n0jq5bVNi   --table cms_good_course   --target-dir /data/up/cms_good_course   --num-mappers 1  --fields-terminated-by '\0001'  --delete-target-dir  --hive-import  --hive-overwrite  --hive-database default  --hive-table cms_good_course
    
    增加--direct会导致Error: java.io.IOException: mysqldump terminated with status 2
## 4、增量导入到HIVE
    sqoop import  --connect jdbc:mysql://drds1pouikzz3j49.drds.aliyuncs.com:3306/cdb  --username cdb  --password Gp30fTtj50blGXke   --table student   --target-dir /data/up/student   --num-mappers 1  --fields-terminated-by '\0001'   --hive-import     --hive-database default  --hive-table cdb_student  --incremental append  --check-column id --last-value 7335551
    sqoop import  --connect jdbc:mysql://drds1pouikzz3j49.drds.aliyuncs.com:3306/cdb  --username cdb  --password Gp30fTtj50blGXke   --table subject   --target-dir /data/up/subject   --num-mappers 1  --fields-terminated-by '\0001'   --hive-import     --hive-database default  --hive-table cdb_subject  --incremental append  --check-column id --last-value 1615