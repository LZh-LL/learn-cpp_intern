## 第一个程序

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
我们的第一个程序分三部分来看。<br/>

### 编译指令
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
首先每个C++程序都会使用库，以此来执行必要的功能。<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
例如，本章节会使用到的头文件——**iostream**，定义了用于打印的**cout**。我们必须添加以下代码才能直接使用**cout**：
```r
#include <iostream>
using namespace std;
```

### 函数头和函数体
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
然后就是我们要编写代码的main函数：
```r
int main(){
	...
	our code goese here.
}
```
其中，第一行int main()叫函数头，花括号（{和}）中包括的部分叫函数体。

### 返回语句
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
我们做事要有头有尾，在main函数中的最后一条语句一般会是返回语句：
```r
return 0;
```
它的作用就是结束该函数。