# git command list
## 基本操作
git init            #创建一个本地仓库

git add *           #跟踪文件

git status          #查看状态

git status -s       #查看简短状态信息

git diff            #查看改动

git diff --cached   #查看已经暂存的改动

## 查看
git log             #显示提交历史

git log -p -2       #显示最近2次提交

git log --stat      #显示简略统计
```
 .gitignore | 2 ++
 README.md  | 1 +
 gitcmds.md | 8 ++++++++
 3 files changed, 11 insertions(+)
```
git log --since=2.week #显示最近2周的提交

git log --pretty=oneline #一行显示

git log --pretty=format:"%h - %an, %ad : %s" #指定显示格式

```
%h  -提交对象的简短哈希值
%an -作者名
%ad -修改日期
%s  -提交说明
```

## 提交
git commit -m "add comments message"    #添加注释

git fetch

git push

git push origin master                  #提交到远程服务器


## 远程查看
git remote show origin                  #查看远程仓库信息


# 远程仓库的移除
git remove name                         #移除远程仓库

# 从服务器中删除文件
git rm -r -n --cached [file path]       #确认待删除文件列表 
```
-n         #只打印文件名，并不删除
--cached   #只从仓库中删除，保留本地文件
```
git rm -r --cached [file path]       #标记删除文件

git commit -m "delete files"         #提交删除文件

git push 

## 创建分支
git branch branch_name #在本地创建分支

git checkout branch_name #切换到分支

git log --oneline --decorate --graph --all #查看分叉历史


## 取消回退
### 取消对文件的修改。还原到最近的版本，废弃本地做的修改。
```
git checkout -- <file>
```

### 取消已经暂存的文件。即，撤销先前"git add"的操作
```
git reset HEAD <file>...
```

### 修改最后一次提交。用于修改上一次的提交信息，或漏提交文件等情况。
```
git commit --amend
```

### 回退所有内容到上一个版本
```
git reset HEAD^
```
### 回退a.py这个文件的版本到上一个版本  
```
git reset HEAD^ a.py  
```
### 向前回退到第3个版本  
```
git reset –soft HEAD~3  
```
### 将本地的状态回退到和远程的一样  
```
git reset --hard origin/master 
```
### 回退到某个版本  
```
git reset 057d  
```
### 回退到上一次提交的状态，按照某一次的commit完全反向的进行一次commit.(代码回滚到上个版本，并提交git)
```
git revert HEAD
```
