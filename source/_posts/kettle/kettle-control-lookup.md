---
title: kettle查询控件
date: 2020-12-15 14:37:03
tags:
categories:
- [kettle]
---

- [Column exists](#Column+exists)
- [数据库查询](#数据库查询)
- [数据库连接](#数据库连接)
- [检查表是否存在](#检查表是否存在)
- [流查询](#流查询)
- [调用DB存储过程](#调用DB存储过程)

##### Column exists
检查表指定的字段是否存在(结果字段名是Boolean类型)
{% asset_img 1608347285.png %}

##### 数据库查询
数据库里面的左连接。左连接就是两张表执行左关联查询，把左边的表数据全部查询出来
{% asset_img tvsh4rqhbe.png %}

##### 数据库连接
可以执行两个数据库的查询，和单参数的表输入
{% asset_img bwow6hdwwx.png %}

##### 检查表是否存在
和[Column exists](#Column+exists)一样，只不过这个检查表是否存在
{% asset_img 1608347618.png %}

##### 流查询
查询前把数据都加载到内存中，并且只能进行等值查询
{% asset_img 1kuxfvetmu.png %}

##### 调用DB存储过程
执行数据库的存储过程
{% asset_img 1608347827.png %}