---
title: kettle流程控件
date: 2020-12-15 14:36:20
tags:
categories:
- [kettle]
---

- [Switch/case](#Switch/case)
- [过滤记录](#过滤记录)
- [空操作](#空操作)
- [中止](#中止)
- [检测空流](#检测空流)
- [Blocking step（阻塞数据）](#Blocking+step（阻塞数据）)

##### Switch/case
数据流从一路到多路,等同java中switch
{% asset_img jxe3r6lbml.png %}

##### 过滤记录
从一路到两路,等同java中if
{% asset_img 2k4z2t7s5i.png %}

##### 空操作
数据流的终点
{% asset_img qeacjl4b55.png %}

##### 中止
数据流的终点，如果有数据到这里，将会报错。用来校验数据的时候使用
{% asset_img eslpl1d7w3.png %}

##### 检测空流
如果数据流为空（即数据流不包含任何行），则此步骤将输出一行。 输出行将具有与输入行相同的字段，但是所有字段值将为空（NULL）
如果数据流不为空，则不会输出任何内容
{% asset_img 1608283112.png %}

##### Blocking step（阻塞数据）
有多条数据时，只会通过最后一条数据
{% asset_img 1608283356.png %}

