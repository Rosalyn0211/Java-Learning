# Java-Learning
## Java语言概述

### Java技术体系平台
 - Java SE(Java Standard Edition)标准版：支持桌面级应用的Java平台，提供了完整的Java核心API。  

 - Java EE(Java Enterprise Edition)企业版，是为开发企业环境下的应用程序提供的一套解决方案。该技术体系中包含的技术主要针对于Web应用程序开发。  

 - Java ME(Java Micro Edition)小型版，支持Java程序运行在移动终端上的平台。  

 - Java Card：支持一些Java小程序运行在小内存设备上的平台

### Java语言的特点
 - 面向对象
 - 健壮性
 - 跨平台性
 
### JVM & JDK & JRE
 - JVM(Java Virtual Machine)是一个虚拟的计算机，具有指令集并使用不同的存储区域。负责执行指令，管理数据、内存、寄存器。实现了“一次编译，到处运行”。  

 - JDK(Java Development Kit) = JRE + 开发工具（编译工具javac.exe、打包工具jar.exe）  

 - JRE(Java Runtime Environment) = JVM + Java程序核心类库

### 配置环境变量
根据windows系统查找可执行程序的原理，可将Java工具所在路径定义到Path环境变量中。

### 注释
```
//单行注释
```
<br>   

```
/*  

多行注释  

*/  
```
<br>   

```
/**  

文档注释  

Java特有  

注释内容可以被JDK提供的工具javadoc所解析，生成一套以网页文件形式体现的该程序的说明文档。  

操作方式：javadoc -d mydoc -author -version HelloWorld.java  

*/
```

### 注意事项
 - Java源文件是以java为扩展名。源文件的基本组成是类（class）。  

 - Java应用程序的执行入库时main()方法。固定书写格式： public static void main(String[]args){ }  

 - Java语言严格区分大小写。  

 - Java方法由语句构成，每个语句以“;”结束。  

 - 一个源文件中最多只能由一个public类。其他类的个数不限，如果源文件中包含一个public类，则文件名必须按该类名命名。
 
## Java基本语法

### 关键字和保留字
 - 关键字：被Java赋予了特殊含义，用做专门用途的字符串，关键字中所有字母均为小写。
 ![image](images/关键字.png)
 ![image](images/关键字2.png)
 - 保留字：现有Java版本尚未使用，但以后版本可能会作为关键字使用。(goto,const)

### 标识符
 - 标识符：Java对各种变量、方法和类等要素命名时使用的字符序列。    

 - 定义合法标识符规则：
    - 由英文字母大小写，数字，_和$组成。
    - 数字不可开头
    - 不可使用关键字和保留字
    - 严格区分大小写，长度无限制
 
 - Java名称命名规范  
    - 包名：多单词组成时所有字母都小写
    - 类名、接口名：多单词组成时，所有单词的首字母大写
    - 变量名、方法名：多单词组成时，第一个单词首字母小写，第二个单词开始每个单词首字母大写
    - 常量名：所有字母都大写，多单词时用下划线连接  
 
 ### 变量
 - 变量包含：变量类型，变量名和存储的值  

 - 使用变量注意：
    - Java中每个变量必须先声明后使用
    - 变量的作用域：其定义所在的一对{}内

 - 变量的分类
    - 按数据类型  
   
     ![image](images/数据类型.png)
    - 按声明位置的不同  
   
     ![image](images/变量类型.png)
  
  
 - 整数类型：byte,short,int,long   
 
   ![image](images/整数类型.png)

    - Java整型变量默认为int，声明long型常量需后加‘L’或‘l’
 
 - 浮点类型：float,double  
    - float：单精度，尾数可精确到7位有效数字，需后加‘f’
    - double：双精度，浮点型默认类型  
 

 - 字符类型：char   
    - '单个字母'
    - Java中的所有字符都是用Unicode编码。因此，char类型是可以进行运算的。  



 - Boolean类型  
    - 只允许取值true和false，无null。  
    - 不可使用0或非0的整数替代false和true。
    - Java虚拟机中没有任何boolean值专用的字节码指令，编译后用int数据类型代替。

 - 基本数据类型转换

    - 自动类型转换：  
   
   ![image](images/基本数据类型转换.png)

 - 注意：
    - 当把任何基本数据类型的值和字符串进行连接运算时，基本数据类型的值将自动转化为字
