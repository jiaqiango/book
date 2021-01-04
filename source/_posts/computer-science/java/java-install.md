---
title: Java安装&&配置
date: 2012-01-04 11:16:54
categories:
- [计算机科学, java]
tags:
- [java]
---

- [Java介绍](#Java介绍)
- [Java安装](#Java安装)
- [Java配置](#Java配置)


#### Java介绍
Java最早是由SUN公司（已被Oracle收购）的詹姆斯·高斯林（高司令，人称Java之父）在上个世纪90年代初开发的一种编程语言，最初被命名为Oak，目标是针对小型家电设备的嵌入式应用，结果市场没啥反响。谁料到互联网的崛起，让Oak重新焕发了生机，于是SUN公司改造了Oak，在1995年以Java的名称正式发布，原因是Oak已经被人注册了，因此SUN注册了Java这个商标。随着互联网的高速发展，Java逐渐成为最重要的网络编程语言

Java介于编译型语言和解释型语言之间。编译型语言如C、C++，代码是直接编译成机器码执行，但是不同的平台（x86、ARM等）CPU的指令集不同，因此，需要编译出每一种平台的对应机器码。解释型语言如Python、Ruby没有这个问题，可以由解释器直接加载源码然后运行，代价是运行效率太低。而Java是将代码编译成一种“字节码”，它类似于抽象的CPU指令，然后，针对不同平台编写虚拟机，不同平台的虚拟机负责加载字节码并执行，这样就实现了“一次编写，到处运行”的效果。当然，这是针对Java开发者而言。对于虚拟机，需要为每个平台分别开发。为了保证不同平台、不同公司开发的虚拟机都能正确执行Java字节码，SUN公司制定了一系列的Java虚拟机规范。从实践的角度看，JVM的兼容性做得非常好，低版本的Java字节码完全可以正常运行在高版本的JVM上

#### Java安装
打开Oracle网站[下载JDK](https://www.oracle.com/java/technologies/javase-downloads.html)
{% asset_img 1609742342.png %}
下载的时候可能需要登入账号
#### Java配置
##### window系统
配置JAVA_HOME
{% asset_img 1609742725.png %}
配置PATH
{% asset_img 1609742812.png %}
##### linux系统
###### 临时配置
```shell
export JAVA_HOME=/usr/local/jdk1.8.0_60
export PATH=$JAVA_HOME/bin:$PATH
```
###### 永久配置
Radhat/Centos编辑 `vim .bash_profile`
Debian/Ubuntu编辑 `vim .bashrc`
```shell
# .bash_profile

# Get the aliases and functions
if [ -f ~/.bashrc ]; then
        . ~/.bashrc
fi

# User specific environment and startup programs
JAVA_HOME=/usr/local/jdk1.8.0_60
PATH=$JAVA_HOME/bin:$PATH:$HOME/bin

export JAVA_HOME
export PATH
```

##### 测试安装

```shell
root@iZ2ze194ik3s5at2cz2dahZ:~# java -version
java version "1.8.0_60"
Java(TM) SE Runtime Environment (build 1.8.0_60-b27)
Java HotSpot(TM) 64-Bit Server VM (build 25.60-b23, mixed mode)
```