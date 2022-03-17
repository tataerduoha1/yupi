# JAVA基础

## 1、内容描述

### SSM

- spring（轻量级的容器框架）
- springMVC（分层的web开发框架）
- mybatis（持久化框架）
- Spring，SpringMVC，SpringBoot，SpringCloud有什么区别和联系

  Spring是一个轻量级的控制反转(IoC)和面向切面(AOP)的容器框架。Spring使你能够编写更干净、更可管理、并且更易于测试的代码。Spring更具体的介绍：https://spring.io/ ；
  Spring MVC是Spring的一个模块，一个web框架。通过Dispatcher Servlet, ModelAndView 和 View Resolver，开发web应用变得很容易。主要针对的是网站应用程序或者服务开发——URL路由、Session、模板引擎、静态Web资源等等；
  Spring配置复杂，繁琐，所以推出了Spring boot，约定优于配置，简化了spring的配置流程；
  Spring Cloud构建于Spring Boot之上，是一个关注全局的服务治理框架。
  
  总接下来：
  Spring是核心，提供了基础功能；
  Spring MVC 是基于Spring的一个 MVC 框架 ；
  Spring Boot 是为简化Spring配置的快速开发整合包；
  Spring Cloud是构建在Spring Boot之上的服务治理框架。
  查看：https://www.zhihu.com/question/332686495
  
  
	- spring

	  spring是一个一站式的轻量级的java开发框架，核心是控制反转（IOC）和面向切面（AOP），针对于开发的WEB层(springMvc)、业务层(Ioc)、持久层(jdbcTemplate)等都提供了多种配置解决方案；
	  springMvc是spring基础之上的一个MVC框架，主要处理web开发的路径映射和视图渲染，属于spring框架中WEB层开发的一部分；
	  
	- springMVC

	  springMvc属于一个企业WEB开发的MVC框架，涵盖面包括前端视图开发、文件配置、后台接口逻辑开发等，XML、config等配置相对比较繁琐复杂；
	  springBoot框架相对于springMvc框架来说，更专注于开发微服务后台接口，不开发前端视图，同时遵循默认优于配置，简化了插件配置流程，不需要配置xml，相对springmvc，大大简化了配置流程；
	  区别于springMvc的是，springBoot专注于微服务方面的接口开发，和前端解耦，虽然springBoot也可以做成springMvc前后台一起开发，但是这就有点不符合springBoot框架的初衷了；
	  
	- springboot

	  spring boot使用了默认大于配置的理念，集成了快速开发的spring多个插件，同时自动过滤不需要配置的多余的插件，简化了项目的开发配置流程，一定程度上取消xml配置，是一套快速配置开发的脚手架，能快速开发单个微服务；
	  spring cloud大部分的功能插件都是基于springBoot去实现的，springCloud关注于全局的微服务整合和管理，将多个springBoot单体微服务进行整合以及管理； springCloud依赖于springBoot开发，而springBoot可以独立开发；
	  
	- springcloud

	  对于springCloud框架来说，它和springBoot一样，注重的是微服务的开发，但是springCloud更关注的是全局微服务的整合和管理，相当于管理多个springBoot框架的单体微服务
	  
	- 联系

		- 

## 2、JAVA 概述

### Java 技术体系平台

- Java SE(Java Platform,Standard Edition)标准版

  JavaSE 可以开发和部署在桌面、服务器、嵌入式环境和实时环境中使用的 Java 应用程序。是EE，和ME的基础。一般就是指JDK。就是Java的基础语法（变量、方法、类之间的调用、关系，继承、接口、线程之类的），工具包（java.util.* ）,或者其他的一些封装
  
  链接：https://www.zhihu.com/question/31455874/answer/63915653
  
- Java EE (Java Platform，Enterprise Edition)企业版

  JavaEE，其实是一套规范，就是用java语言做企业开发（目前看来就是开发一些动态网站，或者对外提供调用服务的网站，或者其他没接触过的。。。）中的一整套规范，比如类怎么封装，网页的请求要用什么方法处理，语言编码一类的处理，拦截器啊什么的定义，请求返回得有什么信息。。。（具体看servlet的接口就知道了）
  比如：tomcat就是按照这套规范开发的容器软件，还有什么weblogic，JBoss、Resin等等
  
  正因为我们开发网站（使用JSP，Servelet。。或者封装了这些的框架：SSH。。。）可以放在tomcat，也可以放在JBoss。。。。，因为都是按照一个规范开发的东西，实际使用的还是JavaSE的那些东西，多出来的就是EE的一些规范类的封装代码。
  
- Java ME(Java Platform，Micro Edition)微型版

  JavaME 是微型版本，顾名思义，使用在手机啊，小设备啊上面的Java版本，特点就是小，相比JavaSE精简了很大一部分东西
  
### Java 重要特点

- Java 语言是面向对象的

	- 面向对象的理解？

- Java 语言是健壮的

	- Java 的强类型机制、异常处理、垃圾的自动收集等是 Java 程序健壮性的重要保证

- Java 语言是跨平台性的

	- 即: 一个编译好的.class 文件可以在多个系统下运行，这种特性称为跨平台，详见JVM

		- 
		- 
		- 

	- Java 核心机制-Java 虚拟机

	  1) JVM 是一个虚拟的计算机，具有指令集并使用不同的存储区域。负责执行指令，管理数据、内存、寄存器，包含在 
	  JDK 中. 
	  2) 对于不同的平台，有不同的虚拟机。 
	  3) Java 虚拟机机制屏蔽了底层运行平台的差别，实现了“一次编译，到处运行”
	  
	  
	  
- Java 语言是解释型的

	- 解释性语言：javascript,PHP, java 编译性语言: c / c++
	- 区别是：
解释性语言，编译后的代码，不能直接被机器执行,需要解释器来执行,

编译性语言, 编译后的代码, 可 以直接被机器执行, c /c++

### 什么是 JDK，JRE

- JDK 基本介绍

  1) JDK 的全称(Java Development Kit 
  Java 开发工具包) 
  JDK = JRE + java 的开发工具 [java, javac,javadoc,javap 等] 
  2) JDK 是提供给 Java 开发人员使用的，其中包含了 java 的开发工具，也包括了 JRE。所以安装了 JDK，就不用在单独 
  安装 JRE 了。
  
	- JDK=Java开发工具+JRE

- JRE 基本介绍

  1) JRE(Java Runtime Environment 
  Java 运行环境) 
  JRE = JVM + Java 的核心类库[类] 
  2) 包括 Java 虚拟机(JVM Java Virtual Machine)和 Java 程序所需的核心类库等，如果想要运行一个开发好的 Java 程序， 
  计算机中只需要安装 JRE 即可。
  
	- JRE=JVM+Java类库

- JDK、JRE 和 JVM 的包含关系

  1) JDK = JRE + 开发工具集（例如 Javac,java 编译工具等) 
  2) JRE = JVM + Java SE 标准类库（
  java 核心类库） 
  3) 如果只想运行开发好的 .class 文件 只需要 JRE
  
	- 

### JAVA执行流程

- 

### 注释

- 单行注释 //
- 多行注释 /* */
- 文档注释 /** */

### Windows常用的 dos 命令

- 查看当前目录是有什么内容 dir
- 切换到其他地址 cd
- 查看指定的目录下所有的子级目录 tree

	- tree /f
	- tree /d
	- tree -L n

- 清屏 cls
- 退出 DOS exit
- 其它

  md[创建目录]
  rd[删除目录]
  copy[拷贝文件]
  del[删除文件]
  echo[输入内容到文件]
  type[显示文本文件的内容]
  move[剪切、移动]
  
## 3、变量

### 数据类型

- 基本数据类型

	- 变量类型、字节数

		- 

- 引用类型

	- 类
	- 接口
	-  数组

### 基本数据类型转换

- 自动类型转换

	- Java程序进行赋值时，进度小的自动转换为精度大的数据类型
	- 精度大小排序

		- 

	- 自动类型转换注意和细节

		- 

- 强制类型转换

	- 自动类型转换的逆过程，将容量大的数据类型转换为容量小的数据类型。使用时要加上强制转换符 ( )，但可能造成 精度降低或溢出,格外要注意
	- 强制类型转换细节说明

		- 

### [JAVA API文档](https://www.matools.com/)

- jdk 长期支持版本

	- JDK8
	- JDK11
	- JDK17

### 基本数据类型和 String 类型的转换

- String 转化成 基本数据类型

	- 利用基本数据类型对应的包装类的parseXxx() 或 valueOf() 方法

- 基本 数据类型 转化成String 类型

	- 1) 利用基本数据类型对应包装类的toString 方法 转化成String实例
	- 2) 利用String.valueof() 转化成String实例
	- 3) + “” 注意： 字符串和任何数据使用 + 都是相连接，最终都会变成字符串

- 

## 4、运算符

### 运算符介绍

- 算术运算符

	- 

- 关系运算符(比较运算符)

	- 

- 逻辑运算符
- 赋值运算符

	- 基本赋值运算符 = int a = 10
	- 复合赋值运算符

		- += ，-= ，*= ， /= ，%=

- 三元运算符

	- 条件表达式 ? 表达式 1: 表达式 2;

- 运算符优先级

	- 

### 标识符的命名规则和规范

- 

### 关键字

- 
- 

### 保留字

- byValue、cast、future、 generic、 inner、 operator、 outer、 rest、 var 、 goto 、const

### 键盘输入语句

- Scanner

  1) 导入该类的所在包, java.util.* 
  2) 创建该类对象（声明变量） 
  3) 调用里面的功能
  
	- Scanner myScanner = new Scanner(System.in);
	- String name = myScanner.next();

### 进制

二进制：0,1 ，满 2 进 1.以 0b 或 0B 开头。 
十进制：0-9 ，满 10 进 1。 
八进制：0-7 ，满 8 进 1. 以数字 0 开头表示。 
十六进制：0-9 及 A(10)-F(15)，满 16 进 1. 以 0x 或 0X 开头表示。此处的 A-F 不区分大小写

- 进制的转换

### 位运算

- 按位取反~
按位与&
按位或|

	- A = 0011 1100
B = 0000 1101
-----------------
A&B = 0000 1100
A | B = 0011 1101
~A= 1100 0011

- 异或^

	- A = 0011 1100
B = 0000 1101
-----------------
A ^ B = 0011 0001

- 同或

	- 同或运算 = 异或运算  ^  1
A：1 0 1 0 1 1 0 0
B：0 0 0 0 1 1 1 1
异或：1 0 1 0 0 0 1 1 
1：1 1 1 1 1 1 1 1
同或：0 1 0 1 1 1 0 0

- 算术右移>> 
算术左移<< 
无符号右移>>> 

	- 左移的规则只记住一点：丢弃最高位，0补最低位
	- 右移的规则只记住一点：符号位不变，左边补上符号位
	- 无符号右移的规则只记住一点：忽略了符号位扩展，0补最高位
	- 

- A:00111100
B:00001101
- 原码、反码、补码

	- 

## 5、程序控制结构

### 顺序控制

- 

### 分支控制

- if-else

	- 1) 单分支 if 
2) 双分支 if-else
3) 多分支 if-else if -....-else

- 嵌套分支

	- 

- switch 分支结构

	- switch表达式后面的数据类型只能是byte,short，char，int四种整型类型，枚举类型和java.lang.String类型（从java 7才允许），不能是boolean，long，float，double类型

	  在网上看到好多文章，说switch还支持byte,short,char,int 的包装类，首先可以肯定说switch不支持这些包装类，但是如下的代码又是正确的：
	  public static void main(String[] args) {
	          switch (new Integer(45)) {
	          case 40:
	              System.out.println("40");
	              break;
	          case 45:
	              System.out.println("45");//将会打印这句
	              break;
	          default:
	              System.out.println("?");
	              break;
	          }
	      }
	  可以打印正确的结果，在挨着挨着试完Byte,Short,Character,Integer后发现都可以正确打印，于是便说switch也支持byte，short，char，int的包装类。这种说法不完全正确，之所以switch能够支持他们的包装类，是因为自动拆箱（从JDK1.5开始支持自动拆箱和自动装箱，自动拆箱就是自动将引用数据类型转化为基本数据类型，自动装箱就是自动将基本数据类型转化为引用数据类型）的原因；
	  使用jclasslib软件打开上面的.class文件，
	  
	  0 new #2 <java/lang/Integer>                             创建一个Integer类的对象
	  3 dup                                                    将对象的标识压入栈顶部
	  4 bipush 45                                              将整形45压入栈中
	  6 invokespecial #3 <java/lang/Integer.<init>>            调用Integer类型的构造方法
	  9 invokervirtual #4 <java/lang/Integer.intValue>         调用intValue()方法
	  12 lookupswitch 2
	          40:40(+28)
	          45:51(+39)
	          defalut:62(+50)
	  40 getstatic #5 <java/lang/System.out>                   获得标准输出流
	  43 ldc #6 <40>                                           从常量池中将40的索引压入栈中
	  45 invokevirtual #7 <java/io/PrintStream.println>        调用println()方法
	  48 goto 70 (+22)
	  51 gestatic #5 <java/lang/System.out>
	  54 ldc #8 <45>
	  56 invokevirtual #7 <java/io/PrintStream.println>
	  59 goto 70 (+11)
	  62 getstatic #5 <java/lang/System.out>
	  65 ldc #9<?>
	  67 invokevirtual #7 <java/io/PrintStream.println>
	  70 return
	  从上面的第5行我们可以看出编译器自动调用了intValue()方法，如果是使用Byte会自动调用byteValue()方法，如果是Short会自动调用shortValue()方法，如果是Integer会自动调用intValue()方法。switch 的查找原理是使用key-offset在目标表格中查找的，lookupswitch后面的数字和goto后面的数字都是有规律的。
	  
	  因此switch表达式后面的数据类型只支持byte,short,int整形类型、字符类型char、枚举类型和java.lang.String类型。
	  
	  
	- 
	- 
	- 

