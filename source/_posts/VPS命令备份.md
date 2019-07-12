---
title: VPS命令备份
comments: true
abbrlink: ab54e950
date: 2019-06-29 08:13:01
categories:
tags:
---

# VPS命令备份
更新系统
sudo apt-get update && sudo apt-get dist-upgrade
开启BBR
* 修改系统变量
`echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf`
`echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf`
* 检测