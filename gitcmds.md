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

## 创建分支
git branch branch_name #在本地创建分支
git checkout branch_name #切换到分支
git log --oneline --decorate --graph --all #查看分叉历史

## 合并分支
git commit -m "add comment message" 
git push branch_name    #提交分支
git checkout master     #且换到主分支
git merge branch_name   #合并分支


