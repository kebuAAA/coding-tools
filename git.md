## 一些简单的概念
一般来说，在本地创建一个git仓库，会产生三个区域：工作区（disk）、暂存区(stage/index)、本地仓库（local）。
* 工作区即为电脑的硬盘空间，
* 暂存区：相当于一个缓存区域，用来临时存放改动
* 本地仓库：存放在本地的git仓库，主要用于本地的版本控制

![](img/git/2025-01-12-22-03-44.png)

## 仓库创建
```bash
#将一个文件夹初始化为一个git 仓库
git init
#将文件夹下的所有文件添加到git仓库(添加到暂存区)
git add *
#提交文件到git仓库（添加到本地的Head中）
git commit -m "first commit"
# 提交到远程仓库
git remote add origin target-url
# -u 参数是将本地的main分支和远程的main分支关联起来
git push -u origin main
```

## 添加上游仓库
期望实现的目标是代码保存在自己的仓库中，但是如果fork的上游代码有变动，同步到自己的仓库中。
```bash
# 查看当前远程仓库的配置
git remote -v
#添加上游仓库
git remote add upstream https://github.com/ORIGINAL_OWNER/repo.git
```
## 分支管理
```bash

```

## github国内访问配置
修改配置文件:
```bash
sudo vim /etc/hosts
```
```bash
# add github.com

140.82.121.4 github.com

199.232.69.194 github.global.ssl.fastly.net
```
