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

> 查看记录的每一条命令

    $ git reflog
    75121ab HEAD@{0}: reset: moving to 75121
    4718977 HEAD@{1}: reset: moving to HEAD^
    75121ab HEAD@{2}: commit: 完善README.md文件
    4718977 HEAD@{3}: commit: 添加README.md文件
    a9ddb4d HEAD@{4}: commit (initial): 添加gitignore文件