符串类型。
    - byte,short,char之间进行运算时转换为int类型

 - 字符串类型：String  
    - String不是基本数据类型，属于引用数据类型

 - 强制类型转换
    - 自动类型转换的逆过程，将容量大的数据类型转换为容量小的数据类型。使用时要加上强制转换
符：()，但可能造成精度降低或溢出。
    - 通常字符串不能转换为基本类型，但可通过基本类型对应的包装类则可实现。   
    String a = "43"; int i = Integer.parselnt(a);
    - boolean类型不可以转换为其他的数据类型
 
 ### 运算符
 - 算数运算符

![image](images/运算符.png)

   - +除字符串相加功能外，还能把非字符串转换成字符串  
   例如：System.out.println (“5+ 5+5); // 打印结果是5+5=55
 
 - 赋值运算符
    - =当 “=”两侧数据类型不一致时，可以使用自动类型转换或使用强制类型转换原则进行处理。
 
 - 比较运算符

![image](images/比较运算符.png)

 - 逻辑运算符

![image](images/逻辑运算符.png)

 - 位运算符

![image](images/位运算符.png)

 - 三元运算符

![image](images/三元运算符.png)

### 程序流程控制

#### if-else结构
例：  

```
public class AgeTest{
    public static void main(String args[]){
    int age = 18;
    if(age<0){
            System.out.println("错误");
    }else if(age>250){
            System.out.println("超过范围")；
    }else{
             System.out.println("年龄："+ age);
    }
   }   
 }
 ```
 
#### switch-case结构
```
switch(表达式）{  
case 常量1：  
     语句1；       
     //break;       
case 常量2：  
     语句2；       
     //break;  
…    
default：  
     语句；  
     //break  
```     
  - switch(表达式)中表达式的值必须是下述几种类型之一：byte，short，char，int，枚举(jdk5.0)，String(jdk7.0)
  - case子句中的值必须是常量
  
 #### for循环
```
for(①初始化部分;②循环条件部分;④迭代部分){  
     ③循环体部分       
 }
```

 - 初始化部分可以声明多个变量，但必须是同一个类型，用逗号分隔
 
 #### while循环
``` 
 ①初始化部分；     
 while(②循环条件部分){  
     ③循环体部分；       
     ④迭代部分；  
 }  
```
#### do-while循环
```
①初始化部分；     
 do{   
     ③循环体部分；       
     ④迭代部分；  
 }while(②循环条件部分)；  
 ```    
     
## 数组
### 数组的概述
 - 数组本身是引用数据类型，而数组中的元素可以是任何数据类型。
 - 创建数组对象会在内存中开辟一整块连续的空间，而数组中引用的是这块连续空间的首地址。
 - 数组的长度一旦确定，就不能修改。
### 一维数组的使用
#### 声明
- 一维数组的声明方式：type var[]或type[] var;
 ```
 int a[];
 int[] a1;
 double b[];
 String[] c; //引用类型变量数组
 ```
 - Java中声明数组时不能指定其长度，例如：int a[5];
 #### 初始化
 - 动态初始化：数组声明且为数组元素分配空间与复制的操作分开进行
 ```
 int[] arr = new int[3];
 arr[0] = 3;
 arr[1] = 9;
 arr[2] = 8;
 String names[];
 names = new String[3]
 names[0] = Mike;
 names[1] = Jane;
 names[2] = Linda;
 ```
  - 静态初始化：在定义数组的同时就为数组元素分配空间并赋值。
  ```
  int arr[] = new int[]{3,9,8};
  int[] arr = {3,9,8};
  ```
  #### 数组元素的默认初始化值
 ![images](images/数组的默认初始化值.png)
 
 ### 多维数组的使用
 ![images](images/二维数组的使用1.png)   
 
 ![images](images/二维数组的使用2.png) 
 
 ### Arrays工具类的使用
 ![images](images/数组工具使用.png)