- switch 和 if 的比较

	- 1) 如果判断的具体数值不多，而且符合 byte、 short 、int、 char, enum[枚举], String 这 6 种类型。虽然两个语句都可 以使用，建议使用 swtich 语句。
2) 其他情况：对区间判断，对结果为 boolean 类型判断，使用 if，if 的使用范围更广

### 循环控制

- for 循环控制
- while 循环控制
- do..while 循环控制

	- 基本语法

	  循环变量初始化; 
	  do{ 
	  	循环体(语句); 
	  	循环变量迭代; 
	  }while(循环条件);
	  
	  0. do while 是关键字 
	  1. 也有循环四要素, 只是位置不一样 
	  2. 先执行，再判断，也就是说，一定会至少执行一次 
	  3. 最后 有一个 分号 ; 
	  4. while 和 do..while 区别
	  
- 多重循环控制

	- 

### 跳转控制语句-break

- break 语句用于终止某个语句块的执行，一般使用在 switch 或者循环[for , while , do-while]中
- 

### 跳转控制语句-continue

- continue 语句用于结束本次循环，继续执行下一次循环。
- continue 语句出现在多层嵌套的循环语句体中时，可以通过标签指明要跳过的是哪一层循环 , 这个和前面的标签的 使用的规则一样

### 跳转控制语句-return

- return 使用在方法，表示跳出所在的方法，如果 return 写在 main 方法，退出程序

### 导致方法结束方式

- return
- throw
- 区别

	- throw作用会一层一层往上抛出 最终抛向虚拟机
	- return的作用很简单，意思是方法直接返回了，该方法不在向下执行。但是调用该方法的方法继续执行
	- throw指抛出异常，并且该方法以及调用该方法的一切方法将不会向下执行

## 6、数组、排序和查找

### 数组介绍

- 数组可以存放多个同一类型的数据。数组也是一种数据类型，是引用类型。

### 数组的使用

- 初始化

	- 静态初始化

	  初始化时由程序员显式指定每个数组元素的初始值，由系统决定数组的长度
	  01、
	  int[] intArr;
	  intArr = new int[]{1,2,3,4,5,9};
	  02、
	  String[] strArr = {"张三","李四","王二麻"};
	  
	- 动态初始化

	  初始化时由程序员指定数组的长度，由系统初始化每个数组元素的默认值 arrayName = new type[length];
	  
	  int[] price = new int[4];
	  
	- 数组的默认初始化

	  数组是引用类型，它的元素相当于类的实例变量，因此数组一经分配空间，其中的每个元素也被按照实例变量同样的方式被隐式初始化（即使不给赋初值，也会被程序赋予默认值）
	  //默认初始化 
	  int[] iDefaultArr = new int[3]; //数组中的每个元素被赋予默认值0, 0, 0 
	  LOLHero[] defaultHeros = new LOLHero[3]; //数组中每个元素被赋予默认值null， null, null
	  
- 数组使用注意事项和细节

  注意：不要同时使用静态初始化和动态初始化，也就是说，不要在进行数组初始化时，既指定数组的长度，也为每个数组元素分配初始值。
  一旦数组完成初始化，数组在内存中所占的空间将被固定下来，所以数组的长度将不可改变
  
  1) 数组是多个相同类型数据的组合，实现对这些数据的统一管理 
  2) 数组中的元素可以是任何数据类型，包括基本类型和引用类型，但是不能混用。 
  3) 数组创建后，如果没有赋值，有默认值 
  int 0，short 0, byte 0, long 0, float 0.0,double 0.0，char \u0000，boolean false，String null 
  4) 使用数组的步骤 1. 声明数组并开辟空间 2 给数组各个元素赋值 3 使用数组 
  5) 数组的下标是从 0 开始的。 
  6) 数组下标必须在指定范围内使用，否则报：下标越界异常
  7) 数组属引用类型，数组型数据是对象(object)
  
- 数组赋值

	- 1) 基本数据类型赋值，这个值就是具体的数据，而且相互不影响。 int n1 = 2; int n2 = n1;
	- 2) 数组在默认情况下是引用传递，赋的值是地址
	- 

- 数组拷贝

	- 浅拷贝

	  浅拷贝：创建一个新对象，然后将当前对象的非静态字段复制到该新对象，如果字段是值类型的，那么对该字段执行复制；如果该字段是引用类型的话，则复制引用但不复制引用的对象。因此，原始对象及其副本引用同一个对象。
	  
		- 

	- 深拷贝

	  深拷贝：创建一个新对象，然后将当前对象的非静态字段复制到该新对象，无论该字段是值类型的还是引用类型，都复制独立的一份。当你修改其中一个对象的任何内容时，都不会影响另一个对象的内容
	  
		- 

	- JAVA深拷贝和浅拷贝的实现

		- 浅拷贝

			- 1.通过构造方法实现浅拷贝

			  package copy;
			  
			  /**
			   * @author zhouxuan
			   * @since 2019/5/22
			   */
			  public class ShallowCopy {
			  
			      public static void main(String[] agrs){
			          Stock stock = new Stock(100);
			          Car p1 = new Car("Audi",stock);
			          Car p2 = new Car(p1);
			          System.out.println("修改前:");
			          System.out.println("p1:" + p1.toString());
			          System.out.println("p2:" + p2.toString());
			          //修改基本数据类型数据
			          p1.setBrand("Porches");
			          //修改引用类型数据
			          stock.setStock(999);
			          System.out.println("修改后:");
			          System.out.println("p1:" + p1.toString());
			          System.out.println("p2:" + p2.toString());
			      }
			  
			  }
			  
			  class Car {
			      private String brand;
			      private Stock stock;
			  
			      public Car(String brand, Stock stock) {
			          this.brand = brand;
			          this.stock = stock;
			      }
			      public Car(Car car){
			          this.brand = car.brand;
			          this.stock = car.stock;
			      }
			  
			      public String getBrand() {
			          return brand;
			      }
			  
			      public void setBrand(String brand) {
			          this.brand = brand;
			      }
			  
			      public Stock getStock() {
			          return stock;
			      }
			  
			      public void setStock(Stock stock) {
			          this.stock = stock;
			      }
			  
			      @Override
			      public String toString() {
			          return "brand='" + brand + '\'' +
			                  ", stock=" + stock;
			      }
			  }
			  
			  class Stock{
			      private int stock;
			  
			      public Stock(int stock) {
			          this.stock = stock;
			      }
			  
			      public int getStock() {
			          return stock;
			      }
			  
			      public void setStock(int stock) {
			          this.stock = stock;
			      }
			  
			      @Override
			      public String toString() {
			          return ""+this.getStock();
			      }
			  }
			  
			  
			- 2.通过重写clone()接口实现浅拷贝

			  所有类的都有一个Obeject根类,Obeject中提供了clone()方法:
			  protected native Object clone() throws CloneNotSupportedException;
			  但我们不能直接调用clone()方法，需要实现Cloneable接口，否则会抛出CloneNotSupportedException异常。我们可以在类中重写clone()方法，实现浅拷贝
			  
			  原文链接：https://blog.csdn.net/zhouxuanwushini/article/details/90446668
			  
			  
			  public class ShallowCopyClone {
			      public static void main(String[] agrs) {
			          Price price = new Price(100);
			          Computer p1 = new Computer(price, 999);
			          Computer p2 = (Computer) p1.copy();
			          System.out.println("修改前");
			          System.out.println(p1.toString());
			          System.out.println(p2.toString());
			          p1.setStock(20);
			          price.setPrice(123);
			          System.out.println("修改后");
			          System.out.println(p1.toString());
			          System.out.println(p2.toString());
			      }
			  }
			  
			  class Computer implements Cloneable{
			      private Price price;
			      private int stock;
			  
			      public Computer(Price price, int stock) {
			          this.price = price;
			          this.stock = stock;
			      }
			  
			      public Computer(Computer computer) {
			          this.price = computer.price;
			          this.stock = computer.stock;
			      }
			  
			      public Price getPrice() {
			          return price;
			      }
			  
			      public void setPrice(Price price) {
			          this.price = price;
			      }
			  
			      public int getStock() {
			          return stock;
			      }
			  
			      public void setStock(int stock) {
			          this.stock = stock;
			      }
			  
			      @Override
			      public String toString() {
			          return "price=" + price.getPrice() +
			                  ", stock='" + stock ;
			      }
			  
			      public Object copy() {
			          Object obj = null;
			          try {
			              obj = super.clone();
			          } catch (CloneNotSupportedException e) {
			              e.printStackTrace();
			          }
			          return obj;
			      }
			  }
			  
			  class Price{
			      private int price;
			  
			      public Price(int price) {
			          this.price = price;
			      }
			  
			      public int getPrice() {
			          return price;
			      }
			  
			      public void setPrice(int price) {
			          this.price = price;
			      }
			  
			  
			  
		- 深拷贝

			- 1.通过序列化和反序列化实现深拷贝

			  需要拷贝的类实现Serializable接口，否则会抛出NotSerializableException异常。
			  
			  public class DeepCopy {
			      public static void main(String[] args) throws IOException, ClassNotFoundException {
			  
			          Category category = new Category(1);
			          Watch p1 = new Watch("high", category);
			  
			          ByteArrayOutputStream bos = new ByteArrayOutputStream();
			          ObjectOutputStream oos = new ObjectOutputStream(bos);
			          //将p1序列化
			          oos.writeObject(p1);
			          oos.flush();
			          //反序列化
			          ObjectInputStream ois = new ObjectInputStream(new ByteArrayInputStream(bos.toByteArray()));
			          Watch p2 = (Watch) ois.readObject();
			          System.out.println("修改前:");
			          System.out.println(p1.toString());
			          System.out.println(p2.toString());
			          System.out.println("修改后:");
			          p1.setLevel("low");
			          category.setCategory(2);
			          System.out.println(p1.toString());
			          System.out.println(p2.toString());
			      }
			  }
			  
			  class Watch implements Serializable{
			      private String level;
			      private Category category;
			  
			      public Watch(Watch watch) {
			          this.level = watch.level;
			          this.category = watch.category;
			      }
			  
			      public Watch(String level, Category category) {
			          this.level = level;
			          this.category = category;
			      }
			  
			      public String getLevel() {
			          return level;
			      }
			  
			      public void setLevel(String level) {
			          this.level = level;
			      }
			  
			      public Category getCategory() {
			          return category;
			      }
			  
			      public void setCategory(Category category) {
			          this.category = category;
			      }
			  
			      @Override
			      public String toString() {
			          return "Watch{" +
			                  "level='" + level + '\'' +
			                  ", category=" + category +
			                  '}';
			      }
			  }
			  
			  class Category implements Serializable{
			      private int category;
			  
			      public Category(int category) {
			          this.category = category;
			      }
			  
			      public int getCategory() {
			          return category;
			      }
			  
			      public void setCategory(int category) {
			          this.category = category;
			      }
			  
			      @Override
			      public String toString() {
			          return "Category{" +
			                  "category=" + category +
			                  '}';
			      }
			  }
			  
			  
### 排序

- 内部排序

  指将需要处理的所有数据都加载到内部存储器中进行排序。包括(交换式排序法、选择式排序法和插入式排序法)
  
- 外部排序

  数据量过大，无法全部加载到内存中，需要借助外部存储进行排序。包括(合并排序法和直接合并排序法)
  
### 多维数组-二维数组

- 内存结构

	- 

- 动态初始化

	- 语法: 类型[][] 数组名=new 类型[大小][大小]
比如: int a[][]=new int[2][3]
	- 动态初始化-列数不确定
比如：int[][] arr = new int[3][]

- 静态初始化

	- 数组名[][] = {{值 1,值 2..},{值 1,值 2..},{值 1,值 2..}}
比如: int[][] arr = {{1,1,1}, {8,8,9}, {100}};

- 二维数组使用细节和注意事项

  1) 一维数组的声明方式有: 
  int[] x 或者 int x[] 
  2) 二维数组的声明方式有: 
  int[][] y 或者 int[] y[] 或者 int y[][]
  3) 二维数组实际上是由多个一维数组组成的，它的各个一维数组的长度可以相同，也可以不相同。比如： map[][] 是 
  一个二维数组 
  int map [][] = {{1,2},{3,4,5}} 
  由 map[0] 是一个含有两个元素的一维数组 ，map[1] 是一个含有三个元素的一维数组构成，我们也称为列数不等 
  的二维数组
  
## 7、面向对象编程（基础部分）

### 类与对象

- 1) 类是抽象的，概念的，代表一类事物,比如人类,猫类.., 即它是数据类型. 
2) 对象是具体的，实际的，代表一个具体事物, 即 是实例. 
3) 类是对象的模板，对象是类的一个个体，对应一个实例
- 对象在内存中存在形式

	- 

