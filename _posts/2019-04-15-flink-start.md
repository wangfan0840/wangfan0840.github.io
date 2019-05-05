---
layout: post
title: "flink"
date: 2019-04-15
category: flink
tags: [flink，命令]
---
## flink详解
- **走自己的路，让别人无路可走！**  


## Install
https://flink-china.org/doc/quickstart/setup_quickstart.html
~~~
$ brew install apache-flink
$ flink --version
Version: 1.7.2, Commit ID: ceba8af


~~~
## Start  a Local Flink Cluster
~~~
$ cd /usr/local/Cellar/apache-flink/1.7.2/libexec
$ ./bin/start-cluster.sh
~~~
http://localhost:8081

## Run the Example
### start local server
~~~
nc -l 9000
~~~

### Submit the Flink program
~~~
./bin/flink run examples/streaming/SocketWindowWordCount.jar --port 9000
~~~

### input something

~~~
nc -l 9000

lorem ipsum
ipsum ipsum ipsum
bye
~~~
### 
~~~
$ tail -f log/flink-*-taskexecutor-*.out
lorem : 1
bye : 1
ipsum : 4
~~~

stop Flink 
~~~
$ ./bin/stop-cluster.sh
~~~