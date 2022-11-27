# JDK

## JDK简介

 jdk全称“Java Development Kit”，指的是Java语言的软件开发工具包，主要用于移动设备、嵌入式设备上的java应用程序的开发。jdk是java开发的核心，包括了Java运行环境、一堆Java工具和Java基础的类库。 

**JDK包含的基本组件包括：**

- javac – 编译器，将源程序转成字节码
- jar – 打包工具，将相关的类文件打包成一个文件
- javadoc – 文档生成器，从源码注释中提取文档
- jdb – debugger，查错工具
- java – 运行编译后的java程序（.class后缀的）
- appletviewer：小程序浏览器，一种执行HTML文件上的Java小程序的Java浏览器。
- Javah：产生可以调用Java过程的C过程，或建立能被Java程序调用的C过程的头文件。
- Javap：Java反汇编器，显示编译类文件中的可访问功能和数据，同时显示字节代码含义。
- Jconsole: Java进行系统调试和监控的工具

JDK=Java开发工具+JRE

JRE=JVM+Java类库

- JDK 用于开发，JRE 用于运行Java程序 ；如果只是运行Java程序，可以只安装JRE，无序安装JDK。
- JDk包含JRE，JDK 和 JRE 中都包含 JVM。
- JVM 是 Java 编程语言的核心并且具有平台独立性。

## 卸载JDK

1.通过环境变量找到jdk路径 删除java的安装目录

2.删除环境变量中的java_home

3.删除path下的java目录

4.java-version检测



## 安装jdk

1.搜索jdk8，点击下载地址[https://www.oracle.com/java/technologies/downloads/#java8-windows]

![1669555966035](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669555966035.png)

2.同意协议，根据电脑系统选择下载

![1669556027639](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669556027639.png)

下载时需要登录Oracle账户，没有的话需要进行注册。

![1669556059080](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669556059080.png)



![1669556145084](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669556145084.png)

3.安装

![1669556204703](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669556204703.png)

点击更改可以选择安装jdk的位置

![1669558308618](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669558308618.png)

安装成功

![1669558682565](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669558682565.png)

4.*配置环境变量*

找到环境变量，新建系统变量JAVA_HOME 值为jdk安装路径![1669558973490](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669558973490.png)![1669559110324](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669559110324.png)

   然后配置Path变量，添加%JAVA_HOME%\bin和%JAVA_HOME%\jre\bin      (%%表示引用路径)

![1669559456590](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669559456590.png)

![1669559509383](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669559509383.png)

   点击确定

5.测试jdk是否安装成功

在终端中输入java -version命令即可

 ![1669559571532](C:\Users\ZSY\AppData\Roaming\Typora\typora-user-images\1669559571532.png)  



## 输出Hello,World！

1.创建一个java类型的文件-hello.java，文件类型是java类型

2.右键编辑文件在文件中输入代码:

```java
public class hello {
    public static void main(String[] args){
        System.out.println("hello world");
    }
}
```

3.打开cmd终端，cd到该文件目录下面，使用javac hello编译文件。此时会在此目录下生成一个hello.class的文件

4.使用java hello 代码运行文件

5.显示输出结果-hello world





## JAVA运行机制

源文件(java文件)-java编译器-字节码(class文件)-类装载器-字节码校验器-解释器-操作系统平台