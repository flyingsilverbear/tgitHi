# Learning Git

## Basic Operators

1. git clone
2. git remote
3. git fetch
4. git pull
5. git push

### git clone

远程操作的第一步，通常是从远程主机克隆一个版本库:

`git clone git@github.com:flyingsilverbear/tgitHi.git`

### git remote

为了便于管理，Git要求每个远程主机都必须制定一个主机名。`Git remote` 命令就用与管理主机名。

### git fetch

一旦远程主机版本库有了更新(Git术语叫做commit),需要将这些更新全部取回本地，这时就用到`git fetch`命令。

`git fetch <远程主机名>`

上面的命令是将某个远程主机的更新，全部取回本地。

`git fetch`命令通常用来查看其他人的进程，因为它取回的代码对你本地的开发代码没有影响。默认情况下，`git fetch`取回所有分支的更新。如果只想取回特点分支的更新，可以指定分支名。

`git fetch <远程主机名> <分支名>`

所取回的更新，在本地主机上要用"远程主机名/分支名"的形式读取


### git pull

`git pull`命令的作用是， 取回远程主机某个分支的更新，再与本地的指定分支合并。

比如，取回*origin*主机的*next*分支，与本地的*master*分支合并，需要写成下面这样：

`git pull origin next:master`

如果远程分支是与当前分支合并，则冒号后面的部分可以省略。

### git push

`git push`命令用于将本地分支的更新，推送到远程主机。它的格式与`git pull`命令相仿。例如，将本地的*master*分支推送到远程主机*origin*的*master*分支。如果后者不存在，则会被创建

`git push origin master`