- 属性如果不赋值，有默认值，规则和数组一致。具体说: int 0，short 0, byte 0, long 0, float 0.0,double 0.0，char \u0000， boolean false，String null
- 类和对象的内存分配机制

	- Java 内存的结构分析

		- 1) 栈： 一般存放基本数据类型(局部变量) 2) 堆： 存放对象(Cat cat , 数组等) 3) 方法区：常量池(常量，比如字符串)， 类加载信息 4) 示意图 [Cat (name, age, price)]

	- Java 创建对象的流程简单分析

		- 1) 先加载 Person 类信息(属性和方法信息, 只会加载一次) 
2) 在堆中分配空间, 进行默认初始化(看规则)
3) 把地址赋给 p , p 就指向对象
4) 进行指定初始化， 比如 p.name =”jack” p.age = 10

	- 

		- 

- 成员方法

	- 方法的调用机制原理

		- 

	- 成员方法的好处

		- 1) 提高代码的复用性 
2) 可以将实现的细节封装起来，然后供其他用户来调用即可

	- 访问修饰符

		- : public, protected, 默认, private

	- 成员方法传参机制

		- 基本数据类型的传参机制

			- 

		- 引用数据类型的传参机制

			- 
			- 
			- 在看一个案例，下面的方法会对原来的对象有影响吗？ p=null 和 p = new Person(); 对应示意图

			- 
			- 

	- 方法递归调用

		- 
		- 
		- 递归重要规则

			- 

	- 方法重载

		- java 中允许同一个类中，多个同名方法的存在，但要求 形参列表不一致：参数个数、参数类型，以及传入的顺序

	- 可变参数

		- 可以通过可变参数实现将同一个类中多个同名同功能但参数个数不同的方法，封装成一个方法
		- 注意事项和使用细节

	- 作用域

		- 
		- 注意事项和细节使用

			- 
			- 

	- 对象创建的流程分析

		- 
		- 

	- this 关键字

		- 
		- 
		- 深入理解 this

			- 

		- this 的注意事项和使用细节

			- 1) this 关键字可以用来访问本类的属性、方法、构造器 
2) this 用于区分当前类的属性和局部变量 
3) 访问成员方法的语法：this.方法名(参数列表);
4) 访问构造器语法：this(参数列表); 注意只能在构造器中使用(即只能在构造器中访问另外一个构造器, 必须放在第一 条语句) 
5) this 不能在类定义的外部使用，只能在类定义的方法中使用。

	- 构造方法/构造器

	  1) 构造器的修饰符可以默认， 也可以是 public protected private 
	  2) 构造器没有返回值 
	  3) 方法名 和类名字必须一样 
	  4) 参数列表 和 成员方法一样的规则 
	  5) 构造器的调用, 由系统完成
	  
		- 注意事项和使用细节

			- 

	- 方法重写

		- 执行顺序

			- 当一个子类继承父类并调用了子类的某个方法时代码块的执行顺序为：
1)父类静态代码块
2)子类静态代码块
3)父类普通代码块
4)父类构造器方法
5)子类普通代码块
6)子类构造器方法
7)子类A方法

		- 绑定

		  1、当子类和父类存在同一个方法，子类重写了父类的方法，程序在运行时调用方法是调用父类的方法还是子类的重写方法呢？
		   2、当一个类中存在方法名相同但参数不同(重载)的方法，程序在执行的时候该如何辨别区分使用哪个方法呢？
		   在Java中我们使用静态绑定（static binding）和动态绑定（Dynamic binding）来解决
		  
		  绑定指的是一个方法的调用与方法所在的类(方法主体)关联起来
		  
		  对java来说，绑定分为静态绑定和动态绑定；或者叫做前期绑定和后期绑定
		  
			- 动态绑定

			  在运行时根据具体对象的类型进行绑定。提供了一些机制，可在运行期间判断对象的类型，并分别调用适当的方法。也就是说，编译器此时依然不知道对象的类型，但方法调用机制能自己去调查，找到正确的方法主体。
			  
				- 类的字段/属性不会自动绑定

					- 1、子类的对象(由父类的引用handle)调用到的是父类的成员变量，运行时（动态）绑定针对的范畴只是对象的方法，而属性要采取静态绑定方法。
2、执行p.method()时会先去调用子类的method方法执行，若子类没有则向上转型去父类中寻找。
所以在向上转型的情况下，对象的方法可以找到子类，而对象的属性还是父类的属性。

				- 类的方法会自动绑定

					- 虚拟机提取对象的实际类型的方法表；
虚拟机搜索方法签名；
调用方法。

				- java当中的向上转型或者说多态是借助于动态绑定实现的，所以理解了动态绑定，也就搞定了向上转型和多态

					- 动态绑定的典型发生在父类和子类的转换声明之下：
比如：Parent p = new Child();
其具体过程细节如下：
1：编译器检查对象的声明类型和方法名。假设我们调用p.method()方法，并且p已经被声明为Child类的对象，那么编译器会列举出Child类中所有的名称为method的方法和从Child类的父类继承过来的method方法
2：接下来编译器检查方法调用中提供的参数类型。如果在所有名称为method 的方法中有一个参数类型和调用提供的参数类型最为匹配，那么就调用这个方法，这个过程叫做“重载解析” 
3：当程序运行并且使用动态绑定调用方法时，虚拟机必须调用同p所指向的对象的实际类型相匹配的方法版本。假设child类定义了mehod()那么该方法被调用，否则就在child的父类（Parent类）中搜寻方法method()

			- 静态绑定

			  在程序执行前方法已经被绑定，针对java简单的可以理解为程序编译期的绑定；
			  java当中的方法只有final，static，private和构造方法是前期绑定
			  
			- 区别

				- 1、静态绑定是发生在编译阶段；而动态绑定是在运行阶段；
				- 2、private, final and static方法和变量使用静态绑定，而虚函数(virtual methods)则会根据运行时的具体对象进行绑定（注：在Java语言中, 所有的方法默认都是”虚函数”。只有以关键字 final 标记的方法才是非虚函数。）
				- 3、静态绑定使用的是类信息，而动态绑定使用的是对象信息
				- 4、重载方法(overloaded methods)使用的是静态绑定，而重写方法(overridden methods)使用的是动态绑定

## 8、面向对象编程（中级部分）

### 包

- 应用场景1

	- 

- 包的三大作用

	- 

- 包的本质分析

	- 

- 包的命名

	- 

- 常用的包

	- 1) java.lang.* //lang 包是基本包，默认引入，不需要再引入. 
2) java.util.* //util 包，系统提供的工具包, 工具类，使用 Scanner 
3) java.net.* //网络包，网络开发 
4) java.awt.* //是做 java 的界面开发，GUI

- 引入包

	- 

- 注意事项和使用细节

	- 

### 访问修饰符

- 基本介绍

	- 1) 公开级别:用 public 修饰,对外公开
2) 受保护级别:用 protected 修饰,对子类和同一个包中的类公开
3) 默认级别:没有修饰符号,向同一个包的类公开
4) 私有级别:用 private 修饰,只有类本身可以访问,不对外公开

- 4种访问修饰符的访问范围

	- 

### 面向对象编程三大特征

- 封装

	- 封装介绍

		- 

	- 封装的理解和好处

		- 

	- 封装的实现步骤 (三步)

		- 

- 继承

	- 场景

		- 

	- 继承基本介绍和示意图

		- 继承可以解决代码复用,让我们的编程更加靠近人类思维.当多个类存在相同的属性(变量)和方法时,可以从这些类中 抽象出父类,在父类中定义这些相同的属性和方法，所有的子类不需要重新定义这些属性和方法，只需要通过 extends 来 声明继承父类即可

1) 代码的复用性提高了
2) 代码的扩展性和维护性提高了
		- 

	- 继承的基本语法

		- 

	- 继承的深入讨论/细节问题

		- 1) 子类继承了所有的属性和方法，非私有的属性和方法可以在子类直接访问, 但是私有属性和方法不能在子类直接访 问，要通过父类提供公共的方法去访问 
2) 子类必须调用父类的构造器， 完成父类的初始化 
3) 当创建子类对象时，不管使用子类的哪个构造器，默认情况下总会去调用父类的无参构造器，如果父类没有提供无参构造器，则必须在子类的构造器中用 super 去指定使用父类的哪个构造器完成对父类的初始化工作，否则，编译不会通过(怎么理解。) 
4) 如果希望指定去调用父类的某个构造器，则显式的调用一下 : super(参数列表) 
5) super 在使用时，必须放在构造器第一行(super 只能在构造器中使用) 
6) super() 和 this() 都只能放在构造器第一行，因此这两个方法不能共存在一个构造器 
7) java 所有类都是 Object 类的子类, Object 是所有类的基类. 
8) 父类构造器的调用不限于直接父类！将一直往上追溯直到 Object 类(顶级父类) 
9) 子类最多只能继承一个父类(指直接继承)，即 java 中是单继承机制。 思考：如何让 A 类继承 B 类和 C 类？ 【A 继承 B， B 继承 C】 
10) 不能滥用继承，子类和父类之间必须满足 is-a 的逻辑关系

	- 继承的本质分析

		- 

- 多态

	- Java中不要在父类的构造方法中调用会被子类重写的方法

	  import java.util.*;
	   
	  class Animal
	  {
	     public Animal()
	     {
	       this.eat();
	     }
	     
	     protected void eat()
	     {
	       System.out.println("Eat something");
	     }
	  }
	   
	  public class Bird extends Animal
	  {
	    public Bird()
	    {
	      
	    }
	    @Override
	    protected void eat()
	    {
	      System.out.println("Just eat worm");
	    }
	    
	    public static void main(String[]args)
	    {
	      new Bird();
	    }
	  } 
	  
	  输出结果是：
	  Just eat worm
	  
	  这其实涉及到编译时类型和运行时类型的问题，在上面的例子中，虽然使用了this，即在调用父类的构造方法中，其编译时类型确实是Animal，但是运行时类型却是Bird，因而调用的是子类中重写的eat()方法。另外，动态绑定不涉及属性，只涉及方法。
	  
	- 多[多种]态[状态]基本介绍

		- 方法或对象具有多种形态

	- 多态的具体体现

		- 方法的多态

			- 重写和重载就体现多态

		- 对象的多态

			- 
			- 

	- 多态注意事项和细节讨论
	- 多态的前提是：两个对象(类)存在继承关系
	- 多态的向上转型

		- 

	- 多态向下转型

		- 
		- 只有父类对象本身就是用子类new出来的时候, 才可以在将来被强制转换为子类对象
F f = new S();
S s2 = (S)f
		- 属性没有重写之说！属性的值看编译类型

	- instanceOf 比较操作符，用于判断对象的运行类型是否为 XX 类型或 XX 类型的子类型
	- 
	- java 的动态绑定机制

		- 

	- 多态的应用

		- 多态数组

			- 数组的定义类型为父类类型，里面保存的实际元素类型为子类类型

		- 多态参数

### Object 类详解

- equals 方法

	- ==和 equals 的对比

		- 
		- 
		- 

	- 如何重写 equals 方法

- hashCode 方法

	- 
	- 1) 提高具有哈希结构的容器的效率！ 
2) 两个引用，如果指向的是同一个对象，则哈希值肯定是一样的！ 
3) 两个引用，如果指向的是不同对象，则哈希值是不一样的 
4) 哈希值主要根据地址号来的！， 不能完全将哈希值等价于地址

- toString 方法

	- 基本介绍

		- 默认返回：全类名+@+哈希值的十六进制
		- 子类往往重写 toString 方法，用于返回对象的属性信息

	- 重写 toString 方法，打印对象或拼接对象时，都会自动调用该对象的 toString 形式
	- 当直接输出一个对象时，toString 方法会被默认的调用, 比如 System.out.println(monster)； 就会默认调用 monster.toString()

- finalize 方法

	- 1) 当对象被回收时，系统自动调用该对象的 finalize 方法。子类可以重写该方法，做一些释放资源的操作【演示】 
2) 什么时候被回收：当某个对象没有任何引用时，则 jvm 就认为这个对象是一个垃圾对象，就会使用垃圾回收机制来 销毁该对象，在销毁该对象前，会先调用 finalize 方法。 
3) 垃圾回收机制的调用，是由系统来决定(即有自己的 GC 算法), 也可以通过 System.gc() 主动触发垃圾回收机制

### super 关键字

- super 代表父类的引用，用于访问父类的属性、方法、构造器
- 
- super 给编程带来的便利/细节

	- 

- super 和 this 的比较

	- 

### 方法重写/覆盖

- 
- 方法重写也叫方法覆盖，需要满足下面的条件

	- 

- 对方法的重写和重载做一个比较

	- 

## 9、面向对象编程（高级部分）

### 类变量

- 什么是类变量

	- 

- 内存布局

	- 
	- 

- 类变量使用注意事项和细节

	- 
	- 

### 类方法

- 
- 类方法使用注意事项和细节

	- 
	- 

### 深入理解 main 方法

- 
- 1) 在 main()方法中，我们可以直接调用 main 方法所在类的静态方法或静态属性。
2) 但是，不能直接访问该类中的非静态成员，必须创建该类的一个实例对象后，才能通过这个对象去访问类中的非静 态成员

### 代码块

