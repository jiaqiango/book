---
title: kettle映射控件
date: 2020-12-15 14:37:40
tags:
categories:
- [kettle]
---

- [Simple mapping (sub-transformation)](#Simple+mapping)
- [映射（子转换）](#映射（子转换）)
- [映射输入规范](#映射输入规范)
- [映射输出规范](#映射输出规范)

##### Simple mapping
是用来配置子转换，对子转换进行调用的一个步骤。子转换可以让相同的业务功能进行重用，抽取出来，方便进行调用
* 注意：这个子转换只有一个输入输出
{% asset_img 1608361013.png %}

##### 映射（子转换）
是用来配置子转换，对子转换进行调用的一个步骤。子转换可以让相同的业务功能进行重用，抽取出来，方便进行调用
* 注意：这个子转换可以多个输入输出
{% asset_img eid8iwp6eg.png %}
配置输入
{% asset_img 1608360840.png %}
配置输出
{% asset_img 1608360894.png %}

##### 映射输入规范
是输入字段，由调用的转换输入
{% asset_img 9gmbva6wtc.png %}

##### 映射输出规范
向调用的转换输出所有列，不做任何处理
{% asset_img eor71soyi8.png %}