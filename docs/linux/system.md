# 系统状态

### 负载

* `top`
* `uptime` 

### CPU

* `mpstat -P ALL` cpu各核使用率

### 内存

* `vmstat`
* `free`

### 网络

* `ss` 
* `ifstat` 网络io统计
* `netstat -nat | grep <port>` 指定端口的网络连接数
* `netstat -nat|awk '{print $6}'|sort|uniq -c|sort -rn` 网络连接各状态统计

### 磁盘

* `iostat` 磁盘io统计
* `iotop -o` 磁盘io占用top 
* `du -sh ./* | sort -rn | head -n 10` 磁盘空间占用top10的文件

### 进程

* `pidstat`
* `ps aux head -1; ps aux | sort -rn -k3 | head -n 10` cpu占用top10的进程
* `ps aux head -1; ps aux | sort -rn -k4 | head -n 10` 内存占用top10的进程
* `pidstat -d <时间间隔> -p <进程id>` 进程占用磁盘io
* `iftop`
* `nethogs` 进程带宽

### 线程

* `ps hH p | grep <pid>` 查看进程的线程