- 基本介绍

	- 

- 基本语法
- 代码块的好处

	- 
	- 代码块调用的顺序优先于构造器

- 代码块使用注意事项和细节

	- 
	- 
	- 
	- 

### 单例设计模式

- 什么是设计模式

	- 

- 什么是单例模式

	- 

- 单例模式应用实例

	- 

		- 饿汉式

			- 一开始就创建

		- 懒汉式

			- 使用到的时候才创建

		- 饿汉式 VS 懒汉式

			- 

### final 关键字

- 基本介绍

	- 

- final 使用注意事项和细节

	- 
	- 
	- 

### 抽象类

- 抽象类的介绍

	- 
	- 
	- 

- 抽象类使用的注意事项和细节

	- 
	- 
	- 

- 抽象类最佳实践-模板设计模式

	- 基本介绍

		- 

	- 模板设计模式能解决的问题

		- 

	- 实例

		- 
		- 非抽象方法调用抽象方法
子类实现抽象方法
调用非抽象方法即可

### 接口

- 基本介绍

	- 

- 应用场景

	- 
	- 
	- 

- 注意事项和细节

	- 
	- 

### 实现接口 vs 继承类

- 当子类继承了父类，就自动的拥有父类的功能
如果子类需要扩展功能，可以通过实现接口的方式扩展.
可以理解 实现接口 是 对 java 单继承机制的一种补充
- 
- 接口的多态特性

	- 

### 内部类

- 如果定义类在局部位置(方法中/代码块) 
(1) 局部内部类 (2) 匿名内部类
定义在成员位置 (1) 成员内部类 (2) 静态内部类
- 基本介绍

	- 

- 基本语法

	- 

- 内部类的分类

	- 
	- 局部内部类的使用

		- 

	- 匿名内部类的使用

		- 
		- 

	- 成员内部类的使用

		- 
		- 
		- 

	- 静态内部类的使用

		- 

## 10、枚举和注解

### 枚举的2种实现方式

- 1) 自定义类实现枚举

	- 
	- 
	- 自定义类实现枚举-小结

		- 1) 构造器私有化
		- 2) 本类内部创建一组对象[四个 春夏秋冬]
		- 3) 对外暴露对象（通过为对象添加 public final static 修饰符）
		- 4) 可以提供 get 方法，但是不要提供 set

- 2) 使用 enum 关键字实现枚举

  //如果使用了 enum 来实现枚举类 
  //1. 使用关键字 enum 替代 class 
  //2. public static final Season SPRING = new Season("春天", "温暖") 直接使用 
  // 
  SPRING("春天", "温暖") 解读 常量名(实参列表) 
  //3. 如果有多个常量(对象)， 使用 ,号间隔即可 
  //4. 如果使用 enum 来实现枚举，要求将定义常量对象，写在前面 
  //5. 如果我们使用的是无参构造器，创建常量对象，则可以省略 () 
  SPRING("春天", "温暖"), WINTER("冬天", "寒冷"), AUTUMN("秋天", "凉爽"), 
  SUMMER("夏天", "炎热")/*, What()*/; 
  private String name; 
  private String desc;//描述 
  private Season2() {//无参构造器 
  }
  private Season2(String name, String desc) { 
  this.name = name; 
  this.desc = desc; 
  }
  }
  
	- enum 关键字实现枚举注意事项

		- 1) 当我们使用 enum关键字开发一个枚举类时，默认会继承 Enum 类, 而且是一个final 类[如何证明],使用 javap 工具来演示
2) 传统的 public static final Season2 SPRING = new Season2("春天", "温暖"); 简化成 SPRING("春天", "温暖")， 这里必须知道，它调用的是哪个构造器. 
3) 如果使用无参构造器 创建 枚举对象，则实参列表和小括号都可以省略
4) 当有多个枚举对象时，使用,间隔，最后有一个分号结尾
5) 枚举对象必须放在枚举类的行首

			- 
			- 

### enum常用方法说明

- 说明：使用关键字 enum 时，会隐式继承 Enum 类, 这样我们就可以使用 Enum 类相关的方法，定义：
public abstract class Enum<E extends Enum<E>> implements Comparable<E>, Serializable { }
- 
- enum 常用方法

	- 1) toString:Enum 类已经重写过了，返回的是当前对象 名,子类可以重写该方法，用于返回对象的属性信息 
2) name：返回当前对象名（常量名），子类中不能重写 
3) ordinal：返回当前对象的位置号，默认从 0 开始 
4) values：返回当前枚举类中所有的常量 
5) valueOf：将字符串转换成枚举对象，要求字符串必须 为已有的常量名，否则报异常！
6) compareTo：比较两个枚举常量，比较的就是编号！

### enum 实现接口

- 1) 使用 enum 关键字后，就不能再继承其它类了，因为 enum 会隐式继承 Enum，而 Java 是单继承机制。 
2) 枚举类和普通类一样，可以实现接口，如下形式：
enum 类名 implements 接口 1，接口 2{}

### 注解

- 注解的理解

	- 1) 注解(Annotation)也被称为元数据(Metadata)，用于修饰解释 包、类、方法、属性、构造器、局部变量等数据信息。 
2) 和注释一样，注解不影响程序逻辑，但注解可以被编译或运行，相当于嵌入在代码中的补充信息。 
3) 在 JavaSE 中，注解的使用目的比较简单，例如标记过时的功能，忽略警告等。在 JavaEE 中注解占据了更重要的角 色，例如用来配置应用程序的任何切面，代替 java EE 旧版中所遗留的繁冗代码和 XML 配置等。

- 基本的 Annotation 介绍

	- 使用 Annotation 时要在其前面增加 @ 符号, 并把该 Annotation 当成一个修饰符使用。用于修饰它支持的程序元 素
	- 三个基本的 Annotation

		- 1) @Override: 限定某个方法，是重写父类方法, 该注解只能用于方法 
2) @Deprecated: 用于表示某个程序元素(类, 方法等)已过时 
3) @SuppressWarnings: 抑制编译器警告

			- 如果你写了@Override 注解，编译器就会去检查该方法是否真的重写了父类的方法
			- 
			- @Deprecated: 用于表示某个程序元素(类, 方法等)已过时
			- 
			- @SuppressWarnings: 抑制编译器警告
			- 

		- 

- JDK的元Annotation(元注解)

	- 元注解的基本介绍

		- JDK 的元 Annotation 用于修饰其他 Annotation

	- 元注解的种类

		- 1) Retention //指定注解的作用范围，三种 SOURCE,CLASS,RUNTIME 
2) Target // 指定注解可以在哪些地方使用 
3) Documented //指定该注解是否会在 javadoc 体现 
4) Inherited //子类会继承父类注解

			- @Retention 注解

				- 只能用于修饰一个 Annotation 定义, 用于指定该 Annotation 可以保留多长时间, @Rentention 包含一个 RetentionPolicy 类型的成员变量, 使用 @Rentention 时必须为该 value 成员变量指定值
				- @Retention 的三种值

					- 1) RetentionPolicy.SOURCE: 编译器使用后，直接丢弃这种策略的注释 
2) RetentionPolicy.CLASS: 编译器将把注解记录在 class 文件中. 当运行 Java 程序时, JVM 不会保留注解。 这是默认值
3) RetentionPolicy.RUNTIME:编译器将把注解记录在 class 文件中. 当运行 Java 程序时, JVM 会保留注解. 程序可以 通过反射获取该注解
					- 

			- @Target

				- 
				- 

			- @Documented

				- 
				- 

			- @Inherited 注解

				- 

## 11、异常-exception

### 异常介绍

- 

### 异常体系

- 
- 异常体系图的小结

	- 

- 运行时异常

	- 1) NullPointerException 空指针异常 
2) ArithmeticException 数学运算异常 
3) ArrayIndexOutOfBoundsException 数组下标越界异常 
4) ClassCastException 类型转换异常 
5) NumberFormatException 数字格式不正确异常

		- 当应用程序试图在需要对象的地方使用 null 时，抛出该异常NullPointerException

当出现异常的运算条件时，抛出ArithmeticException

用非法索引访问数组时抛出的异常ArrayIndexOutOfBoundsException

当试图将对象强制转换为不是实例的子类时，抛出ClassCastException

当应用程序试图将字符串转换成一种数值类型，但该字符串不能转换为适当格式时，抛出NumberFormatException

- 编译异常

	- 1) SQLException
2) IOException
3) FileNotFoundException
4) ClassNotFoundException
5) EOFException
6) IllegalArgumentException

### 异常处理

- 异常处理的方式

	- 

- 异常机制示意图

	- 
	- 

- try-catch 方式处理异常-注意事项

	- 
	- 
	- 

- try-catch-finally 执行顺序小结

	- 

- throws 异常处理

	- 基本介绍

		- 

	- 注意事项和使用细节

		- 

### 自定义异常

- 基本概念

	- 

- 自定义异常的步骤

	- 

### throw 和 throws 的区别

- 一览表

	- 

### UML中的N种关系

在UML类图中，常见的有以下几种关系: 泛化（Generalization）, 实现（Realization），关联（Association)，聚合（Aggregation），组合(Composition)，依赖(Dependency)


各种关系的强弱顺序：泛化 = 实现 > 组合 > 聚合 > 关联 > 依赖
https://zhuanlan.zhihu.com/p/93289356

- 泛化

  【泛化关系】：是一种继承关系，表示一般与特殊的关系，它指定了子类如何特化父类的所有特征和行为。例如：老虎是动物的一种，即有老虎的特性也有动物的共性。
  【箭头指向】：带三角箭头的实线，箭头指向父类
  
	- 

- 实现

  
  【实现关系】：在这里插入图片描述是一种类与接口的关系，表示类是接口所有特征和行为的实现.
  【箭头指向】：带三角箭头的虚线，箭头指向接口
  
	- 

- 组合

  
  【组合关系】：是整体与部分的关系，但部分不能离开整体而单独存在。如公司和部门是整体和部分的关系，没有公司就不存在部门。
  组合关系是关联关系的一种，是比聚合关系还要强的关系，它要求普通的聚合关系中代表整体的对象负责代表部分的对象的生命周期。
  【代码体现】：成员变量
  【箭头及指向】：带实心菱形的实线，菱形指向整体
  
  
	- 

- 聚合

  【聚合关系】：是整体与部分的关系，且部分可以离开整体而单独存在。如车和轮胎是整体和部分的关系，轮胎离开车仍然可以存在。
  聚合关系是关联关系的一种，是强的关联关系；关联和聚合在语法上无法区分，必须考察具体的逻辑关系。
  【代码体现】：成员变量
  【箭头及指向】：带空心菱形的实心线，菱形指向整体
  
	- 

- 关联

  
  【关联关系】：是一种拥有的关系，它使一个类知道另一个类的属性和方法；如：老师与学生，丈夫与妻子关联可以是双向的，也可以是单向的。双向的关联可以有两个箭头或者没有箭头，单向的关联有一个箭头。
  【代码体现】：成员变量
  【箭头及指向】：带普通箭头的实心线，指向被拥有者
  
	- 

- 依赖

  
  【依赖关系】：是一种使用的关系，即一个类的实现需要另一个类的协助，所以要尽量不使用双向的互相依赖.
  【代码表现】：局部变量、方法的参数或者对静态方法的调用
  【箭头及指向】：带箭头的虚线，指向被使用者
  
	- 

- 各种类图关系

	- 

## 12、常用类

### 包装类

- 包装类的分类

	- 针对八种基本数据类型相应的引用类型—包装类

		- 
		- 
		- 
		- 

- 包装类和基本数据的转换

	- 
	- 包装类型和 String 类型的相互转换（Integer为例，其他类似）

		- 包装类->String

			- 方式 1

				- String str1 = i + "";

			- 方式 2

				- String str2 = i.toString();

			- 方式 3

				- String str3 = String.valueOf(i);

		- String -> 包装类

			- Integer i2 = Integer.parseInt(str4);
			- Integer i3 = new Integer(str4);

	- Integer 类和 Character 类的常用方法

		- Integer.MIN_VALUE //最大值
Integer.MAX_VALUE //最小值
Character.isDigit('a') //是否数字
Character.isLetter('a') //是否字母
Character.isUpperCase('a') //是否大写
Character.isLowerCase('a') //是否小写
Character.isWhitespace('a') //是否空格
Character.toUpperCase('a') //转大写
Character.toLowerCase('A') //转小写

### 实现Serializable

