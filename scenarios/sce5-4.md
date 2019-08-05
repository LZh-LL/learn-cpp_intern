## 参考答案

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下为供以参考的示例解析：

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
首先来看它的输出：

```r
Doing it right:
quiz 0 is a 20
quiz 1 is a 20
quiz 2 is a 20
quiz 3 is a 20
quiz 4 is a 20
Doing it dangerously wrong:
quiz 0 is a 20
quiz 1 is a 20
quiz 2 is a 20
quiz 3 is a 20
quiz 4 is a 20
quiz 5 is a 20
quiz 6 is a 20
quiz 7 is a 20
quiz 8 is a 20
quiz 9 is a 20
quiz 10 is a 20
quiz 11 is a 20
quiz 12 is a 20
quiz 13 is a 20
...
```

可以看到第二个错误循环到了数组末尾还不停止，且每个数组元素均为20。
产生这个错误的原因是测试表达式——**quizscores[i] = 20**。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
我们来看它做了什么，它将一个非零值（20）赋给了数组元素，故此表达式一直为非零，所以始终能进入循环，造成超出数组的输出；并且，它还修改了数组元素的数据，所以每个输出都是20。
而多出来的20一个一个被放入内存中，甚至可能导致其它应用程序无法运行。


