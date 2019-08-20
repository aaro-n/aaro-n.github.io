---
title: 虚拟机安装32位Linux
abbrlink: 5694784e
date: 2019-07-17 07:28:00
tags:
---

我需要在虚拟机中安装一个32位的Linux操作系统，找了Ubuntu、Centos、Debian，经过测试选择，确定使用Debian。
## 为什么?
我只所以选择Debian，是因为Ubuntu、Centos不符合我的要求。
Ubuntu：官方主推18.04已经没有32位，最新支持32位的是Ubuntu 16.04 LTS，Ubuntu16.04在VMware使用时有问题，open-vm-tools并没有睡着官方版本更新，软件接着更新，导致在使用时无法复制粘贴。
Centos：Centos 7有官方的32位版本，在安装测试时发现启用第三方软件源出现问题，第三方软件源没有Centos 7 32位版本，淘汰。
## 使用Debian 9 
优点有以下几点：
* 有官方支持的32位版本，软件更新也及时。
* 和Ubuntu类似的软件包管理方式，使用方便。
* 版本支持时间长。