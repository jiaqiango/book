---
title: Java数据类型
date: 2012-01-04 11:20:33
mermaid: true
categories:
- [java]
tags:
- [java]
---

在JAVA中有2种数据类型
1. 基本数据类型
2. 引用数据类型

```mermaid
graph LR
O[数据类型]
O --> A[基础数据类型]
O --> B[引用初级类型]
A --> B1([整数型])
A --> B2([浮点型])
A --> B3([布尔型])
A --> B4([字符型])
B1 --> C1([byte])
B1 --> C3([short])
B1 --> C4([int])
B1 --> C5([long])
B2 --> D1([float])
B2 --> D2([double])
B3 --> E([boolean])
B4 --> F([char])
B --> G1[对象]
B --> G2[数组]
```

#### 基本数据类型
引用数据类型包括byte,char,short,int,long,float,double,boolean。看下图

* byte 8位内存空间(-128 - 127)
* short 16位内存空间(-32768 - 32767)
* int 32位内存空间(-2147483648 - 2147483647)
* long 64位内存空间(-9223372036854775808 - 9223372036854775807)
* float 32位(1.4E-45 - 3.4028235E38)
* double 64(4.9E-324 - 1.7976931348623157E308)
* char 16位 Unicode 字符(\u0000-\uffff)
* boolean 16

#### 引用数据类型
对象、数组都是引用数据类型。引用类型默认值都是null

#### 数据类型转换

##### 隐示转换

##### 显示转换
