---
title: OLAINDEX使用Memcached缓存
comments: true
abbrlink: fcd3b03b
date: 2019-09-09 19:34:14
categories:
tags:
---

OLAINDEX默认使用文件缓存，使用Memcache缓存提高效率。

# 前提

1.OLAINDEX 已经部署完成。

2.PHP启用Memcache扩展

# 启用

## 禁用文件缓存

修改.env文件中的“缓存配置”，在配置前加#号，即：

`# 缓存配置
#file/memcached/redis
#CACHE_DRIVER=file
#QUEUE_CONNECTION=sync
#SESSION_DRIVER=file
#SESSION_LIFETIME=120`

## 查询Memcached的使用端口

命令`ps -ef | grep memcached`

输出 

`root       556     1  0 Sep08 ?        00:01:21 /usr/local/memcached/bin/memcached -d -l 127.0.0.1 -p 11211 -u root -m 64 -c 1024 -P /var/run/memcached.pid
www        956     1  0 Sep08 ?        00:00:56 memcached -p 11212 -d
www      16356 16350  0 20:42 pts/0    00:00:00 grep memcached`

有两个端口，分别是 11211 和 11212

## 设置

CACHE_DRIVER=memcached  #选择memcached缓存

MEMCACHED_HOST=127.0.0.1 #memcached缓存 iP

MEMCACHED_PORT=11211 #缓存端口

MEMCACHED_PASSWORD= #未使用

## 清理缓存

`php artisan config:cache`

