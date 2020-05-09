# 系统状态

### 负载

* `top`
* `uptime` 

### CPU

* `mpstat -P ALL` cpu各核使用率

### 内存

```
free
vmstat
```

### 网络

* `netstat -nat | grep LISTEN`  获取监听的端口
* `netstat -nat|awk '{print $6}'|sort|uniq -c|sort -rn` tcp状态统计

### 磁盘

* `du -sh ./* | sort -rn | head -n 10` 磁盘占用top10的文件

### 进程

* `ps aux head -1; ps aux | sort -rn -k3 | head -n 10` cpu占用top10的进程
* `ps aux head -1; ps aux | sort -rn -k4 | head -n 10` 内存占用top10的进程
* `iotop -o` 磁盘io占用top 