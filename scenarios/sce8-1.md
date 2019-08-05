## 知识概要

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
前面的sce7提到过，函数本来不改变传进去的参数，除非用指针，本章节将提到另一种方式——引用。

### 引用的定义和使用

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
通过前面的学习，我们知道C++使用&来指示变量的地址，但其实它还有另一个含义——用来声明引用。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
例如：

```r
int name1;
int & name2 = name1;
```

这里int &是指向int的引用，我们将在示例1中更深入了解&的两种含义。

同时，引用还有两点需要注意：
1. 必须在声明引用时将其初始化，而不能先声明，再赋值
2. 创建引用时进行初始化，一旦与某个变量关联，就一直只与它关联。

### 引用作为函数参数

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
在C中只能按值传递，C++能够按引用传递参数。

这种方式允许被调用的函数去访问调用函数中的变量。比如说我们要利用函数交换两个变量的值，那么这就要求必须能修改调用程序中的变量值。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
按值传递变量将不管用了，必须使用引用或指针。示例2中将演示这三张方法。

