## 程序示例

### 简单应用：阶乘

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下是一个for循环的简单应用：

```r
#include <iostream>
const int ArSize = 16;
int main()
{
	long long factorials[ArSize];
	factorials[1] = factorials[0] = 1LL;
	for (int i = 2; i < ArSize; i++)
		factorials[i] = i * factorials[i-1];
	for (int i = 0; i < ArSize; i++)
		std::cout << i << "! = " << factorials[i] << std::endl;
	return 0;
}
```

对应的输出：

```r
0! = 1
1! = 1
2! = 2
3! = 6
4! = 24
5! = 120
6! = 720
7! = 5040
8! = 40320
9! = 362880
10! = 3628800
11! = 39916800
12! = 479001600
13! = 6227020800
14! = 87178291200
15! = 1307674368000
```

### 修改步长

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
可以看到前面的update-expression都是i++，即每次自加1，事实上关于步长我们可以有更改：

```r
#include <iostream>
int main()
{
	using std::cout;
	using std::cin;
	using std:: endl;
	
	cout << "Enter an integer: ";
	int by;
	cin >> by;
	cout << "Counting by " << by << "s:\n";
	for (int i=0; i < 100; i = i + by)
		cout << i << endl;
	return 0;
}
```

对应的输出：

```r
Enter an integer: 17		#17-input#
Counting by 17s:
0
17
34
51
68
85
```

### 关于++和--

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
++为递增运算符，--为递减运算符。但我们讨论的重点是他们出现的位置，其作为前缀或后缀可有这两种形式：

1. ++x
2. x++

对于x的值来说，最终都是自加了1，但是影响的时间上是不同的。就像我们去吃饭，吃完前支付还是吃完后结账的区别。以下示例你将更具体看到这种差异：

```r
#include <iostream>
int main()
{
	using std::cout;
	int a = 20;
	int b = 20;
	cout << "a    = " << a << ":    b = " << b << "\n";
	cout << "a++  = " << a++ << ":    ++b = " << ++b << "\n";
	cout << "a    = " << a << ":    b = " << b << "\n";
	return 0;
}
```

对应的输出：
```r
a    = 20:    b = 20
a++  = 20:  ++b = 21
a    = 21:    b = 21
```

对于上述程序的输出结果的解释是，a++是用当前值计算表达式（即相当于先使用a，再a=a+1；），然后再将a加1；b++则是先将b加1，这时新的b用于计算表达式（即先b=b+1，再使用b）。



