---
layout: post
title: git常用操作命令
date: 2016-09-13 21:45
comments: false
categories: [版本管理]
---

## git常用操作命令

一、远程操作

- 从远程主机克隆一个版本库

```
$ git clone <版本库的网址>
```

- 删除远程分支


```
$ git push origin :branch-name
```
注意：冒号前面的空格不能少，原理是把一个空分支push到server上，相当于删除该分支。

- 当前分支获取另一个分支提交的记录

```
// 获取分支branch1的提交记录Id
$ git checkout branch1
// commit 809d95ea1c3d17ed6ba8e25ae2abe15b0f3e737f
$ git log

// 在分支branch2中重新提交分支branch1中获取的commitId
$ git checkout branch2
$ git cherry-pick 809d95ea1c3d17ed6ba8e25ae2abe15b0f3e737f 
```

注意：如果提示获取失败（冲突），请按正常处理流程安排。