### 练习
 - 从键盘读入学生成绩，找出最高分，并输出学生成绩等级。
 ```
package array;

import java.util.Scanner;

public class ArrayDemo1 {
	public static void main(String[] args) {
		Scanner scanner = new Scanner(System.in);
		System.out.println("请输入学生人数：");
		int number = scanner.nextInt();
		int scores[] = new int[number];
		System.out.println("请输入"+number+"个学生成绩：");
		for(int i = 0; i < scores.length; i++) {
			scores[i] = scanner.nextInt();	
		}
		int maxScore = 0;
		for(int i = 0; i < scores.length;i++) {
			if(scores[i] > maxScore) {
				maxScore = scores[i];		
			}	
		}
		char level;
		for(int i = 0;i < scores.length; i++) {
			if(maxScore - scores[i] < 10) {
				level = 'A';
			}else if(maxScore - scores[i] <=20 ) {
				level = 'B';
			}else if(maxScore - scores[i] <= 30) {
				level = 'C';					
			}else{
				level = 'D';
			}
			System.out.println("student"+i+"'grade is "+level);
		}		
	}
}
```

 - 使用二维数组打印一个10行杨辉三角。
 ```
 package array;

public class ArrayDemo3 {
	public static void main(String[] args) {
		int[][] arr = new int[10][];
		for(int i = 0; i < arr.length;i++) {
			arr[i] = new int[i+1];
			arr[i][0] = 1;
			arr[i][i] = 1;
			if(i > 1) {
				for(int j = 1; j < i; j++) {
					arr[i][j] = arr[i-1][j-1]+arr[i-1][j];
				}
			}
		}
		for(int i = 0; i < arr.length; i++) {
			for(int j = 0; j < arr[i].length; j++) {
				System.out.print(arr[i][j] + " ");
			} 
			System.out .println();
		}
	}
}
```
 - 数组的复制与反转
 ```
 package array;

public class ArrayDemo4 {
	public static void main(String[] args) {
		int[] arr1,arr2;
		arr1 = new int[] {2,3,5,7,11,13};
		for(int i = 0; i < arr1.length; i++) {
			System.out.print(arr1[i]+"\t");
		}
		//数组的复制
		//arr2 = arr1; 不是真正的数组的复制，只是地址值的复制，修改其一另一个也会改变。
		arr2 = new int[arr1.length];
		for(int i = 0; i < arr1.length; i++) {
			arr2[i]=arr1[i];
		}
		//数组的反转
		for(int i = 0;i < arr1.length / 2;i++) {
			int temp = arr1[i];
			arr1[i] = arr1[arr1.length-i-1];
			arr1[arr1.length-i-1] = temp;
		}
	}

}
```
 - 数组的顺序查找
 ```
 package array;

public class LinearSearch {
	public static void main(String[] args) {
		String[] arr = new String[] {"a","b","c","d","e"};
		String dest = "c";
		boolean isflag = true;
		for(int i = 0; i < arr.length; i++) {
			if(dest.equals(arr[i])) {
				System.out.println("找到了指定元素，位置为"+i);
				isflag = false;
				break;				
			}
		}
		if(isflag) {
			System.out.println("未找到指定元素");
		}		
	}
}
```
 - 数组的二分法查找
 ```
 package array;

public class BinarySearch {
	public static void main(String[] args) {
		int[] arr = new int[] {-34,-25,-10,3,7,18,29,37,98};
		int dest = 37;
		int head = 0;
		int end = arr.length - 1;
		boolean isflag = true;
		while(head <= end) {
			int mid = (head + end) / 2;
			if(dest == arr[mid]) {
				System.out.println("找到了指定元素，索引位置为" + mid);
				isflag = false;
				break;
			}else if(dest < arr[mid]) {
				end = mid - 1;				
			}else {
				head = mid + 1;
			}
		}
		if(isflag) {
			System.out.println("未找到指定元素");
		}
	}
}
```

