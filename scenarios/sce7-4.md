## 参考答案

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下为供以参考的答案：

1. 

```r
使用函数的3个步骤：
① 提供函数定义
② 提供函数原型
③ 调用函数
```

2. 

```r
#include <iostream>
using namespace std;
double Average(double,double);

int main()
{
	double a, b, average;
	
	cout<<"Please enter two number:\n";
	while (cin >> a >> b && a != 0 && b != 0)
	{
		average = Average(a, b);
		cout << "Harmonic average: " << average << endl;
		cout << "Please enter two number:\n";
		continue;
	}
	cout << "Bye!!";
	
	return 0;
}

double Average(double a,double b)
{
	double average;
	average = 2 * a * b/(a + b);
	return average;
}
```
