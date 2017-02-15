###Git学习笔记###
***
####Git配置详解####
*配置*

    git config --global user.name='Your Name'
    git config --global user.email='Your Email'

*创建版本库*

> 创建目录
> 进入目录，执行以下命令

    $ git init
    Initialized empty Git repository in E:/git-learn/.git/

*把文件添加到版本库*

> 第一步，用 git add 命令告诉Git，把文件添加到仓库

    $ git add README.md

> 第二步，使用 git commit 命令把文件提交到仓库

    $ git commit README.md -m '添加README.md文件'
    [master 4718977] 添加README.md文件
     1 file changed, 15 insertions(+)
     create mode 100644 README.md

> 查看当前仓库的状态

    $ git status

> 查看修改过的内容

    $ git diff README.md

*版本管理*

> 查看最近提交记录

    $ git log
    $ git log --pretty=oneline
    75121ab247a183e7d52dbbf7d07b287ca6c21b6d 完善README.md文件
    47189773750d0ffa05041ecf2d782dace85eb4b5 添加README.md文件
    a9ddb4d88d201c6f45f5f55bd30fc3f6b091fb08 添加gitignore文件

> 回退到上一个版本

    $ git reset --hard HEAD^

> 回退到指定的版本

    $ git reset --hard 75121 

> 查看记录的每一条命令(可用于回到未来版本)

    $ git reflog
    75121ab HEAD@{0}: reset: moving to 75121
    4718977 HEAD@{1}: reset: moving to HEAD^
    75121ab HEAD@{2}: commit: 完善README.md文件
    4718977 HEAD@{3}: commit: 添加README.md文件
    a9ddb4d HEAD@{4}: commit (initial): 添加gitignore文件

> 撤销修改

    $ git checkout -- filename
    丢弃工作区的修改
    文件回到最近一次git add或git commit时的状态

    $ git reset HEAD filename
    把暂存区的修改撤销掉，重新放回工作区

> 删除文件

    $ git rm test.txt
    $ git commit -m 'remove file test.txt'

    如果误删了文件，使用以下命令恢复
    $ git checkout -- test.txt

*远程仓库*

> 添加远程库

    $ git remote add origin git@github.com:kwanwong/learn-git.git
    本地库与远程库关联

    $ git push -u origin master
    第一次推送
    $ git push origin master
    第一次之后的推送，不需要-u参数
    把本地库的内容推送到远程库

> 从远程库克隆

    $ git clone git@github.com:kwanwong/hello-world.git

> 创建与合并分支

    $ git checkout -b dev
    创建并切换分支
    或者下面两条命令
    $ git branch dev
    $ git checkout dev 
    
    合并分支
    $ git merge dev
    
    删除分支
    $ git branch -d dev







