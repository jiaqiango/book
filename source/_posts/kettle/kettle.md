---
title: kettle
date: 2020-12-14 14:13:49
tags:
categories:
- [kettle]
---

* {% post_link kettle-install 安装kettle %}
* {% post_link kettle-one 编写第一个作业 %}
* {% post_link kettle-control 组件介绍 %}
* {% post_link kettle-demo kettle示例 %}

### ETL介绍
#### ETL是什么
ETL分别是“Extract”、“ Transform” 、“Load”三个单词的首字母缩写也即数据抽取、转换、装载的过程，但我们日常往往简称其为数据抽取

#### ETL工具
ETL的工具功能：必须对抽取到的数据能进行灵活计算、合并、拆分等转换操作
目前，ETL工具的典型代表有:
商业软件：Informatica、IBM Datastage、Oracle ODI、Microsoft SSIS
开源软件：Kettle、Talend、CloverETL、Ketl，Octopus

### Kettle介绍
Kettle是Pentaho的一个组件，主要用于数据库间的数据迁移。
Kettle自己有三个主要组件：Spoon，Kitchen，Pan

#### Spoon
图形化界面工具(GUI方式)，Spoon允许你通过图形界面来设计Job和Transformation，可以保存为文件或者保存在数据库中。
也可以直接在Spoon图形化界面中运行Job和Transformation，
#### Pan
Transformation执行器(命令行方式)，Pan用于在终端执行Transformation，没有图形界面。
#### Kitchen
Job执行器(命令行方式)，Kitchen用于在终端执行Job，没有图形界面。
#### Carte
嵌入式Web服务，用于远程执行Job或Transformation，Kettle通过Carte建立集群。
#### Encr
Kettle用于字符串加密的命令行工具，如：对在Job或Transformation中定义的数据库连接参数进行加密。