## 排序算法
### 衡量排序算法的优劣
 - 时间复杂度：分析关键字的比较次数和记录的移动次数
 - 空间复杂度：分析排序算法中需要多少辅助内存
 - 稳定性：若记录的A和B的关键字值相等，但排序后A和B的值保持不变，则称这种排序算法是稳定的
### 排序算法的分类
- 内部排序：不需要借助外部存储器
- 外部排序：必须借助外部存储器
### 十大内部排序算法
 - 选择排序
    - 直接选择排序，堆排序
 - 交换排序
    - 冒泡排序，快速排序
 - 插入排序
    - 直接插入排序，折半插入排序，Shell排序
 - 并归排序
 - 桶式排序
 - 基数排序
### 冒泡排序
 - 基本思想:依次比较相邻元素，若逆序则交换。
 ```
 package sort;

public class BubbleSort {
	public static void main(String[] args) {
		int[] arr = new int[] {89,7,46,34,95,19,0,-2,-87,89,66,-54};
		for(int i = 0; i < arr.length - 1; i++) {
			for(int j = 0; j < arr.length - 1 - i;j++) {
				if(arr[j] > arr[j+1]) {
					int temp = arr[j];
					arr[j] = arr[j + 1];
					arr[j + 1] = temp;
				}
			}
		}
		for(int i = 0;i < arr.length; i++) {
			System.out.print(arr[i] + " ");
		}
	}
}
```
### 快速排序
 - 基本思想：任取待排序的某个元素作为标准，通过一次划分，将待排元素分为左右两个子序列，对子序列继续进行划分。
```
package sort;


public class QuickSort {
	private static void swap(int[] data, int i, int j) {
		int temp = data[i];
		data[i] = data[j];
		data[j] = temp;
	}

	private static void subSort(int[] data, int start, int end) {
		if (start < end) {
			int base = data[start];
			int low = start;
			int high = end + 1;
			while (true) {
				while (low < end && data[++low] - base <= 0)
					;
				while (high > start && data[--high] - base >= 0)
					;
				if (low < high) {
					swap(data, low, high);
				} else {
					break;
				}
			}
			swap(data, start, high);
			
			subSort(data, start, high - 1);//递归调用
			subSort(data, high + 1, end);
		}
	}
	public static void quickSort(int[] data){
		subSort(data,0,data.length-1);
	}
	
	
	public static void main(String[] args) {
		int[] data = { 9, -16, 30, 23, -30, -49, 25, 21, 30 };
		System.out.println("排序之前：\n" + java.util.Arrays.toString(data));
		quickSort(data);
		System.out.println("排序之后：\n" + java.util.Arrays.toString(data));
	}
}
```
## 面向对象编程(上)
### 面向过程(POP)与面向对象(OOP)
 - 面向过程，强调的时功能行为，以函数为最小单位；
 - 面向对象，将功能封装进对象，强调具备了功能的对象，以类/对象为最小单位。
 - 面向对象的三大特征
   - 封装
   - 继承
   - 多态
### 类和对象
 - 类和对象时面向对象的核心概念
    - 类是对一类事物的描述，是抽象的，常见的类的成员有：属性（对应类中的成员变量），行为（对应类中的成员方法）
    - 对象是实际存在的该类事物的每个个体，因而也称为实例 
 - 类的语法格式
 ![images](images/类的语法格式.png)
