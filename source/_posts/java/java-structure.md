---
title: Java程序结构
date: 2021-01-04 15:37:56
categories:
- [java]
tags:
- [java]
---

我们看一个最简单的java程序。我们运行这个程序会向控制台输出`Hello, world!`
```java
public class Main {
    public static void main(String[] args) {
        // 向屏幕输出文本:
        System.out.println("Hello, world!");
    }
} 
```

- public 访问修饰符
- class 定义类的关键词
- Main 类名
- static 表示当前是静态方法
- void 程序运行结束后返回类型
- main 程序入口方法


#### 修饰符
java中有4种修饰符 `default `,`public`,`private`,`protected`。作用在：类、接口、变量、方法
1. default：（默认修饰符，不指定就是default）在同一包内可见，不使用任何修饰符。使用对象：类、接口、变量、方法
2. public：对所有类可见
3. private：在同一类内可见
4. protected：对同一包内的类和所有子类可见

#### 类名
