# 基本使用

### 帮助

* `tmux list-commands` 所有命令
* `tmux list-keys` 所有快捷键
* `tmux list-sessions` 所有会话
* `tmux list-windows` 所有窗口
* `tmux list-pannes` 所有窗格

### 会话管理 (session)

* `tmux new -s <session-name>` 新建会话
* `tmux ls` 查看会话列表
* `tmux attach -t <session-name>` 进入会话
* `tmux detach <session-name>` 退出会话（exit会退出并关闭会话）
* `tmux switch -t <session-name>` 切换会话
* `tmux rename-session -t session1 session2` 重命名会话
* `tmux kill-session <session-name>` 关闭会话

### 窗口管理 (window)

* `tmux new-window -n <window-name>` 新建窗口
* `tmux list-windows` 所有窗口
* `tmux select-window -t <window-name>` 切换窗口
* `tmux rename-window <window-name>` 重命名窗口
* `tmux kill-window <window-name>` 关闭窗口

### 窗格管理 (pane)

* `tmux split-window` 上下分隔窗口得到2个窗格
* `tmux split-window -h` 左右分隔窗口得到2个窗格
* `tmux list-panes` 所有窗格
* `tmux select-pane -t <窗格序号>` 切换窗格
* `Ctrl+b ;/o` 光标切换到上一个/下一个窗格
* `tmux kill-pane` 关闭窗格

### 设置tmux允许滚动

```
echo "setw -g mouse on" >> ~/.tmux.conf
tmux source-file ~/.tmux.conf
```


