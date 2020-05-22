# 文本处理

### awk

* `cat <file> | awk -F ',' 'BEGIN{print "字段1","字段2"} { print }'` 输出表头
* `cat <file> | awk 'BEGIN{ORS=","}{ print }` 逗号连接数组
* `cat <file> | awk 'BEGIN{RS=","}{ print }`  逗号分隔字符串
* `cat <file> | awk -F ',' '{ print NR, NF }'` 查看行数、列数
* `cat <file> | awk -F ',' '{count[$1]++} END {for(k in count) print k,count[k]}'` 统计
* `cat <file> | awk -F ',' '{ sum += $7; if (min == "") min = max = $7; if ($7 > max) max = $7; if ($7 < min) min = $7 } END { print max, sum/NR, min }'` 计算最大值、最小值、平均值 

### grep

* `grep -v "match_pattern" <file>` 输出除了什么之外
* `grep -c "match_pattern" <file>` 输出包含字符行数
* `grep "match_pattern" . -r -n ` 递归搜索文件
* `grep -E "pattern1|pattern2" <file>` 匹配多个样式

### sed

* `sed '/^$/d' <file>` 删除空白行
* `sed '2d' <file>` 删除文件第2行
* `sed '2,$d' file` 删除文件第2到末尾所有行
* `sed '$d' file` 删除文件最后一行
* `sed 's/book/books/g' <file>` 替换文件的所有字符串
* `sed 's/book/books/2g' <file>` 从第N处匹配开始替换时替换文件的所有字符串
* `sed 's/,/\n/g' <file>` 替换换行符


### uniq

* `cat <file1> <file2> | sort | uniq -u` 求文本差集

### tr

* `cat <file> | tr a-z A-Z` 小写转大写
* `cat <file> | tr "," "\t"` 逗号分隔符转tab 

### zip

* `zip -r <file>.zip <file>`  
* `unzip <file>.zip`

### rsync

需要复制本机ssh公钥到远程机器

```
cat ~/.ssh/id_rsa.pub >> authorized_keys
```

* `rsync --bwlimit=10000 -artP <file> -e 'ssh -p <port>' root@<ip>:<target_path>` 从本地传输文件到远程机器
* `rsync --bwlimit=10000 -artP -e 'ssh -p <port>' root@<ip>:<source_path> ./` 从远程机器拉取文件到本地
