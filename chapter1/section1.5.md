# git 常用命令
##level1：
初始化仓库：git init

与远程仓库关联：eg： $ git remote add origin git@github.com:orrvan/workspace.git

下拉项目：git pull

当然你也可以使用git clone 这个复合高级命令（包含 git init +git remote add +git pull +git checkout）

查看与远程仓库关联的信息：eg ： git remote -v 

## level2：
查看当前版本库状态：git status

查看当前‘储藏区’的状态：git stash list 

查看提交日志：git log

推送：$ git push <远程主机名> <本地分支名>:<远程分支名>

如果省略本地分支名，则表示删除指定的远程分支，因为这等同于推送一个空的本地分支到远程分支：$ git push origin :master

时光机：$ git reset --hard HEAD^

创建一个全新的分支，HEAD引用为空，无视你之前分支的无数次提交： $ git checkout --orphan <branch>(搭配  $ git rm --cached  -r . 和 $ git clean -df 使用，注意-r后面还有一个点，表示删除所有文件)