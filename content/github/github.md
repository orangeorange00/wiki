---
title: "Github tips"
layout: page
data: 2016-12-4 14:50
---

[TOC]

#Github 命令#

##New project##

linux

* 在github中创建新仓库
* 在本地中$git init #其中.git文件记录git相关信息。
* $ git checkout -b source #创建source分支，默认会有master分支
* $ git add 添加文件至暂存区
* $ git commit -m "your commit" #添加描述
* $ git remote add origin git@github.com:<username>/<projectname>.git #管理主机名
* $ git push 提交

windows

用github中的desktop选项，在本地仓库改变后提交commit，然后publish

##git clone##

支持http,ssh,git协议

##git remote##

$git remote #列出所有主机

$git remote -v #列出主机地址

$ git remote add <主机名> <网址> #添加主机


##git add##

$ git add -A #暂存区与工作区保持一致（stages All）

$ git add . #暂存区新建文件及更改文件

$ git add -u #暂存区删除文件及更改文件


##git fetch##

$ git fetch <远程主机名> #将某个远程主机的更新，全部取回本地。

git fetch命令通常用来查看其他人的进程，因为它取回的代码对你本地的开发代码没有影响。

$ git fetch <远程主机名> <分支名>

$ git checkout -b newBrach origin/master #在origin/master的基础上，创建一个新分支。

$ git merge origin/master #在当前分支上，合并origin/master


##git pull##

$ git pull <远程主机名> <远程分支名>:<本地分支名> #取回远程主机某个分支的更新，再与本地的指定分支合并

$git branch --set-upstream master origin/next #指定master分支追踪origin/next分支

这样可以直接用$ git pull

$git pull -p 加上参数 -p 就会在本地删除远程已经删除的分支。

##git push##

$ git push <远程主机名> <本地分支名>:<远程分支名>

$ git push origin master #将本地的master分支推送到origin主机的master分支。如果后者不存在，则会被新建。

$ git push origin :master #删除origin主机的master分支。

$ git push -u origin master #令行中的-u参数，在推送成功后自动建立本地分支与远程版本库分支的追踪。

$ git push --all origin #不管是否存在对应的远程分支，将本地的所有分支都推送到远程主机，这时需要使用--all选项。

$ git push --force origin #如果远程主机的版本比本地版本更新，推送时Git会报错，要求先在本地做git pull合并差异，然后再推送到远程主机。这时，如果你一定要推送，可以使用--force选项。

参考[http://www.ruanyifeng.com/blog/2014/06/git_remote.html](http://www.ruanyifeng.com/blog/2014/06/git_remote.html).Thank you so much.