### 对象的创建和使用
 - 创建对象语法：类名 对象名 = new 类名();
 - 使用 对象名.对象成员 访问对象成员包括属性和方法
 - 类的访问机制：
    - 在一个类中的访问机制：类中的方法可以直接访问类中的成员变量。
       （例外：static方法访问非static，编译不通过。）
    - 在不同类中的访问机制：先创建要访问类的对象，再用对象访问类中定义的成员。
 - 内存解析
    - 堆：存放对象实例，所有的对象实例以及数组都要再堆上分配。
    - 栈：虚拟机栈，存储局部变量等，局部变量表存放了编译器可知长度的各种基本数据类型、对象引用。方法执行完，自动释放。
    - 方法区：存储已知被虚拟机加载的类信息、常量、静态变量、即时编译器编译后的代码等数据。
     ![images](images/内存解析.png)
 - 匿名对象
    - 匿名对象：我们可以不定义对象的句柄，而直接调用这个对象的方法。如：new Person().shout();
    - 如果对一个对象只需要进行一次方法调用，那么就可以使用匿名对象。
    - 我们经常将匿名对象作为实参传递给一个方法调用。
### 类的成员之一————属性(field)
 - 语法格式：修饰符 数据类型 属性名 = 初始化值;
    - 常用的权限修饰符：private、缺省、protected、public
    - 其他修饰符：static、final、
 - 变量的分类：成员变量与局部变量
    - 在方法体外，类体内声明的变量称为成员变量。包括实例变量（不以static修饰），类变量（以static修饰）。
    - 在方法体内部声明的变量成为局部变量。包括形参（方法、构造器中定义的变量），方法局部变量（再方法内定义），代码块局部变量（在代码块中定义）。
    - 二者均有生命周期；局部变量除形参外，均需显示初始化。
      ![images](images/变量.png)
### 类的成员之二————方法(method)
 - 什么是方法？
    - 方法是类或对象行为特征的抽象，用来完成某个功能操作。Java里的方法不能独立存在，所有的方法必须定义在类里。
 - 声明格式：
 
 
```
 修饰符 返回值类型 方法名(参数类型 形参1，参数类型 形参2，……){
     方法体程序
     return 返回值;
 }
```



    - 修饰符：public，缺省，private，protected等
    - 返回值类型：
       - 没有返回值：void
       - 有返回值：声明返回值的类型
 - 没有具体返回值的情况，返回值类型用关键字void表示，那么方法体中可以不必使用return语句。
 - 方法中只能调用方法或属性，不可以在方法内部定义方法。
 - 方法的重载
    - 概念：在同一个类中，允许存在一个以上的同名方法，只要它们的参数个数或参数类型不同即可。
    - 特点：与返回值类型无关，只看参数列表，且参数列表必须不同。调用时，根据方法参数列表的不同来区别。
 - 可变个数的形参
    - JavaSE 5.0中提供Varargs机制，允许直接定义能和多个实参相匹配的形参。
 ![images](images/可变个数的形参.png)  
 
    - 可变参数的个数：0个，1个或多个
    - 方法的参数部分有可变形参，需要放在形参声明的最后
    - 在一个方法的形参位置，最多只能声明一个可变个数形参
 - 变量的赋值
    - 如果变量是基本数据类型（ byte（字节型）、short（短整型）、int（整型）、long（长整型）、float（单精度浮点型）、double（双精度浮点型）、boolean（布尔型）、char（字符型）），此时赋值的是变量所保存的数据值。
    - 如果变量是引用数据类型，此时复制的是变量所保存的数据的地址值。
 - 方法形参的传递机制：值传递
    - 形参是基本数据类型：将实参基本数据类型变量的“数据值”传递给形参
    - 形参是引用数据类型：将实参引用数据类型变量的“地址值”传递给形参
 - 递归方法：一个方法体内调用它自身
    - 方法递归包含了一种隐式的循环，他会重复执行某段代码，但这种重复执行无需循环控制。
    - 递归一定要向已知方向递归，否则这种递归就i变成了无穷递归，类似于死循环。
 
### 面向对象特征之一：封装和隐藏
Java中通过将数据声明为私有的(private)，再提供公共的(public)方法: getXxx 和 setXxx 实现对该属性的操作,以实现下述目的：  
 - 隐藏一个类中不需要对外提供的实现细节；
 - 使用者只能通过事先定制好的方法来访问数据,可以方便地加入控制逻辑,限制对属性的不合理操作；
 - 便于修改,增强代码的可维护性；  
 
