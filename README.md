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
