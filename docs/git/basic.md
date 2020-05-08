# 基本使用

### 工作流

* `git clone`
* `git pull/git fetch`
* `git commit`
* `git merge/git rebase`
* `git push`
* `git tag`

### 分支管理

* `git branch 分支名` 创建分支
* `git checkout 分支名` 切换分支
* `git checkout -b 分支名` 创建并切换分支
* `git branch -d` 删除分支

### 修改

* `git add` 
* `git rm`
* `git mv`
* `git checkout file`
* `git cherry-pick commit_id` 在当前分支重放commit
* `git reset --soft HEAD^`  撤销提交并保留文件和索引
* `git reset HEAD^` 撤销提交并保留文件
* `git reset --hard HEAD^` 撤销提交
* `git revert commit_id` 撤销已push的commit

### 暂存

* `git stash save`
* `git stash apply`
* `git stash drop`
* `git stash clear` 
* `git stash list`
* `git stash show [stash]`

### 查看

* `git branch`
* `git diff`
* `git status`
* `git log`
* `git show`