- 串行化(序列化)

	- 序列化是什么/干什么的？

	  Java序列化和Java串行化都是一样的，都对应英文中的Serializable。可能是翻译的时候不统一，我一开始的时候以为是两个不同的概念
	  
	  简单说就是为了保存内存中的各种对象的状态，并且可以把保存的对象状态再读出来。虽然你可以用你自己的各种方法来保存Object States,但是java给你提供了一种应该更好的保存对象状态的机制，那就是序列化。
	  
	  一个对象随着创建而存在，随着程序结束而结束。那如果我要保存一个对象的状态呢？Java序列化能够将对象的状态写入byte流存储起来，也从其他地方将byte流读取出来，重新构造一个新的对象。这种机制允许你将对象通过网络进行传播，并且可以随时把对象持久化到数据库、文件系统中。简而言之，序列化就是将一个对象的状态保存起来，而反序列化就是将已经保存的流对象恢复成原来的对象。
	  
	- 如何实现序列化

	  要实现串行化的类必须先实现Serializable接口。
	  其实一个类要实现串行化，不但这个类要实现Serializable接口外，这个类里面的成员属性也要实现Serializable接口才能把这个类的成员写进文件里。
	  
	  之后可以利用ObjectInputStream的readOjbect()方法和OjbectOutputStream的writeObject()方法进行对象的读和写，即反序列化和序列化。
	  
		- 示例

		  a)Java对象
		  在java中要想使一个java对象可以实现序列化与反序列化,必须让该类实现java.io.Serializable接口
		  java.io.Serializable接口定义如下:
		  publicinterfaceSerializable {
		  
		  }
		  
		  b)序列化主要依赖java.io.ObjectOutputStream类,该类对java.io.FileOutputStream进一步做了封装,这里主要使用ObjectOutputStream类的writeObject()方法实现序列化功能
		  /**
		  
		  *将对象序列化到磁盘文件中
		  
		  *@paramo
		  
		  *@throwsException
		  
		  */
		  public static void writeObject(Object o)throwsException{
		  
		  File f=new File("d:""user.tmp");
		  
		  if(f.exists()){
		  
		  f.delete();
		  
		  }
		  
		  FileOutputStream os=new FileOutputStream(f);
		  
		  //ObjectOutputStream核心类
		  
		  ObjectOutputStream oos=newObjectOutputStream(os);
		  
		  oos.writeObject(o);
		  
		  oos.close();
		  
		  os.close();
		  
		  }
		  
		  c)反序列化主要依赖java.io.ObjectInputStream类,该类对java.io.InputStream进一步做了封装,这里主要使用ObjectInputStream类的readObject()方法实现序列化功能
		  
		  /**
		  
		  *反序列化,将磁盘文件转化为对象
		  
		  *@paramf
		  
		  *@return
		  
		  *@throwsException
		  
		  */
		  
		  publicstaticUser readObject(File f)throwsException{
		  
		  InputStream is=newFileInputStream(f);
		  
		  //ObjectOutputStream核心类
		  
		  ObjectInputStream ois=newObjectInputStream(is);
		  
		  return(User)ois.readObject();
		  
		  }
		  
		  
### String 类

- String 类的理解和创建对象

	- 
	- 

- 创建 String 对象的常用两种方式

	- 直接赋值String a = "a";
	- 调用构造器String b = new String("b");
	- 两种创建 String 对象的区别

		- 
		- 

### 字符串的特性

- 

	- 

- 

	- 

- 

	- 
	- 
	- 
	- 

- intern方法

	- jdk1.6中
intern方法会把首次遇到的字符串复制到方法区中，返回的也是方法区这个字符串的引用。

而由StringBuilder创建的字符串实例在Java堆上，所以必然不是一个引用

		- 
		- 

	- dk1.7(jdk1.8适用)的intern方法
jdk1.7的intern方法不会在复制实例，只是在常量池中记录首次出现的实例引用

		- 
		- str2指向的引用其实就是str1指向Java堆中StringBuilder创建的字符串实例。所以返回结果为true。
但是java这个字符串常量在编译期就已经在方法区的常量池中了，不符合首次出现，所以str4指向的是常量池中的java字面量，所以返回结果为false。
问题又来了，java这个字面量为什么在编译期就出现在了常量池。我们可以进入System类中。
进入System类之后，我们发现这里有一个Version.init方法，内部已有常量，包括java，版本号，此版本号，都已经加载到常量池中，所以当我们调用str3.intern()方法时，java字面量已经存在，不符合首次出现，所以返回false，同理，我们也可以试一试这里的字面量，发现返回都是false

	- 面试问题

		- （1）现在当有人问 String str = new String(“abc”);创建了几个对象，常量池有abc字段是1个，常量池没有"abc"字段则是2个。
（2）String str=“abc”;创建了几个对象（如果常量池里面已经有对象了就是0个。如果没有就是1个）;
（3）new String(“abc”).intern();创建了几个对象（如果常量池里面已经有该字符串对象了就是1个，如果没有就是两个）

### String 类的常见方法

- 方法列表

	- equals //是否相等
equalsIgnoreCase //是否相等，忽略大小写
length //长度
indexOf //字符第一次出现的索引，无则返回-1
lastIndexOf //字符最后出现一次的索引，无则返回-1
subString //截取指定范围的子串
trim //去除前后的空格
charAt //获取某索引处的字符

toUpperCase //转大写
toLowerCase //转小写
concat //连接
replace //替换字符串的字符
split //根据正则或规则分割字符串
compareTo //比较2个字符串的大小
toCharArray //转换成字符数组
format //格式字符串

### StringBuffer 类

- 基本介绍

	- 

- String VS StringBuffer

	- 
	- String 和 StringBuffer 相互转换

		- String- >StringBuffer

			- 方式 1 使用构造器

				- StringBuffer stringBuffer = new StringBuffer(str);

			- 方式 2 使用的是 append 方法

				- StringBuffer stringBuffer1 = new StringBuffer(); 
stringBuffer1 = stringBuffer1.append(str);

		- StringBuffer ->String

			- 方式 1 使用 StringBuffer 提供的 toString 方法

				- String s = stringBuffer3.toString();

			- 方式 2: 使用构造器来搞定

				- String s1 = new String(stringBuffer3);

- StringBuffer 类常见方法

	- append //增
delete //删
replace //改
insert //插
length //长度

### StringBuilder 类

- 基本介绍

	- 

- StringBuilder 常用方法

### String、StringBuffer 和 StringBuilder 的比较

- 

### String、StringBuffer 和 StringBuilder 的效率： StringBuilder > StringBuffer > String

### String、StringBuffer 和 StringBuilder 的选择

- 

### Math 类

- 基本介绍

	- Math 类包含用于执行基本数学运算的方法，如初等指数、对数、平方根和三角函数

- 方法列表

	- abs //绝对值
pow //求幂
ceil //向上取整,返回>=该参数的最小整数(转成 double);
floor //向下取整，返回<=该参数的最大整数(转成 double)
round //四舍五入
sqrt //求开方
random //求随机数，返回的是 0 <= x < 1 之间的一个随机小数

### Arrays 类

- 常用方法

	- toString //返回数组的字符串形式
sort //排序（自然排序和定制排序）
binarySearch //二分查找，前提是有序
copyOf //数组元素的复制
fill //数组元素的填充
equals //比较2个数组元素内容是否完全一直
asList //将一组值转换为list

### System 类

- 常见方法

	- exit //退出当前程序
arrayCopy //复制数组元素，比较适合底层调用，一般使用Arrays.copyOf来做
currentTimeMillis //当前减1970-1-1的毫秒数
gc //运行垃圾回收机制

### BigInteger 和 BigDecimal 类

- BigInteger 和 BigDecimal 介绍
- BigInteger 和 BigDecimal 常见方法

	- 在对 BigInteger、BigDecimal进行加减乘除的时候，需要使用对应的方法，不能直接进行 + - * /
当我们需要保存一个精度很高的数时，double 不够用
	- add
subtract
multiply
divide

### 日期类

- 第一代日期类

	- 
	- 
	- 常用方法

		- Date d1 = new Date(); //获取当前系统时间
Date d2 = new Date(9234567); //通过指定毫秒数得到时间
SimpleDateFormat sdf = new SimpleDateFormat("yyyy 年 MM 月 dd 日 hh:mm:ss E")
String format = sdf.format(d1); // format:将日期转换成指定格式的字符串
String s = "1996 年 01 月 01 日 10:20:30 星期一"; Date parse = sdf.parse(s); 
sdf.format(parse))

- 第二代日期类

	- 
	- Calender类介绍

		- 1. Calendar 是一个抽象类， 并且构造器是 private
2. 可以通过 getInstance() 来获取实例
3. 提供大量的方法和字段提供给程序员
4. Calendar 没有提供对应的格式化的类，因此需要程序员自己组合来输出(灵活)
5. 如果我们需要按照 24 小时进制来获取时间， Calendar.HOUR ==改成=> Calendar.HOUR_OF_DAY

			- 

- 第三代日期类

	- 
	- 
	- DateTimeFormatter 格式日期类

		- 

	- Instant 时间戳

		- 

			- Instant now = Instant.now(); //通过 静态方法 now() 获取表示当前时间戳的对象
Date date = Date.from(now); //通过 from 可以把 Instant 转成 Date
Instant instant = date.toInstant(); //通过 date 的 toInstant() 可以把 date 转成 Instant 对象

	- 第三代日期类更多方法

		- 

## 13、集合

### 集合的理解和好处

- 数组有不足的地方

	- 

- 集合优点

	- 

### 集合的框架体系

- Java 的集合类主要分为两大类

	- 
	- 

### Collection接口

- Collection接口实现类的特点

	- 

- Collection接口常用方法

	- add:添加单个元素
remove:删除指定元素
contains:查找元素是否存在
size:获取元素个数
clear:清空
addAll:添加多个元素
containsAll:查找多个元素是否都存在
removeAll：删除多个元素

- Collection 接口遍历元素方式

	- 使用 Iterator(迭代器)

		- 
		- 迭代器执行原理

			- 

		- iterator接口方法

			- 
			- hasNext
next
remove
			- 
			- 
			- 

	- for 循环增强

		- 

### List 接口

- List 接口基本介绍

	- 

- List 接口的常用方法

	- add //添加
add(int index, Object ele)://在 index 位置插入元素
addAll(int index, Collection eles)://从 index 位置开始将 eles 中的所有元素添加进来
get(int index)://获取指定 index 位置的元素
 int indexOf(Object obj)://返回 obj 在集合中首次出现的位置
lastIndexOf(Object obj)://返回 obj 在当前集合中末次出现的位置
remove(int index)://移除指定 index 位置的元素，并返回此元素
set(int index, Object ele)://设置指定 index 位置的元素为 ele , 相当于是替换
subList(int fromIndex, int toIndex)://返回从 fromIndex 到 toIndex 位置的子集合；注意返回的子集合 fromIndex <= subList < toIndex


- List 的三种遍历方式 [ArrayList, LinkedList,Vector]

	- 

### ArrayList 底层结构和源码分析

- ArrayList 的注意事项

	- 

- ArrayList 的底层操作机制源码分析

	- 
	- 

### Vector 底层结构和源码剖析

- Vector 的基本介绍

	- 

- Vector 和 ArrayList 的比较

	- 

### LinkedList 底层结构

- LinkedList 的全面说明

	- 

- LinkedList 的底层操作机制

	- 

- LinkedList 的增删改查

	- add
remove
set
get

### ArrayList 和 LinkedList 比较

- 

### Set 接口

- Set 接口基本介绍

	- 

- Set 接口的常用方法

	- 和 List 接口一样, Set 接口也是 Collection 的子接口，因此，常用方法和 Collection 接口一样.

- Set 接口的遍历方式

	- 

- Set 接口实现类-HashSet

	- HashSet 的全面说明

		- 

	- HashSet 底层机制说明

		- 
		- 
		- 
		- 
		- 
		- 

- Set 接口实现类-LinkedHashSet

	- LinkedHashSet 的全面说明

		- 
		- 

### Map 接口

- Map 接口实现类的特点

	- 
	- 

- Map 接口常用方法

	- put
remove://根据键删除映射关系
get //根据键获取值
size //获取元素个数
isEmpty //判断个数是否为 0
clear //清除 k-v
containsKey //查找键是否存在
	- 

- Map 接口遍历方法

	- 
	- 1、增强 for
2、迭代器
	- 第一组: 先取出 所有的 Key , 通过 Key 取出对应的 Value

		- Set keyset = map.keySet();
//(1) 增强 for 
System.out.println("-----第一种方式-------"); for (Object key : keyset) { System.out.println(key + "-" + map.get(key)); }

//(2) 迭代器 
System.out.println("----第二种方式--------"); Iterator iterator = keyset.iterator(); while (iterator.hasNext()) { Object key = iterator.next(); System.out.println(key + "-" + map.get(key)); }

	- 第二组: 把所有的 values 取出

		- Collection values = map.values();
/(1) 增强 for
System.out.println("---取出所有的 value 增强 for----"); for (Object value : values) { System.out.println(value); }

(2) 迭代器
Iterator iterator2 = values.iterator(); while (iterator2.hasNext()) { Object value = iterator2.next();
System.out.println(value); }

	- 第三组: 通过 EntrySet 来获取 k-v

		- Set entrySet = map.entrySet();
