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

