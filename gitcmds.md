# git command list
## 基本操作
git init
git add *
git status
git status -s
git diff
git diff --cached
## 查看·
git log
git log -p -2  #显示最近2次提交
git log --stat  #显示简略统计
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

```

git commit #added git command  
## 
