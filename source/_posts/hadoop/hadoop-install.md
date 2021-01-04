---
title: hadoop_install
date: 2020-12-29 14:01:41
tags:
categories: hadoop
---

- [hadoop介绍](#hadoop介绍)
- [记录集连接](#记录集连接)
- [记录关联](#记录关联)

* {% post_link kettle-install 安装kettle %}
* {% post_link kettle-one 编写第一个作业 %}
* {% post_link kettle-control 组件介绍 %}
* {% post_link kettle-demo kettle示例 %}

#### hadoop介绍

#### hadoop下载

#### hadoop安装

#### hadoop配置

#### hadoop异常解决

##### ERROR: but there is no HDFS_NAMENODE_USER defined. Aborting operation.
The root cause of this problem,

hadoop install for different user and you start yarn service for different user. OR
in hadoop config's hadoop-env.sh specified HDFS_NAMENODE_USER and HDFS_DATANODE_USER user is something else.
Hence we need to correct and make it consistent at every place. So a simple solution of this problem is to edit your hadoop-env.sh file and add the user-name for which you want to start the yarn service. So go ahead and edit $HADOOP_HOME/etc/hadoop/hadoop-env.sh by adding the following lines
```shell
export HDFS_NAMENODE_USER=root
export HDFS_DATANODE_USER=root
export HDFS_SECONDARYNAMENODE_USER=root
export YARN_RESOURCEMANAGER_USER=root
export YARN_NODEMANAGER_USER=root
```
##### ERROR: JAVA_HOME is not set and could not be found.
没有配置好java环境变量
第一种临时修改环境变量
`export JAVA_HOME=/usr/java/jdk1.6.0_45`
第二种修改hadoop JAVA_HOME
`cd $HADOOP_HOME/etc/hadoop`
`vim hadoop-env.sh`
```python
# Many of the options here are built from the perspective that users
# may want to provide OVERWRITING values on the command line.
# For example:
#
#  JAVA_HOME=/usr/java/testing hdfs dfs -ls
#
# Therefore, the vast majority (BUT NOT ALL!) of these defaults
# are configured for substitution and not append.  If append
# is preferable, modify this file accordingly.

###
# Generic settings for HADOOP
###

# Technically, the only required environment variable is JAVA_HOME.
# All others are optional.  However, the defaults are probably not
# preferred.  Many sites configure these options outside of Hadoop,
# such as in /etc/profile.d

# The java implementation to use. By default, this environment
# variable is REQUIRED on ALL platforms except OS X!
export JAVA_HOME=/root/java/jdk1.8.0_271

# Location of Hadoop.  By default, Hadoop will attempt to determine
# this location based upon its execution path.
# export HADOOP_HOME=

# Location of Hadoop's configuration information.  i.e., where this
# file is living. If this is not defined, Hadoop will attempt to
# locate it based upon its execution path.
#
# NOTE: It is recommend that this variable not be set here but in
# /etc/profile.d or equivalent.  Some options (such as
# --config) may react strangely otherwise.
#
# export HADOOP_CONF_DIR=${HADOOP_HOME}/etc/hadoop

# The maximum amount of heap to use (Java -Xmx).  If no unit
# is provided, it will be converted to MB.  Daemons will
# prefer any Xmx setting in their respective _OPT variable.
# There is no default; the JVM will autoscale based upon machine
# memory size.
# export HADOOP_HEAPSIZE_MAX=
```

##### Permission denied (publickey,gssapi-keyex,gssapi-with-mic,password).
