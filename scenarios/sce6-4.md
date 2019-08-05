## 参考答案

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下为供以参考的答案：

* 简答题

1. 

```r
①入口条件循环和出口条件循环的主要区别在于：入口条件循环在执行循环体前先检查循环条件；出口条件循环是在执行循环体的语句之后检查循环条件。
②for循环和while循环都是入口条件循环，do while循环为出口条件循环。
```

2. 

```r
#①---------------------#
01234

#②---------------------#
0369
12

#③---------------------#
6
8

#④---------------------#
k=8

```

* 编程题

```r
#include <iostream>
int main()
{
	using namespace std;
	double Daphne = 100.0;
	double Cleo = 100.0;
	int years;
	
	for (years = 1; Daphne >= Cleo; years++)
	{
		Daphne = Daphne + 0.10 * 100.0;
		Cleo = Cleo * 1.05;
	}
	
	cout << "经过" << years << "年后，Cleo的投资价值才能超过Daphne的投资价值" << endl;
	cout << "此时Daphne的投资价值为：" << Daphne << endl;
	cout << "此时Cleo的投资价值为：" << Cleo << endl;
	
	return 0;
}
```

