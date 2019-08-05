## 知识概要

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
前面我们提到过数组和字符串，如果要将一个数组进行累加，或者将一个字符串重复打印多次时，这种重复的操作就涉及到了循环。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
本章节将带大家了解一下for循环。

### for循环的组成

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nb  sp;&nbsp;
先看一个示例：

```r
for (i =0 ; i < 5 ; i++)
	cout << " C++ knows loops.\n"
```

上面就是一个简单的for循环语句（ps：C++将整个for看作一条语句，尽管循环体可包含多条语句），
故其结构一般形式如下：

```r
for (initialization; test-expression; update-expression)
	body
```

结合for循环的步骤来看，首先我们通常要对变量进行初始化（initialization），用该变量计算循环周期（可以初始化多个，在循环体内其它用途）；然后关于test-expression，这是循环测试，我们要知道for循环是一种入口条件循环，即每轮循环前都要计算测试表达式的值，比如上面的示例中i<5，因为i初始化为0，故一开始可以进入循环体，但是打印5次后，i自加到5，便不再满足循环测试，故跳出循环，不再执行循环体；
然后是update-expression——更新表达式，每轮循环结束时执行，通常用来对跟踪循环轮次的变量值进行增减，可以是有效的C++表达式或其它控制表达式。最后是body——循环体，是你需要重复进行的操作。

ps：for循环中申请的变量只存在于for语句中（即initializ中使用声明语句表达式产生的变量），当程序离开循环后，这种变量将消失。


