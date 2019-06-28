---
title: 评论定时任务
abbrlink: 5d26ab24
date: 2019-02-16 06:54:28
tags:
---
# 调整Valine定时任务
## 美国节点安装Valine
按照[Valine Admin 配置手册](https://deserts.io/valine-admin-document/)进行安装配置，进行测试。
## 问题
 在Leancloud后台发现定时需要调整，经过发现需要将定时任务调整如下到：`0 0/30 7-23 * * ?`修改为`0 0/30 23-15 * * ?`，邮件漏发自行调整。