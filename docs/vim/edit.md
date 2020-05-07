# 编辑

### 增加

* `i\a\A` 当前字母前\后插入;当前行尾部插入
* `O\o` 上一行/下一行插入
* `bi/ba/bA` 上一个单词插入
* `ei/ea/eA` 下一个单词插入
* `wi/wa/wA` 下一个单词插入

### 删除

* `x/s` 删除字符；删除字符并进入插入模式
* `d` 删除单词
* `nx` 删除n个字符
* `dnw` 删除n个单词
* `d0` 删除到行首
* `d$` 删除到行尾
* `dw/db/de` 反向删除单词、正向删除单词
* `cw/cb/ce` 反向删除单词并进入插入模式、正向删除单词并进入插入模式
* `dt{char}` 删除直到遇到字符
* `dfa` 删除从当前光标到光标后面的第一个a字符之间的内容
* `dd/D` 删除当前行并鼠标移动到下一行；删除当前行并鼠标在当前行
* `cc\C`：删除当前行并进入插入模式；删除当前字母并进入插入模式
* `d%` 删除函数体
* `ggdG` 删除全部

### 替换

* `r{char}` 替换字符
* `R{chars}` 替换多个字符
* `:%s/xx/xx` 替换第一个
* `:%s/xx/xx/g` 替换当前行
* `:%s/xx/xx/g` 替换全部
* `:%s/old/new/gc` 替换全部，并提示是否进行替换
* `xp` 交换当前字母与后一个字母的位置
* `u/U` 将可视模式下选择的字母全改成大写/小写字母

### 查找

* `t/F/f{char}` 行内搜索，;查找下一个，,查找上一个    
* `%` 当前行可以查找配对的括号
* `/xx` 可以查找某个单词xx，n查找下一个，N查找上一个
* `?xx` 可以反向查找
 
### 复制

* `y` 复制
* `yfa` 拷贝从当前光标到光标后面的第一个a字符之间的内容.
* `y%` 复制函数体
* `nyy` 复制多行
* `ggyG` 拷贝全部

### 粘贴

* `p` 粘贴

### 撤销

* `u` 撤销命令
* `Ctrl + R` 重做撤销命令