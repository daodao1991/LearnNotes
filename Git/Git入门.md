# Git入门

###### 什么是版本库呢？版本库又名仓库，英文名**repository**，你可以简单理解成一个目录，这

###### 个目录里面的所有文件都可以被Git管理起来，每个文件的修改、删除，Git都能跟踪，以便

###### 任何时刻都可以追踪历史，或者在将来某个时刻可以“还原”。

###### 初步的git命令：

#### git  init                                   把一个目录变成Git可管理的仓库

#### git  add  <file_name>          将文件添加到仓库中

#### git  commit  -m "xxx"         提交，后面的“xxx”是本次提交的说明

#### git  status                              可以随时查看工作区的状态

#### git  diff  <file_name>		 查看修改内容 



# Git时光机穿梭

### 1.Git跟踪并管理的是修改，而非文件

### 2.工作区和暂存区

#### 工作区（Working Directory）

###### 就是你在电脑里能看到的目录，比如我的`learngit`文件夹就是一个工作区：

![working-dir](https://cdn.liaoxuefeng.com/cdn/files/attachments/0013849082162373cc083b22a2049c4a47408722a61a770000/0)

#### 版本库（Repository）

###### 工作区有一个隐藏目录`.git`，这个不算工作区，而是Git的版本库。

###### Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支`master`，以及指向`master`的一个指针叫`HEAD`。

![git-repo](https://cdn.liaoxuefeng.com/cdn/files/attachments/001384907702917346729e9afbf4127b6dfbae9207af016000/0)



### 3.几种撤销修改的情况

#### 本人总结：

#### git  checkout  --  <file_name>		撤销修改（还未添加到暂存区）

#### git  reset  HEAD  <file_name>		把暂存区的修改撤销掉  (已经添加到了暂存区，但是还未commit)

#### git  reset  --hard  <commit_id>  	回退到之前的某个版本（已经提交到了版本库）

#### 网友总结：

###### 文件已修改，未add到暂存区:

#### git checkout -- file	可还原

###### 文件已修改，并add到暂存区未commit：

#### git read HEAD file

#### git checkout -- file	可还原