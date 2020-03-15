# Git

## Git的安装（一路傻瓜式的next)

## 初始化Git仓储（仓库）
- 这个仓库会存放，git对我们项目代码进行备份的文件
- 在项目目录右键打开 git bash
- 命令：`git init`

## 自报家门
- 就是在git中设置当前使用的用户是谁
- 每一次备份都会把当前备份者的信息存储起来
- 命令：
    + 配置用户名：`git config --global user.name "xiaoming"`
    + 配置邮箱：`git config --global user.email "xiaoming@sina.com"`

## 把代码存储到.git
- 1.把代码放到仓储的门口（暂存区）
    + `git add ./test.md`   所有指定的文件放到暂存区
    + `git add ./`          把所有修改的文件添加到暂存区
- 2.把仓储门口的代码放到里面的房间中去（版本库）
    + `git commit -m "这次提交的说明"`

## 可以一次性把我们修改的代码放到版本库中去
- `git commit --all -m "说明信息"`
    + --all 表示把所有修改的文件提交到版本库

## 查看当前的状态
- 可以用来查看当前代码有没有被放到仓储中去
- 命令：`git status`

## 回退到指定的版本
- `git reset --hard Head~0`
    + 表示回退到上一次代码提交时的状态
- `git reset --hard Head~1`
    + 表示回退到上上次代码提交时的状态
- `git reset --hard [版本号]`
    + 可以通过版本号精确的回退到某一次提交时的状态
- `git reflog`
    + 可以看到每一次切换版本的记录：可以看到所有提交的版本号

## 分支
- 默认是有一个主分支master

### 创建分支
- `git branch dev`
    + 创建了一个dev分支
    + 在刚创建时dev分支里的东西和master分支里的东西时一样的

### 切换分支
- `git checkout dev`
    + 切换到指定的分支，这里的切换到名为dev的分支
    + `git branch` 可以查看当前有哪些分支

### 合并分支
- `git merge dev`
    + 合并分支内容，把当前分支与指定的分支（dev），进行合并
    + 当前分支指的是`git branch` 命令输出的前面有*号的分支
- 合并时如果有冲突，需要手动去处理，处理后还需要再提交一次

## GitHub
- https://github.com
- 不是git，只是一个网站
- 只不过这个网站提供了允许别人通过git上传代码的功能

### 提交代码到GitHub（当作git服务器来用）
- `git push [地址] master`
    + 实例：`git push https://github.com/mengliuliu/test2.git master`
    + 会把当前分支的内容上传到远程的master分支上

- `git pull [地址] master`
    + 实例：`git pull https://github.com/mengliuliu/test2.git master`
    + 会把远程分支的数据得到：（*注意本地要初始一个仓储*）

- `git clone [地址]`
    + 会得到远程仓储相同的数据，如果多次执行会覆盖本地内容
