## 知识概要

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
在sec0中我们提到过C++的特性之一——OOP（面向对象编程），Stephen Prata书中总结了一点：

>面向对象编程（OOP）的本质是设计并扩展自己的数据类型，设计自己的数据类型就是让类型与数据匹配。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
在创建自己的类型前，我们首先要理解C++**内置的类型**，因为它们是创建自己数据类型的基本组件。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
本章节要介绍的内置C++类型为**基本类型——整数和浮点数**（复合类型将在后面的课程讲解），那么产生了一个问题：存储的数据我们怎么使用？
对应这个问题，程序还需要引进一种存储数据的标识，也就是我们章节标题的另一个主角——变量。

### 变量
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
变量实质上是一种用来标识信息的方法，给出一个简单的变量声明：

```r
int var;
var=5;
```

其中的int是一种类型，var是变量名，因此var能表示一个整数的值，第二个语句表明存储了一个整数5，我们不需要管它存在哪块内存，我们只需要使用var来进行其它工作（比如算术运算）。
但是，在没有第二个赋值语句时，我们不知道var里存了什么（ps：根据全局/局部，动态/静态等的不同，不同的编译器处理方式可能不同，有的会默认为0，有的直接报错，所以无论什么变量，最好进行初始化操作）

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
值得一提的是一些变量的命名规则：
* 变量名只能包含三种符号：字母、数字和下划线（_）
* 变量名首字符不能是数字
* C++中变量名区分字母大小写
* C++中不能用关键字作为变量名
* 以两个下划线或下划线和大写字母打头的名称被保留实现（编译器及其使用的资源）使用
* 以一个下划线开头的名称被保留给实现，用作全局标识符
* C++中对于名称的长度没有限制，名称中所有的字符都有意义，但是有些IDE会有长度限制

除了遵循基本的命名规则外，我们可以有自己命名风格，但记住：**一致性和精度是最重要的**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
最后我们可以运用整型变量做个简单的算术运算：

```r
int a=0,b=1,c=2,d=3,e=4;
a=b-c+d*e;
cout<<a<<endl;
```

试试看，会打印出什么结果。


### 类型
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
在变量中我们提到过基本类型之一——整数，还有一大基本类型是浮点数。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
首先简要罗列下部分内置类型：
* 基本整型，按宽度递增依次为char,short,int,long,long long（C++11新增），每种类型又包括signed和unsigned版本，因此共十种
* 浮点数，常定义使用float和double
* 布尔型，true和false，取值分别为整数1和0
* 空类型，void
* 宽字符类型，wchar_t，实际也是一种整数类型

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
除了上述初学者常用的内置类型外，以后我们会接触的类型如下：
1. 结构-struct
2. 类-class
3. 定义别名-typedef
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
其主要作用是为现有类型创建新名称，例如：

```r
typedef int counter;
counter tick_c = 100;
```

tick_c实际上是一个整型变量。

4. 枚举类型-enum
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
一般形式：

```r
enum enum-name { list of name} var-list; 
```

其中，eunm-name指的是这个数据类型的名称；list of name是枚举量；var-list是enum-name类型的变量列表。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
举例：

```r
enum colour {red, green, blue} a_colour, another_colour;
a_colour = green; //a_colour will be assigned value of '1'
```

上述代码定义了一种枚举，其名字为colour，由于默认情况下编译器设置第一个枚举量为0，下一个为1，
故red=0，green=1，blue=2。其实到了这一步（enum colour {red, green, blue}）还只是定义了一个数据类型，
定义变量还需要有enum a_colour，上述代码在定义数据类型的同时定义了a_colour和another_colour两个变量，
且将a_colour赋了green。**(ps:“//”后接的是注释，多行注释采用/*注释内容*/的方式)**