![image](images/权限修饰符.png)

### 类的成员之三————构造器
 - 构造器的特征
    - 它具有与类相同的名称
    - 它不声明返回值类型。（与声明为void不同）
    - 不能被static、final、synchronized、abstract、native修饰，不能有return语句返回值
 - 构造器的作用：创建对象；给对象进行初始化，如Person p = new Person("Peter",15)
 - 构造器的分类：
    - 隐式无参构造器（系统默认提供）
    - 显式的定义一个或多个构造器（无参、有参）
 - 注意点
    - 一旦显式的定义了构造器，则系统不在提供默认构造器
### 属性赋值过程
 - 赋值的位置
    - 默认初始化
    - 显式初始化
    - 构造器中初始化
    - 通过“对象.属性”或“对象.方法”的方式赋值
  - 赋值的先后顺序：从上到下（后面覆盖前面的）

### 关键字————this
 - this修饰属性和方法
    - 我们可以使用this来区分属性和局部变量，如this.name = name;可以理解为当前对象的name属性 = 形参name。  
    - 当形参与成员变量同名时，如果在方法内或构造器内需要使用成员变量，必须添加this来表明该变量是类的成员变量。
 - this调用构造器
    - 我们在类的构造器中，可以显式的使用“this(形参列表)”方式，调用本类中指定的其他构造器。
    - this调用构造器必须放在首行，最多只能有一个。

### 关键字————package
 - 使用package声明类或接口所属的包，声明在文件的首行
 - 每“.”一次就代表一层文件目录。


 ### 练习
  - 创建一个Person类
 ```
 package oop;

public class Person {
	String name;
	int age;
	/**
	 * sex:1表示男性
	 * sex:2表示女性
	 */
	int sex;
	
	public void study() {
		System.out.println("studying");
	}
	public void showAge() {
		System.out.println("age:" + age);	
	}
	public int addAge(int i) {
		age += i;
		return age;
	}
}

 package oop;

public class PersonTest {
	public static void main(String[] args) {
		Person p1 = new Person();
		
		p1.name = "Tom";
		p1.age = 18;
		p1.sex = 1;
		
		p1.study();
		p1.showAge();
		int newAge = p1.addAge(2);
		System.out.print(p1.name + "的新年龄为" + newAge + "岁");
	}
}
```
 - 利用面向对象的编程方法，设计类 Circle 计算圆的面积。
 ```
 package oop;

public class Circle {
	double radius;
	
	public double findArea() {
		double area = Math.PI * radius * radius;
		return area;
	}

}
package oop;

public class CircleTest {
	public static void main(String[] args) {
		
		Circle c1 = new Circle();		
		c1.radius = 5;		
		double area = c1.findArea();
		System.out.println(area);
	}

}
```

 - 将对象作为参数传递给方法
```
public class PassObject {
	public static void main(String[] args) {
		PassObject test = new PassObject();
		Circle c = new Circle();
		test.printAreas(c, 5);
		System.out.println("now radius is" + c.radius)
	}
	public void printAreas(Circle c, int time) {
		System.out.println("Radius\t\tArea");
		//设置圆的半径
		for(int i = 1;i <= time;i++) {
			c.radius = i;
			System.out.println(c.radius + "\t\t" + c.findArea());
		}
		c.radius = time + 1
	}
}
```
 - 递归方法
```
public class recursion {
	public int f(int n) {
		if(n == 0) {
			return 1;
		}else if(n == 1) {
			return 4;
		}else {
			return 2*f(n-1) + f(n - 2);
		}
	}
}
```
 - 封装性
 ```
public class NewPerson {
	private int age;
	public void setAge(int a ) {
		if(a<0 || a > 130) {
			System.out.println("传入的数据非法");
			return;
		}
		age = a;				
	}
	public int getAge() {
		return age;
	}
}
public class NewPersonTest {
	public static void main(String[] args) {
		NewPerson p1 = new NewPerson();
		p1.setAge(12);
		System.out.println("年龄为" + p1.getAge());
	}

}
```
