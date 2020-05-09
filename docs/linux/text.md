# 文本处理三大利器

### awk

* `cat <file> | awk -F ',' 'BEGIN{print "字段1","字段2"} { print }'` 输出表头
* `cat <file> | awk 'BEGIN{ORS=","}{ print }` 逗号连接数组
* `cat <file> | awk 'BEGIN{RS=","}{ print }`  逗号分隔字符串
* `cat <file> | awk -F ',' '{ sum += $7; if (min == "") min = max = $7; if ($7 > max) max = $7; if ($7 < min) min = $7 } END { print max, sum/NR, min }'` 计算最大值、最小值、平均值

### grep

* `grep -rl 'aaa' ./  | xargs sed -i "" "s/aaa/bbb/g"` 将当前目录下所有aaa都替换为bbb


### sed