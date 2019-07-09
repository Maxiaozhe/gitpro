## 基本操作
1. 初期化
```bash
git init        #创建本地仓库
git clone https://github.com/Maxiaozhe/gitpro.git   #克隆远程仓库
```
2. 跟踪文件修改
```bash
git status              #检查文件状态
git status -s | --short #文件状态的简短信息
git add *               #添加修改的文件到暂存区
```
3. 忽略文件
```powershell
new-item .\.gitignore     #创建.gitignore文件
```
🔗[获取各种类型的忽略文件列表](https://github.com/github/gitignore)

4. 比较文件
```bash
git diff                #比较文件
git diff --staged       #比较已暂存的文件
```

5. 提交
```bash
git commit                  #启动默认编辑器
git commit -m "commont"     #直接写注释
#设置默认编辑器
git config --global core.editor code #将缺省编辑器设为vscode
git commit -a -m "add commont"       #跳过追加到暂存区直接commit
```

6. 移除
```bash
git rm                  #未放入缓存区时
git rm -f               #已放入缓存区时
git rm --cached *.a     #仅从暂存区移除，文件保留
```

7. 重命名
```bash
git mv before.txt after.txt     #修改放入暂存区的文件名
```
8. 查看提交历史
```bash
git log                 #查看提交历史
git -p -2               #查看最近的2次提交
                        #-p 查看两次提交的差异
git log --stat          #显示log的简短信息
git log --pretty=online #显示为1行
git log --pretty=format:"%h - %an, %ar: %s"         #按照格式化输出
git log --pretty=format:"%h - %an, %ar: %s" --graph #显示树形结构
git log --since=2.weeks #两周内的便跟
git log -$function_name
```
Format格式
选项  |  说明
-----|------------------------------------------
%H   | 完整哈希字串
%h   | 简短哈希字串
%T   | 树对象的完整嘻哈
%t   | 树对象的简短嘻哈
%P   | 父对象的完整嘻哈
%p   | 父对象的简短嘻哈
%an  | 作者名字
%ae  | 作者email
%ad  | 作者修改日期
%ar  | 作者修定日期（按多久前的计算）
%cn  | 提交者名字
%ce  | 提交者email
%cd  | 提交日期
%cr  | 提交日期（按多久前的计算）
%s   | 提交说明