# Git push 本地项目推送到远程分支操作步骤

1.创建本地项目，在目录中打开Git Bash命令行工具

2.设置全局信息(包括用户名，邮箱地址)

    git config --global user.name "您的姓名"

    git config --global user.email "lnssky@163.com"

3.创建本地数据仓库，执行以下命令

    git init

    touch README.md

    git add README.md

    git commit -m "通过Git Bash提交"

    git remote add origin https://github.com/5c5d/tkp-news

    git push -u origin master

4.命令解释:

    1、在当前目录下生成.git目录，该目录为仓库；而当前目录为工作空间。

    2、生成README.md文件,是关于工程代码的介绍，类似与使用说明书。

    3、将README.md添加到索引库中。

    4、将修改提交到本地仓库中，并写上备注"通过Git Bash提交"

    5、添加一个新的远程仓库origin

    6、将本地文件推送到远程仓库origin的分支master中。

    git push <远程主机名> <本地分支名>:<远程分支名>

    git push origin master:master

5.使用git命令推送项目完成

====小提示====

git push origin与git push -u origin master的区别

git push origin
上面命令表示，将当前分支推送到origin主机的对应分支。如果当前分支只有一个追踪分支，那么主机名都可以省略，直接git push。
如果当前分支与多个主机存在追踪关系，那么这个时候-u选项会指定一个默认主机，这样后面就可以不加任何参数使用git push。

---------------------------------------------------------------
git push -u origin master
上面命令将本地的master分支推送到origin主机，同时指定origin为默认主机。
后面就可以不加任何参数使用git push。 不带任何参数的git push，默认只推送当前分支，叫做simple方式。
此外，还有一种matching方式，会推送所有有对应的远程分支的本地分支。
Git 2.0版本之前，默认采用matching方法，现在改为默认采用simple方式。


# Git基本常用命令如下：

    mkdir xx                创建一个空目录 xx指目录名

    pwd                     显示当前目录的路径。

    git init                把当前的目录变成可以管理的git仓库，生成隐藏.git文件。

    git add xx              把xx文件添加到暂存区去。

    git commit –m "xx"      提交文件 –m 后面的是注释。

    git status              查看仓库状态

    git diff xx             查看xx文件修改了那些内容

    git log                 查看历史记录

    git reset –hard HEAD^ 或者 git reset –hard HEAD~ 回退到上一个版本

    (如果想回退到100个版本，使用git reset –hard HEAD~100)

    cat xx                  查看xx文件内容

    git reflog              查看历史记录的版本号id

    git checkout – xx       把xx文件在工作区的修改全部撤销。

    git rm xx               删除xx文件

    git remote add origin https://github.com/5c5d/tkp-news    关联一个远程库

    git push –u(第一次要用-u 以后不需要) origin master          把当前master分支推送到远程库

    git clone https://github.com/5c5d/tkp-news                从远程库中克隆

    git checkout –b dev     创建dev分支 并切换到dev分支上

    git branch              查看当前所有的分支

    git branch name         创建分支

    git branch –d dev       删除dev分支

    git checkout master     切换回master分支

    git merge dev           在当前的分支上合并dev分支

    git stash               把当前的工作隐藏起来 等以后恢复现场后继续工作

    git stash list          查看所有被隐藏的文件列表

    git stash apply         恢复被隐藏的文件，但是内容不删除

    git stash drop          删除文件

    git stash pop           恢复文件的同时 也删除文件

    git remote              查看远程库的信息

    git remote –v           查看远程库的详细信息

    git push origin master  Git会把master分支推送到远程库对应的远程分支上

---------------------------Git常用命令结束-------------------------------

通过Git Bash提交 2019-10-25

增加 hello-world 分支

# tkp-news
