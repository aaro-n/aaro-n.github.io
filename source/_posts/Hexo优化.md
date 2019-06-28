---
title: Hexo优化
tags:
  - Hexo
  - 优化
abbrlink: 7b3ddb57
date: 2019-02-16 06:54:28
---

## 主要记录Hexo 的设置，以便恢复

启用阅读统计注意事项

博客使用基于[LeanCloud](https://us.leancloud.cn)，在使用Next主题时出现问题，发现需将`  

```  
security: true 
betterPerformance: false
```
修改成

```  
security: false
betterPerformance: false
```
否则无法使用阅读统计。
### Hexo增强

* 添加阅读时间

``sudo npm install hexo-symbols-count-time --save
``
[参考链接](https://github.com/theme-next/hexo-symbols-count-time)
* 添加本地搜索

``sudo npm install hexo-generator-searchdb --save``
[参考链接](https://github.com/theme-next/hexo-generator-searchdb)

* RSS输出

安装扩展

```
sudo npm install --save hexo-generator-feed
```

在博客配置文件尾端添加

```
plugins: hexo-generate-feed
```

在主题配置文搜索RSS修改为

```
rss: /atom.xml
```




* 添加网站地图

  安装扩展
  
  ``` 
  sudo npm install hexo-generator-sitemap --save
sudo npm install hexo-generator-baidu-sitemap --save 
  ```
  
  修改博客配置文集
  
  ``` 
  sitemap: 
    path: sitemap.xml
  baidusitemap:
    path: baidusitemap.xml
  
  url: https://blog.itansuo.info
  ```
  

## 本文历史
* 19年5月20日，添加网站地图、本地搜索、RSS输出