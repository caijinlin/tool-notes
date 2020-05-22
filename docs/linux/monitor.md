# 系统监控

### 进程内存（cpu）监控

```
# !/bin/sh
# 内存是$4，cpu是$3，$2是进程号，内存>5%
pids=ps aux | grep <progress> | grep -v grep | awk '{if($4>=5)print $2}' 
for pid in pids; 
   do kill -9 $pid echo date +'%F %T' $pid >>/var/log/kill.log 
done
```

### 网络带宽监控

```

```

### 磁盘空间监控

```
#!/bin/sh 

diskinfo="/tmp/diskinfo.txt"
for d in `df -P | grep /dev | awk '{print $5}'| sed 's/%//g'`
do
	if [ $d -gt 90 ];then
		df -h>>$diskinfo;
		#sendmail
		mutt -s "disk warining!" "1399534656@qq.com" <${diskinfo} -a ${diskinfo}
		exit 0;
	fi
done
``` 

