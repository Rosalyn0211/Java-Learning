# Java语言概述

### Java技术体系平台
Java SE(Java Standard Edition)标准版：支持桌面级应用的Java平台，提供了完整的Java核心API。  

Java EE(Java Enterprise Edition)企业版，是为开发企业环境下的应用程序提供的一套解决方案。该技术体系中包含的技术主要针对于Web应用程序开发。  

Java ME(Java Micro Edition)小型版，支持Java程序运行在移动终端上的平台。  

Java Card：支持一些Java小程序运行在小内存设备上的平台

### Java语言的特点
 - 面向对象
 - 健壮性
 - 跨平台性
 
### JVM & JDK $ JRE
JVM(Java Virtual Machine)是一个虚拟的计算机，具有指令集并使用不同的存储区域。负责执行指令，管理数据、内存、寄存器。实现了“一次编译，到处运行”。  

JDK(Java Development Kit) = JRE + 开发工具（编译工具javac.exe、打包工具jar.exe）  

JRE(Java Runtime Environment) = JVM + Java程序核心类库

### 配置环境变量
根据windows系统查找可执行程序的原理，可将Java工具所在路径定义到Path环境变量中。

### 注释
//单行注释

<br>   


/*  

多行注释  

*/  

<br>   


/**  

文档注释  

Java特有  

注释内容可以被JDK提供的工具javadoc所解析，生成一套以网页文件形式体现的该程序的说明文档。  

操作方式：javadoc -d mydoc -author -version HelloWorld.java  

*/

### 注意事项
 - Java源文件是以java为扩展名。源文件的基本组成是类（class）。  

 - Java应用程序的执行入库时main()方法。固定书写格式： public static void main(String[]args){ }  

 - Java语言严格区分大小写。  

 - Java方法由语句构成，每个语句以“;”结束。  

 - 一个源文件中最多只能由一个public类。其他类的个数不限，如果源文件中包含一个public类，则文件名必须按该类名命名。