(1) 增强 for
for (Object entry : entrySet) { //将 entry 转成 Map.Entry Map.Entry m = (Map.Entry) entry; System.out.println(m.getKey() + "-" + m.getValue()); }

(2) 迭代器
Iterator iterator3 = entrySet.iterator(); while (iterator3.hasNext()) { Object entry = iterator3.next(); //System.out.println(next.getClass());
//HashMap$Node -实现-> Map.Entry (getKey,getValue) 
//向下转型 Map.Entry Map.Entry m = (Map.Entry) entry; System.out.println(m.getKey() + "-" + m.getValue()); }

- Map 接口实现类-HashMap

	- HashMap 小结

		- 

	- HashMap 底层机制及源码剖析

		- 
		- 

- Map 接口实现类-Hashtable

	- HashTable 的基本介绍

		- 

	- Hashtable 和 HashMap 对比

		- 

- Map 接口实现类-Properties

	- 基本介绍

		- 

	- 基本使用

		- properties.put("john", 100); //增
properties.get("lic"); //查
properties.remove("lic"); //删
properties.put("john", "约翰"); //改

### 总结-开发中如何选择集合实现类

- 

### Collections 工具类

- Collections 工具类介绍

	- 

- 排序操作

	- 

- reverse
shuffle
sort
swap
max
min
frequency
copy
replaceAll

- 查找、替换

	- 

## 14、泛型

### 泛型的理解和好处

- 使用传统方法的问题分析

	- 

- 泛型的好处

	- 

### 泛型介绍

- 
- 泛型的语法

	- 泛型的声明

		- 

	- 泛型的实例化

		- 

### 泛型使用的注意事项和细节

- 

### 自定义泛型

- 基本语法

	- 

- 自定义泛型接口

	- 

- 自定义泛型方法

	- 

### 泛型的继承和通配符

- 

## 15、多线程基础

### 线程相关概念

- 程序

	- 

- 进程

	- 

- 线程

	- 
	- 线程如何理解

		- 
		- 

- 其他相关概念

	- 
	- 

### 线程基本使用

- 创建线程的两种方式

	- 
	- 线程应用案例 1-继承 Thread 类

		- 
		- 细节

			- 

	- 线程应用案例 2-实现 Runnable 接口

		- 

- 线程使用应用案例-多线程执行

	- T1 t1 = new T1();
T2 t2 = new T2();
Thread thread1 = new Thread(t1); 
Thread thread2 = new Thread(t2); 
thread1.start();//启动第 1 个线程
thread2.start();//启动第 2 个线程

### 继承 Thread vs 实现 Runnable 的区别

- 

### 线程终止

- 基本说明

	- 

### 线程常用方法

- 
- 

### 注意事项和细节

- 

### 用户线程和守护线程

- 
- 实例

	- 

### 线程的生命周期

- 线程的几种状态

	- 

- 线程状态转换图

	- 

### 线程的同步

- Synchronized

	- 线程同步机制

		- 

	- 同步具体方法-Synchronized

		- 

- 分析同步原理

	- 

### 互斥锁

- 基本介绍

	- 

- 注意事项和细节

	- 

### 线程的死锁

- 基本介绍

	- 

- 手动实现

  public class DeadLock_ {
      public static void main(String[] args) {
          //模拟死锁现象 
          DeadLockDemo A = new DeadLockDemo(true);
          A.setName("A 线程");
          DeadLockDemo B = new DeadLockDemo(false);
          B.setName("B 线程");
          A.start();
          B.start();
      }
  }
  
  
  class DeadLockDemo extends Thread {
      static Object o1 = new Object();// 保证多线程，共享一个对象,这里使用 static 
      static Object o2 = new Object();
      boolean flag;
  
      public DeadLockDemo(boolean flag) {//构造器 
          this.flag = flag;
      }
  
      @Override
      public void run() {
          //下面业务逻辑的分析 
          //1. 如果 flag 为 T, 线程 A 就会先得到/持有 o1 对象锁, 然后尝试去获取 o2 对象锁 
          //2. 如果线程 A 得不到 o2 对象锁，就会 Blocked 
          //3. 如果 flag 为 F, 线程 B 就会先得到/持有 o2 对象锁, 然后尝试去获取 o1 对象锁 
          //4. 如果线程 B 得不到 o1 对象锁，就会 Blocked 
          if (flag) {
              synchronized (o1) {//对象互斥锁, 下面就是同步代码 
                  System.out.println(Thread.currentThread().getName() + " 进入 1");
                  synchronized (o2) { // 这里获得 li 对象的监视权 
                      System.out.println(Thread.currentThread().getName() + " 进入 2");
                  }
              }
          } else {
              synchronized (o2) {
                  System.out.println(Thread.currentThread().getName() + " 进入 3");
                  synchronized (o1) { // 这里获得 li 对象的监视权 
                      System.out.println(Thread.currentThread().getName() + " 进入 4");
                  }
              }
          }
      }
  }
  
  
### 释放锁

- 会释放锁的操作

	- 

- 不会释放锁的操作

	- 

## 16、IO流

### 文件

- 什么是文件

	- 

- 文件流

	- 

### 常用的文件操作

- 创建文件对象相关构造器和方法

	- 
	- File file = new File(“e:\\news1.txt”);
File file = new File(new File("e:\\"), "news2.txt");
File file = new File("e:\\", "news4.txt");

- 获取文件的相关信息

	- 
	- 
	- getName
getAbsolutePath
getParent
length
exists
isFile
isDirectory

- 目录的操作和文件删除

	- 
	- mkdir
mkdirs
delete

### IO 流原理及流的分类

- Java IO 流原理

	- 
	- 

- 流的分类

	- 

### IO 流体系图-常用的类

- 
- 文件 VS 流的关系

	- 

- FileInputStream
FileOutputStream
FileReader
FileWriter

	- 
	- 
	- 
	- FileReader 相关方法

		- 

	- FileWriter 常用方法

		- 

### 节点流和处理流

- 基本介绍

	- 

- 节点流和处理流一览图

	- 

- 节点流和处理流的区别和联系

	- 

- 处理流的功能主要体现在以下两个方面

	- 

- 处理流-BufferedReader 和 BufferedWriter

	- 

- 处理流-BufferedInputStream 和 BufferedOutputStream

	- BufferedInputStream、BufferedOutputStream介绍

		- 
		- 
		- 
		- 

- 对象流-ObjectInputStream 和 ObjectOutputStream

	- 
	- 
	- 对象流介绍

		- 功能：提供了对基本类型或对象类型的序列化和反序列化的方法
		- ObjectOutputStream 提供 序列化功能 ObjectInputStream 提供 反序列化功能

			- 
			- 
			- 注意事项

				- 

- 标准输入输出流

	- 

- 转换流-InputStreamReader 和 OutputStreamWriter

	- 文件乱码问题，转换流必要性
	- 

### 打印流-PrintStream 和 PrintWriter

- 
- 

### Properties 类

- 应用场景

	- 
	- 

- 基本介绍

	- 

- 常用方法

	- 

## 17、网络编程

### 网络的相关概念

- 网络通信

	- 

- 网络

	- 

- ip 地址

	- 
	- ipv4 地址分类

		- 
		- 

- 域名、端口

	- 

- 网络通信协议

	- 
	- 
	- 
	- TCP 和 UDP

		- 

### InetAddress 类

- 相关方法

	- 

### Socket

- 基本介绍

	- 
	- 

### TCP 网络通信编程

- 基本介绍

	- 

- 
- netstat 指令

	- 

- TCP 网络通讯

	- 

### UDP 网络通信编程

- 基本介绍

	- 
	- 

- 基本流程

	- 

## 18、反射

### 为什么需要反射

- 需求：
1. 通过外部配置文件，在不修改源码的情况下，控制程序
2. 根据配置文件创建对象

	- 

### 反射机制

- 
- Java 反射机制原理示意图

	- 

### Java 反射可以做的

- 

### 反射相关的主要类

- 
- Class
Field
Method
Constructor

	- Class cls = Class.forName(classfullpath); //加载类, 返回 Class 类型的对象 cls
Object o = cls.newInstance(); //通过 cls 得到你加载的类的对象实例
Method method1 = cls.getMethod(methodName); //通过 cls 得到你加载的类的方法对象
method1.invoke(o); //通过 method1 调用方法: 即通过方法对象来实现调用方法；传统方法 对象.方法() , 反射机制 方法.invoke(对象)
Field nameField = cls.getField("age"); //java.lang.reflect.Field: 代表类的成员变量, Field 对象表示某个类的成员变量，传统写法 对象.成员变量 , 反射 : 成员变量对象.get(对象)；getField 不能得到私有的属性
Constructor constructor = cls.getConstructor(); //()中可以指定构造器参数类型, 返回无参构造器；/java.lang.reflect.Constructor: 代表类的构造方法, Constructor 对象表示构造器

### 反射优点和缺点

- 

### 反射调用优化-关闭访问检查

- 
- 

### Class 类

- 基本介绍

	- 
	- 

- Class 类的常用方法

	- 

- 获取 Class 类对象方式

	- 

- 哪些类型有 Class 对象

	- 

### 类加载

- 基本说明

	- 

- 类加载时机

	- 

- 类加载过程图

	- 

- 类加载各阶段完成任务

	- 
	- 加载阶段

		- 

	- 连接阶段-验证

		- 

	- 连接阶段-准备

		- 

	- 连接阶段-解析

		- 

	- Initialization（初始化)

		- 

### 通过反射获取类的结构信息

- java.lang.Class 类

	- 

- java.lang.reflect.Field 类

	- 

- java.lang.reflect.Method 类

	- 

- java.lang.reflect.Constructor 类

	- 

### 通过反射创建对象

- 

### 通过反射访问类中的成员

- 访问属性

	- 

- 访问方法

	- 

## 19、零基础学MySQL

### 使用命令行窗口连接 MYSQL 数据库

- 
- 

### 数据库三层结构

- 

	- 

### 数据在数据库中的存储方式

- 

### SQL 语句分类

- 

### 创建数据库

- 

### 查看、删除数据库

- 

### 备份恢复数据库

- 

### 备份恢复数据库的表

- 

### 创建表

- 

### Mysql 常用数据类型(列类型)

- 

	- 数值型(整数)的基本使用

		- 
		- 定义一个无符号的整数

			- 

	- 数值型(bit)的使用

		- 

	- 数值型(小数)的基本使用

		- 

	- 字符串的基本使用

		- 
		- 字符串使用细节

			- 
			- 
			- 
			- 

	- 日期类型的基本使用

		- 

### 表操作

- 创建表

	- CREATE TABLE `emp` ( id INT, `name` VARCHAR(32), sex CHAR(1), brithday DATE,entry_date DATETIME, job VARCHAR(32), salary DOUBLE, `resume` TEXT) CHARSET utf8 COLLATE utf8_bin ENGINE INNODB;

- 修改表

	- 
	- DESC employee -- 显示表结构，可以查看表的所有列

### 数据库 C[create]R[read]U[update]D[delete]语句

-- select 语句 
CREATE TABLE student( id INT NOT NULL DEFAULT 1, 
NAME VARCHAR(20) NOT NULL DEFAULT '', 
chinese FLOAT NOT NULL DEFAULT 0.0, 
english FLOAT NOT NULL DEFAULT 0.0, 
math FLOAT NOT NULL DEFAULT 0.0 );

INSERT INTO student(id,NAME,chinese,english,math) VALUES(1,'韩顺平',89,78,90); 
INSERT INTO student(id,NAME,chinese,english,math) VALUES(2,'张飞',67,98,56); 
INSERT INTO student(id,NAME,chinese,english,math) VALUES(3,'宋江',87,78,77); 
INSERT INTO student(id,NAME,chinese,english,math) VALUES(4,'关羽',88,98,90); 
INSERT INTO student(id,NAME,chinese,english,math) VALUES(5,'赵云',82,84,67); 
INSERT INTO student(id,NAME,chinese,english,math) VALUES(6,'欧阳锋',55,85,45); 
INSERT INTO student(id,NAME,chinese,english,math) VALUES(7,'黄蓉',75,65,30); 
INSERT INTO student(id,NAME,chinese,english,math) VALUES(8,'韩信',45,65,99); 

SELECT * FROM student; 
-- 查询表中所有学生的信息。 
SELECT * FROM student; 
-- 查询表中所有学生的姓名和对应的英语成绩。 
SELECT `name`,english FROM student; 
-- 过滤表中重复数据 distinct
SELECT DISTINCT english FROM student; 
-- 要查询的记录，每个字段都相同，才会去重 
SELECT DISTINCT `name`, english FROM student;

- insert
delete
update
select

	- Insert 语句

		- 

	- update 语句

		- 
		- 使用细节

			- 

	- delete 语句

		- 
		- 使用细节

			- 

	- select 语句

	  -- 统计每个学生的总分 
	  SELECT `name`, (chinese+english+math) FROM student; 
	  -- 在所有学生总分加 10 分的情况 
	  SELECT `name`, (chinese + english + math + 10) FROM student; 
	  -- 使用别名表示学生分数
	  SELECT `name` AS '名字', (chinese + english + math + 10) AS total_score FROM student;
	  SELECT `name`, (chinese + english + math) AS total_score FROM student  WHERE `name` LIKE '韩%'  ORDER BY total_score;
	  
		- 
		- 注意事项

			- 

		- 使用表达式对查询的列进行运算

			- 

		- 在 select 语句中可使用 as 语句

			- 

		- 在 where 子句中经常使用的运算符

			- 

		- 使用 order by 子句排序查询结果

			- 

### 合计/统计函数

- count

	- 
	- SELECT COUNT(*) FROM student;
SELECT COUNT(*) FROM student WHERE math > 90;
SELECT COUNT(*) FROM student WHERE (math + english + chinese) > 250;

- sum

	- 
	- SELECT SUM(math) FROM student;
SELECT SUM(math) AS math_total_score,SUM(english),SUM(chinese) FROM student;
SELECT SUM(math + english + chinese) FROM student;
SELECT SUM(chinese)/ COUNT(*) FROM student;
SELECT SUM(`name`) FROM student;

- avg

	- 
	- SELECT AVG(math) FROM student;
SELECT AVG(math + english + chinese) FROM student;

- max/min

	- 
	- SELECT MAX(math + english + chinese), MIN(math + english + chinese) FROM student;
SELECT MAX(math) AS math_high_socre, MIN(math) AS math_low_socre FROM student;

- group by

	- 
	- SELECT AVG(sal), MAX(sal) , deptno FROM emp GROUP BY deptno;
SELECT FORMAT(AVG(sal),2), MAX(sal) , deptno FROM emp GROUP BY deptno;
SELECT AVG(sal), MIN(sal) , deptno, job FROM emp GROUP BY deptno, job;
SELECT AVG(sal), deptno FROM emp GROUP BY deptno HAVING AVG(sal) < 2000;
SELECT AVG(sal) AS avg_sal, deptno FROM emp GROUP BY deptno HAVING avg_sal < 2000;

- having

	- 
	- 

### 字符串相关函数

- 
- SELECT CHARSET(ename) FROM emp;
SELECT CONCAT(ename, ' 工作是 ', job) FROM emp;
SELECT INSTR('hanshunping', 'ping') FROM DUAL;
SELECT UCASE(ename) FROM emp;
SELECT LCASE(ename) FROM emp;
SELECT LEFT(ename, 2) FROM emp;
SELECT LENGTH(ename) FROM emp;
SELECT ename, REPLACE(job,'MANAGER', '经理') FROM emp;
SELECT STRCMP('hsp', 'hsp') FROM DUAL;
SELECT SUBSTRING(ename, 1, 2) FROM emp;
SELECT LTRIM(' abc') FROM DUAL;
SELECT RTRIM('svx  ') FROM DUAL;
SELECT TRIM(' sbx ') FROM DUAL;
SELECT CONCAT(LCASE(SUBSTRING(ename,1,1)), SUBSTRING(ename,2)) AS new_name FROM emp;
SELECT CONCAT(LCASE(LEFT(ename,1)), SUBSTRING(ename,2)) AS new_name FROM emp;

### 数学相关函数

- 
- SELECT ABS(-10) FROM DUAL;
SELECT BIN(10) FROM DUAL;
SELECT CEILING(-1.1) FROM DUAL;
SELECT CONV(8, 10, 2) FROM DUAL;
SELECT CONV(16, 16, 10) FROM DUAL;
SELECT FLOOR(-1.1) FROM DUAL;
SELECT FORMAT(78.125458,2) FROM DUAL;
SELECT LEAST(0,1, -10, 4) FROM DUAL;
SELECT MOD(10, 3) FROM DUAL;
SELECT RAND() FROM DUAL;
SELECT CURRENT_TIMESTAMP() FROM DUAL;

### 时间日期相关函数

- 
- SELECT CURRENT_DATE() FROM DUAL;
SELECT CURRENT_TIME() FROM DUAL;
SELECT CURRENT_TIMESTAMP() FROM DUAL;
SELECT id, content, DATE(send_time) FROM mes;
SELECT * FROM mes WHERE DATE_ADD(send_time, INTERVAL 10 MINUTE) >= NOW()
SELECT * FROM mes WHERE send_time >= DATE_SUB(NOW(), INTERVAL 10 MINUTE)
SELECT DATEDIFF('2011-11-11', '1990-01-01') FROM DUAL;
SELECT DATEDIFF(NOW(), '1986-11-11') FROM DUAL;
SELECT DATEDIFF(DATE_ADD('1986-11-11', INTERVAL 80 YEAR), NOW()) FROM DUAL;
SELECT TIMEDIFF('10:11:11', '06:10:10') FROM DUAL;
SELECT YEAR(NOW()) FROM DUAL; 
SELECT MONTH(NOW()) FROM DUAL; SELECT DAY(NOW()) FROM DUAL; 
SELECT MONTH('2013-11-10') FROM DUAL;
SELECT UNIX_TIMESTAMP() FROM DUAL;
SELECT FROM_UNIXTIME(1618483484, '%Y-%m-%d') FROM DUAL;
SELECT FROM_UNIXTIME(1618483100, '%Y-%m-%d %H:%i:%s') FROM DUAL;
SELECT * FROM mysql.user \G

### 加密和系统函数

- 
- SELECT USER() FROM DUAL; -- 用户@IP 地址
SELECT DATABASE();
SELECT MD5('hp1') FROM DUAL;
SELECT LENGTH(MD5('h1p')) FROM DUAL;
SELECT PASSWORD('hp1') FROM DUAL;
select * from mysql.user \G 从原文密码 str 计算并返回密码字符串


### 流程控制函数

- 
- SELECT IF(TRUE, '北京', '上海') FROM DUAL;
SELECT IFNULL( NULL, '韩顺平教育') FROM DUAL;
SELECT CASE WHEN TRUE THEN 'jack' WHEN FALSE THEN 'tom' ELSE 'mary' END
SELECT ename, IF(comm IS NULL , 0.0, comm) FROM emp;
SELECT ename, IFNULL(comm, 0.0) FROM emp;
SELECT ename, (SELECT CASE WHEN job = 'CLERK' THEN '职员' WHEN job = 'MANAGER' THEN '经理' WHEN job = 'SALESMAN' THEN '销售人员' ELSE job END) AS 'job' FROM emp;


### mysql 表查询--加强

- 使用 where 子句

	- SELECT * FROM emp WHERE hiredate > '1992-01-01'

- 如何使用 like 操作符

	- %: 表示 0 到多个任意字符
	- ?如何显示首字符为 S 的员工姓名和工资
	-  _: 表示单个任意字符
	- // 如何显示首字符为 S 的员工姓名和工资
SELECT ename, sal FROM emp WHERE ename LIKE 'S%
//如何显示第三个字符为大写 O 的所有员工的姓名和工资
SELECT ename, sal FROM emp WHERE ename LIKE '__O%'
//如何显示没有上级的雇员的情况
SELECT * FROM emp WHERE mgr IS NULL;
//查询表结构
DESC emp


- 分页查询

	- 

		- //第 1 页
SELECT * FROM emp ORDER BY empno LIMIT 0, 3;
//第 2 页
SELECT * FROM emp ORDER BY empno LIMIT 3, 3;
//第 3 页
SELECT * FROM emp ORDER BY empno LIMIT 6, 3;

	- //公式
SELECT * FROM emp ORDER BY empno LIMIT 每页显示记录数 * (第几页-1) , 每页显示记录数

- 使用分组函数和分组子句 group by

	- SELECT COUNT(*), AVG(sal), job FROM emp GROUP BY job;
SELECT COUNT(*), COUNT(comm) FROM emp
SELECT COUNT(*), COUNT(IF(comm IS NULL, 1, NULL)) FROM emp
SELECT COUNT(*), COUNT(*) - COUNT(comm) FROM emp
SELECT COUNT(DISTINCT mgr) FROM emp;
SELECT MAX(sal) - MIN(sal) FROM emp;
SELECT deptno, AVG(sal) AS avg_sal FROM emp GROUP BY deptno HAVING avg_sal > 1000 ORDER BY avg_sal DESC LIMIT 0,2

### sql顺序

- sql 书写顺序为：
select * from  * where * group by * having *  order by *
- sql执行和书写顺序是不同的，执行顺序为：
from -- where -- group by -- having -- select -- order by --
- 
- 

### mysql 多表查询

- 说明

	- 

- 多表查询

	- SELECT ename,sal,dname,emp.deptno FROM emp, dept WHERE emp.deptno = dept.deptno
SELECT ename,sal,dname,emp.deptno FROM emp, dept WHERE emp.deptno = dept.deptno AND emp.deptno = 10
select ename, sal, grade from emp , salgrade where sal between losal and hisal;

- 自连接

	- SELECT worker.ename AS '职员名' , boss.ename AS '上级名' FROM emp worker, emp boss WHERE worker.mgr = boss.empno;

### mysql 表子查询

- 什么是子查询

	- 子查询是指嵌入在其它 sql 语句中的 select 语句,也叫嵌套查询
	- 单行子查询

		- 单行子查询是指只返回一行数据的子查询语句

	- 多行子查询

		- 多行子查询指返回多行数据的子查询

			- SELECT * FROM emp WHERE deptno = ( SELECT deptno FROM emp WHERE ename = 'SMITH' )

select ename, job, sal, deptno from emp where job in ( SELECT DISTINCT job FROM emp WHERE deptno = 10 ) and deptno <> 10

- 在多行子查询中使用 all/any 操作符

	- all 和 any 的使用
	- SELECT ename, sal, deptno FROM emp WHERE sal > ALL( SELECT sal FROM emp WHERE deptno = 30 )

SELECT ename, sal, deptno FROM emp WHERE sal > ( SELECT MAX(sal) FROM emp WHERE deptno = 30 )

SELECT ename, sal, deptno FROM emp WHERE sal > any( SELECT sal FROM emp WHERE deptno = 30 )

SELECT ename, sal, deptno FROM emp WHERE sal > ( SELECT min(sal) FROM emp WHERE deptno = 30 )

- any，in，some，all

	- 子查询关键词

		- operand comparison_operator any (subquery);
operand in (subquery);
operand coparison_operator some (subquery);
operand comparison_operator all (subquery);

	- any关键词可以理解为“对于子查询返回的列中的任一数值，如果比较结果为true，则返回true”。
	- all的意思是“对于子查询返回的列中的所有值，如果比较结果为true，则返回true”
	- 语句some是any的别名，用法相同
	- not in 是 “<>all”的别名，用法相同。
	- 语句in 与“=any”是相同的。

- 多列子查询

	- 

		- SELECT * FROM emp WHERE (deptno , job) = ( SELECT deptno , job FROM emp WHERE ename = 'ALLEN' ) AND ename != 'ALLEN'

SELECT * FROM student WHERE (math, english, chinese) = ( SELECT math, english, chinese FROM student WHERE `name` = '宋江' )

- 在 from 子句中使用子查询

	- SELECT ename, sal, temp.avg_sal, emp.deptno 
FROM emp, (SELECT deptno, AVG(sal) AS avg_sal FROM emp GROUP BY deptno ) temp 
WHERE emp.deptno = temp.deptno AND emp.sal > temp.avg_sal

SELECT ename, sal, temp.max_sal, emp.deptno FROM emp, ( SELECT deptno, MAX(sal) AS max_sal FROM emp GROUP BY deptno ) temp WHERE emp.deptno = temp.deptno AND emp.sal = temp.max_sal

SELECT dname, dept.deptno, loc , tmp.per_num AS '人数' FROM dept, ( SELECT COUNT(*) AS per_num, deptno FROM emp GROUP BY deptno ) tmp WHERE tmp.deptno = dept.deptno

SELECT tmp.* , dname, loc FROM dept, ( SELECT COUNT(*) AS per_num, deptno FROM emp GROUP BY deptno ) tmp WHERE tmp.deptno = dept.deptno

### 表复制

- 自我复制数据

	- -- 表的复制
CREATE TABLE my_tab01 ( id INT, `name` VARCHAR(32), sal DOUBLE, job VARCHAR(32), deptno INT); 
DESC my_tab01 
SELECT * FROM my_tab01;
INSERT INTO my_tab01 (id, `name`, sal, job,deptno) SELECT empno, ename, sal, job, deptno FROM emp;

-- 自我复制
INSERT INTO my_tab01 SELECT * FROM my_tab01; SELECT COUNT(*) FROM my_tab01;

-- 如何删除掉一张表重复记录
思路
(1) 先创建一张临时表 my_tmp , 该表的结构和 my_tab02 一样 
(2) 把 my_tmp 的记录 通过 distinct 关键字 处理后 把记录复制到 my_tmp 
(3) 清除掉 my_tab02 记录 
(4) 把 my_tmp 表的记录复制到 my_tab02 
(5) drop 掉 临时表 my_tmp
create table my_tmp like my_tab02
insert into my_tmp select distinct * from my_tab02;
delete from my_tab02;
insert into my_tab02 select * from my_tmp;
drop table my_tmp;
select * from my_tab02;

### 合并查询

- 介绍

	- 
	- 
	- -- union all 就是将两个查询结果合并，不会去重 
SELECT ename,sal,job FROM emp WHERE sal>2500 -- 5 
UNION ALL
SELECT ename,sal,job FROM emp WHERE job='MANAGER' -- 3

-- union 就是将两个查询结果合并，会去重 
SELECT ename,sal,job FROM emp WHERE sal>2500 -- 5 
UNION
SELECT ename,sal,job FROM emp WHERE job='MANAGER' -- 3

### mysql 表外连接

- 外连接

	- 
	- -- 左连接
SELECT `name`, stu.id, grade FROM stu, exam WHERE stu.id = exam.id;

-- 左外连接
SELECT `name`, stu.id, grade FROM stu LEFT JOIN exam ON stu.id = exam.id;

-- 右外连接
SELECT `name`, stu.id, grade FROM stu RIGHT JOIN exam ON stu.id = exam.id;

-- 左外连接
SELECT dname, ename, job FROM dept LEFT JOIN emp ON dept.deptno = emp.deptno


### mysql 约束

- 基本介绍

	- 

		- primary key(主键)

			- 
			- primary key 不能重复而且不能为 null
一张表最多只能有一个主键, 但可以是复合主键(比如 id+name)

CREATE TABLE t18 (id INT , 
`name` VARCHAR(32),
email VARCHAR(32), 
PRIMARY KEY (id, `name`) -- 这里就是复合主键 );
			- 主键的指定方式 有两种

				- 1. 直接在字段名后指定：字段名 primakry key
				- 2. 在表定义最后写 primary key(列名);

		- not null(非空)

			- 

		- unique(唯一)

			- 
			- 1. 如果没有指定 not null , 则 unique 字段可以有多个 null
			- 2 一张表可以有多个 unique 字段

		- foreign key(外键)

			- 
			- 
			- 
			- CREATE TABLE my_stu ( 
id INT PRIMARY KEY , -- 学生编号 
`name` VARCHAR(32) NOT NULL DEFAULT '', 
class_id INT , -- 学生所在班级的编号 
-- 下面指定外键关系 
FOREIGN KEY (class_id) REFERENCES my_class(id))

-- 一旦建立主外键的关系，数据不能随意删除了

		- check

			- 
			- CREATE TABLE t23 ( 
id INT PRIMARY KEY, 
`name` VARCHAR(32) , 
sex VARCHAR(6) CHECK (sex IN('man','woman')),
sal DOUBLE CHECK ( sal > 1000 AND sal < 2000) );

### 自增长

- 
- 自增长使用细节

	- 

- CREATE TABLE t24 (
id INT PRIMARY KEY AUTO_INCREMENT, 
email VARCHAR(32)NOT NULL DEFAULT '', 
`name` VARCHAR(32)NOT NULL DEFAULT '');

-- 修改默认的自增长开始值
ALTER TABLE t25 AUTO_INCREMENT = 100

### mysql 索引

创建索引后，只对创建了索引的列有效

- 好处

	- 提升数据库性能，无需改程序或加内存，查询速度可以提升百倍千倍

- 问题

	- 索引本身也会占用空间

-  -- 在 emp表ename 字段上创建索引
CREATE INDEX ename_index ON emp (ename)
- 索引的原理

	- 
	- 根据项目中select的次数[90%]、update、delete、insert哪种操作多来决定

- 索引的类型

	- 

- 索引使用

	- 
	- 
	- -- 查询表是否有索引
SHOW INDEXES FROM t25;
-- 添加唯一索引
CREATE UNIQUE INDEX id_index ON t25 (id);
-- 添加普通索引方式 1
CREATE INDEX id_index ON t25 (id);
-- 添加普通索引方式 2 
ALTER TABLE t25 ADD INDEX id_index (id)
-- 删除索引
DROP INDEX id_index ON t25
-- 删除主键索引
ALTER TABLE t26 DROP PRIMARY KEY
-- 修改索引 ， 先删除，在添加新的索引

-- 查询索引 
-- 1. 方式 
SHOW INDEX FROM t25
 -- 2. 方式 
SHOW INDEXES FROM t25
-- 3. 方式
SHOW KEYS FROM t25
-- 4 方式
DESC t25

- 索引选择

	- 1. 如果某列的值，是不会重复的，则优先考虑使用 unique 索引, 否则使用普通索引
	- 哪些列上适合使用索引

		- 

### mysql 事务

- 什么是事务

	- 
	- 示意图

		- 
		- -- 2. 开始事务
START TRANSACTION
-- 3. 设置保存点 
SAVEPOINT a
-- 执行 dml 操作 
INSERT INTO t27 VALUES(100, 'tom');
SELECT * FROM t27;
SAVEPOINT b
-- 回退到 b 
ROLLBACK TO b 
-- 继续回退 a 
ROLLBACK TO a
-- 如果这样, 表示直接回退到事务开始的状态. ROLLBACK
COMMIT

- 事务和锁

	- 
	- 回退事务

		- 子主题 1

	- 提交事务

		- 

	- 事务细节

		- 

### mysql 事务隔离级别

- 事务隔离级别介绍以及必要性

	- 

- 查看事务隔离级别

	- 

- 事务隔离级别

	- 
	- 设置事务隔离级别

		- 
		- 

	- -- 2. 查看当前 mysql 的隔离级别 
SELECT @@tx_isolation;
-- 3.把其中一个控制台的隔离级别设置 Read uncommitted
SET SESSION TRANSACTION ISOLATION LEVEL READ UNCOMMITTED

### mysql 事务 ACID

- 事务的 acid 特性

	- 

### mysql 表类型和存储引擎

- 基本介绍

	- 

- 主要的存储引擎/表类型特点

	- 

- 细节说明

	- 三种: MyISAM、InnoDB、MEMORY

		- 
		- -- 查看所有的存储引擎 
SHOW ENGINES

CREATE TABLE t28 ( id INT, `name` VARCHAR(32)) ENGINE MYISAM

CREATE TABLE t29 ( id INT, `name` VARCHAR(32)) ENGINE MEMORY

-- 指令修改存储引擎 
ALTER TABLE `t29` ENGINE = INNODB

- 如何选择表的存储引擎

	- 

- 修改存储引擎

	- ALTER TABLE `tableName` ENGINE = engineType

### 视图(view)

- 基本概念

	- 

- 视图的基本使用

	- 
	- -- 创建视图
CREATE VIEW emp_view01 AS SELECT empno, ename, job, deptno FROM emp;
-- 查看视图 
DESC emp_view01
-- 查看创建视图的指令 
SHOW CREATE VIEW emp_view01
-- 删除视图 
DROP VIEW emp_view01;

- 视图的细节

	- - 1. 创建视图后，到数据库去看，对应视图只有一个视图结构文件(形式: 视图名.frm)
	- 2. 视图的数据变化会影响到基表，基表的数据变化也会影响到视图[insert update delete ]
	- 3 改基本表， 会影响到视图
	- 4. 视图中可以再使用视图 , 比如从 emp_view01 视图中，选出 empno,和 ename 做出新视图

- 视图选择

	- 

### Mysql 管理

- Mysql 用户

	- 

- 创建用户

	- 

- 删除用户

	- 

- 用户修改密码

	- 

- mysql 中的权限

	- 

- 给用户授权

	- 

- 回收用户授权

	- 

- 权限生效指令

	- 

- 实例

	- -- 创建用户
CREATE USER 'sng'@'localhost' IDENTIFIED BY '12345678'

-- 给 sng 分配查看 news 表和 添加 news 的权限
GRANT SELECT , INSERT ON testdb.news TO 'sng'@'localhost

-- 可以增加 update 权限 
GRANT UPDATE ON testdb.news TO 'sng'@'localhost'

-- 修改 sng 的密码为 abc
SET PASSWORD FOR 'sng'@'localhost' = PASSWORD('abc');

-- 回收 sng 用户在 testdb.news 表的所有权限
REVOKE SELECT , UPDATE, INSERT ON testdb.news FROM 'sng'@'localhost' 
REVOKE ALL ON testdb.news FROM 'sng'@'localhost'


-- 删除 sng
DROP USER 'sng'@'localhost

## 20、JDBC和数据库连接池

### JDBC 概述

- 基本介绍

	- 
	- 原理

		- 

- JDBC 好处

	- 
	- 
	- 

- JDBC API

	- 

### JDBC 快速入门

- JDBC 程序编写步骤

	- 
	- //1. 注册驱动 
Driver driver = new Driver(); //创建 driver 对象

//2. 得到连接
String url = "jdbc:mysql://localhost:3306/hsp_db02";
Properties properties = new Properties();
properties.setProperty("user", "root");// 用户 
properties.setProperty("password", "hsp"); //密码
Connection connect = driver.connect(url, properties);

//3. 执行 sql
String sql = "delete from actor where id = 1";
Statement statement = connect.createStatement(); 
int rows = statement.executeUpdate(sql); // 如果是 dml 语句，返回的就是影响行数

//4. 关闭连接资源
statement.close(); 
connect.close();

### 获取数据库连接 5 种方式

- 方式 1

	- 

- 方式 2

	- 

- 方式 3

	- 

- 方式 4

	- 
	- 

- 方式 5

	- 

### ResultSet[结果集]

- 基本介绍

	- 
	- 
	- 实例

		- 

### Statement

- 基本介绍

	- 

- statement使用方式

	- Statement statement = connection.createStatement(); 
//4. 组织 SqL 
String sql = "select name , pwd from admin where name ='" + admin_name + "' and pwd = '" + admin_pwd + "'"; 
ResultSet resultSet = statement.executeQuery(sql);

- PreparedStatement

	- 基本介绍

		- 

	- 预处理好处

		- 

	- 使用方式

		- String sql = "select name , pwd from admin where name =? and pwd = ?";
PreparedStatement preparedStatement = connection.prepareStatement(sql);
preparedStatement.setString(1, admin_name);
preparedStatement.setString(2, admin_pwd);
ResultSet resultSet = preparedStatement.executeQuery(sql);

### JDBC 的相关 API 小结

- 

### 事务

- 基本介绍

	- 

- 实现方式

	- //将 connection 设置为不自动提交
connection.setAutoCommit(false); //开启了事务
preparedStatement = connection.prepareStatement(sql);
preparedStatement.executeUpdate(); // 执行第 1 条 sql
int i = 1 / 0; //抛出异常
preparedStatement = connection.prepareStatement(sql2);
preparedStatement.executeUpdate(); // 执行第 3 条 sql
//这里提交事务
connection.commit();


//异常捕获之后处理
//这里我们可以进行回滚，即撤销执行的 SQL
//默认回滚到事务开始的状态
connection.rollback();

//finally执行
//关闭资源

### 批处理

- 基本介绍

	- 

### 数据库连接池

- 传统获取 Connection 问题分析

	- 

- 数据库连接池种类

	- 
	- druid实例

		- Properties properties = new Properties();
properties.load(new FileInputStream("src\\druid.properties"));
DataSource dataSource = DruidDataSourceFactory.createDataSource(properties);

Connection connection = dataSource.getConnection();
connection.close();

### DAO 和增删改查通用方法-BasicDao

- 问题

	- 
	- 分层开发规范

		- 

- 基本说明

	- 

## 21、正则表达式

### 文字、字符匹配

//1. 先创建一个 Pattern 对象 ， 模式对象, 可以理解成就是一个正则表达式对象 
//Pattern pattern = Pattern.compile("[a-zA-Z]+"); 
//Pattern pattern = Pattern.compile("[0-9]+"); 
//Pattern pattern = Pattern.compile("([0-9]+)|([a-zA-Z]+)"); 
//Pattern pattern = Pattern.compile("<a target=\"_blank\" title=\"(\\S*)\"");

### 基本介绍

- 

### 正则表达式机制

什么是分组，比如 (\d\d)(\d\d) ,正则表达式中有() 表示分组,第 1 个()表示第 1 组,第 2 个()表示第 2 组... 
1. 根据指定的规则 ,定位满足规则的子字符串(比如(19)(98)) 
2. 找到后，将 子字符串的开始的索引记录到 matcher 对象的属性 int[] groups; 
	2.1 groups[0] = 0 , 把该子字符串的结束的索引+1 的值记录到 groups[1] = 4 
	2.2 记录 1 组()匹配到的字符串 groups[2] = 0 groups[3] = 2 
	2.3 记录 2 组()匹配到的字符串 groups[4] = 2 groups[5] = 4 
	2.4.如果有更多的分组..... 
3. 同时记录 oldLast 的值为 子字符串的结束的 索引+1 的值即 35, 即下次执行 find 时，就从 35 开始匹配

- 1. 如果正则表达式有() 即分组 
2. 取出匹配的字符串规则如下 
3. group(0) 表示匹配到的子字符串 
4. group(1) 表示匹配到的子字符串的第一组字串 
5. group(2) 表示匹配到的子字符串的第 2 组字串 
6. 但是分组的数不能越界
- 

### 正则表达式语法

- 基本介绍

	- 

- 元字符(Metacharacter)-转义号 \\

	- 
	- 

- 元字符-字符匹配符

	- 
	- 

- 元字符-选择匹配符

	- 

- 元字符-限定符

  用于指定其前面的字符和组合项连续出现多少次
  
	- 

- 元字符-定位符

  定位符, 规定要匹配的字符串出现的位置，比如在字符串的开始还是在结束的位置
  
	- 

- 分组

	- 
	- 

### 应用实例

// 汉字 
String regStr = "^[\u0391-\uffe5]+$";

// 邮政编码 要求：1.是 1-9 开头的一个六位数. 比如：123890
String regStr = "^[1-9]\\d{5}$"; 

//QQ 号码 要求: 是 1-9 开头的一个(5 位数-10 位数) 比如: 12389 , 1345687 , 187698765
String regStr = "^[1-9]\\d{4,9}$";

//手机号码 要求: 必须以 13,14,15,18 开头的 11 位数 , 比如 13588889999
String regStr = "^1[3|4|5|8]\\d{9}$";

Pattern pattern = Pattern.compile(regStr); 
Matcher matcher = pattern.matcher(content); 
if(matcher.find()) { 
System.out.println("满足格式"); 
} else {
System.out.println("不满足格式"); 
}



### 正则表达式三个常用类

- 

### 分组、捕获、反向引用

- 
- 实例

	- 

### String 类中使用正则表达式

- 替换功能

	- public String replaceAll(String regex,String replacement)

- 判断功能

	- public boolean matches(String regex){} //使用 Pattern 和 Matcher 类

- 分割功能

	- public String[] split(String regex)

