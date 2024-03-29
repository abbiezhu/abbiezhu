## **完成配置**：
ssh-keygen -t rsa -C "abbiezhu@gmail.com"  
/用户主目录下/.ssh/id_rsa和id_rsa.pu两个文件  
```git
git config --global user.name "abbiezhu"  
git config --global user.email "abbiezhu@gmail.com"  
```
><img width='20px' src='https://www.lymiss.com/wp-content/themes/abbiezhu/favicon.png#pic_center' />[**我的GIT仓库**](https://github.com/abbiezhu/abbiezhu)
## **命令**
把文件加到git 库
git add 文件名
git commit -m '写信息'  

git status 查看状态
git diff 查看修改内容

git log 查 看各个LOG 版本信息
git log --pretty=oneline 单行查看。

git reset --hard HEAD^ 恢复到上一个版本。
git reset --hard HEAD^^ 恢复到上上一个版本。
git reset --hard "commit_ID"

git relog
git reflog 查看版本记录。

git checkout --文件名    撤销修改 （丢弃工作区的修改）。
git checkout -- file 命令中的--很重要，没有--，就变成了“切换到另一个分支”的命令

git reset HEAD <file>可以把暂存区的修改撤销掉

git rm --file  删除版本库的文件
git checkout --file 其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。

## **github远程**
```git
git remote add origin git@github.com:abbiezhu/abbiezhu.git
```
链接到GITHUB 
```git
git push -u origin master
```
第一次推送到 远程库上。

把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。
由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。
git push origin master 推送到 远程库上。  
---
## **添加gitee.com**
Git 全局设置:
```git
git config --global user.name "abbiezhu"
git config --global user.email "abbiezhu@gmail.com"
```
### **创建 git 仓库:**
```
mkdir abbiezhu
cd abbiezhu
git init
touch README.md
git add README.md
git commit -m "first commit"
git remote add origin https://gitee.com/abbiezhu/abbiezhu.git
git push -u origin master
```
### **已有仓库?**
```
cd existing_git_repo
git remote add origin https://gitee.com/abbiezhu/abbiezhu.git
git push -u origin master
```
…or create a new repository on the command line

### **添加github.com**
```
git init
git add README.md
git commit -m "first commit"
git branch -M master
git remote add origin git@github.com:abbiezhu/abbiezhu.git
git push -u origin master

…or push an existing repository from the command line

git remote add origin git@github.com:abbiezhu/abbiezhu.git
git branch -M master
git push -u origin master
```
## **分支**
git checkout -b abb
创建一个分支 ABB  并切换
同下：
git branch abb
git checkout abb

在分支 中做的修改 切到 主分支后 内容会消失
要把其添加到 主分支中才可以:
git merge abb  在当前分支添加 ABB分支
git branch -d abb 删除ABB 分支（ABB分支做的修改 还是存在的）
当然还可以用swich 命令
git swich -c abb 创建abb分支并切换 （=git checkout -b abb）
git swich abb = git checkout abb

添加分支的解决冲突的测试。看一下效果。
这一行是在  主分支添加了一行内容

可以查看到 合并分支 的详情内容
```git
git log --graph --pretty=oneline --abbrev-commit （git log --graph）
```
> 以下来自 abb01 分支做的修改
不在主分支 做事情，主分支只用来合屏  下面的分支内容。
然后在marster分支中 用
git merge abb01 --no-ff 合并也可以加上 commit
git merge abb01 --no-ff -m '来自abb01分支的修改'。
---
### Contact:
+ What? u dont know me?/
+ QQ: 2264253926
+ TEL：186-6217-3570
+ WEB：[www.lymiss.com](www.lymiss.com)
+ MAIL: abbiezhu@gmail.com