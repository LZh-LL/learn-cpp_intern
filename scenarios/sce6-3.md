## 小试牛刀

### 问题描述

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
通过这两章节的学习，接下来尝试着解答一些问题：

* 简答题

1.

```r
入口条件循环和出口条件循环之间的区别是什么？各种C++循环分别属于其中的哪一种？
```

2. 如果下面的代码片段分别是有效程序的组成部分，则分别会打印什么内容？

```r
#①---------------------#
int i;
for (i = 0; i < 5; i++)
	cout << i;
	cout << endl;

#②---------------------#
int j;
for (j = 0; j < 11; j += 3)
	cout << j;
cout << endl << j << endl;

#③---------------------#
int j = 5;
while ( ++j < 9)
	cout << j++ << endl;

#④---------------------#
int k = 8;
do
	cout << " k = " << k << endl;
while (k++ < 5);

```

* 编程题

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
Daphne以10%的单利投资了100美元。也就是说，每一年的利润都是投资额的10%，即每年10美元：

```r
利息=0.10×原始存款
```

而Cleo以5%的复利投资了100美元。也就是说，利息是当前存款（包括获得的利息）的5%：

```r
利息=0.05×当前存款
```

Cleo在第一年投资100美元的盈利是5%——得到了105美元。下一年的盈利是105美元的5%——即5.25美元，依此类推。
请编写一个程序，计算多少年后，Cleo的投资价值才能超过Daphne的投资价值，并显示此时两个人的投资价值。

