---
title: "SCRAPY"
date: 2022-03-12T18:10:08+08:00

---

# PYTHON爬虫系列

## 定义存储字段和管道类

items.py 主要用于存储对象 

	Item对象

pipeline.py 用于实现对象存储（歌曲入库）和对象操作（歌曲下载）

	触发对Item对象的操作，实现类初始化和数据库连接。

## Spider开发之Get请求和Post请求
Post是传递参数（需要搜索的参数）到服务器，而Get请求是指明url。

Selector选择器会用XPATH和CSS表达式选择HTML中的部分数据。

然后用可以重用的Item pipelines进行文件下载和保存。

## SCRAPY爬虫的运行方式

1. 调度器中取出URL封装成Request请求给下载器
1. 资源下载后封装成Response
1. 解析出实体Item给pipeline处理
1. 解析出URL则给调度器等待抓取
