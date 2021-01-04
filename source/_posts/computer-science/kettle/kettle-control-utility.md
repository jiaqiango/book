---
title: kettle应用控件
date: 2020-12-15 14:36:09
tags:
categories:
- [计算机科学, kettle]
---

- [写日志](#写日志)
- [替换NULL值](#替换NULL值)
- [延迟行](#延迟行)
- [发送邮件](#发送邮件)
- [比较表](#比较表)
- [设置值为NULL](#设置值为NULL)

##### 写日志
调试的时候使用，把日志信息打印到日志窗口
{% asset_img tg6pt6zv8g.png %}

##### 替换NULL值
把null转换为其它的值。NULL值不好进行数据分析
{% asset_img s1rcuqhu0n.png %}

##### 延迟行
延时处理，每次读取都要延迟输出
{% asset_img 1608281593.png %}

##### 发送邮件
顾名思义就是往邮箱发送邮件，一般情况下都会使用脚本拼装邮件内容
{% asset_img 1608281715.png %}

##### 比较表
比较两个表中的数据（假设它们具有相同的表结构）。它将发现两个表中的数据之间的差异并将其记录下来
{% asset_img 1608282045.png %}

##### 设置值为NULL
如果某个字段等于指定的值，则将该值设置为null。备注：字段是字符串类型
{% asset_img 1608282314.png %}
