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
git commit -a -m "add commont"
```
