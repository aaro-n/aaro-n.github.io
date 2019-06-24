---
title: Hexo双分支
date: 2019-06-25 06:10:56
tags:
---

# 优点

便有更换电脑恢复，可以进行文章备份。

# 具体操作

* 按照网上教程进行Hexo部署，修改主目录下的配置文件

* 具体代码：

  `git init` ，初始化

  `git add .`，将修改文件添加

  `git commit -m "修改说明"`，修改内容

  `git remote add origin 将Github上的地址替换`，连接远程Github地址

  `git branch 分支名称`，创建保存备份的分支，注意master分支只能部署生成的网页

  `git branch`，`git checkout 分支名称`，查看并切换到创建的分支

  `git pull origin master`，`git push -u origin 新建分支名称`，拉取远程代码，同步分支。

  ## 博客修改后操作

  `git add .`  //添加修改内容到本地仓储
  `git commit -m 'modify blog'`  //提交修改内容到本地仓库
  `git push --set-upstream origin 分支名称`  //配置push，以方便后期直接git push推送
  `git push`  //将本地分支和分支下的内容推送到远程

# 参考链接

* 利用Github分支备份Hexo博客源文件