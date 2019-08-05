## 小试牛刀

### 问题描述

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
请分析出以下代码的输出：

```r
#include <iostream>
double cube(double a);
double refcube(double &ra);
int main()
{
	usign namespace std;
	double x = 3.0;
	
	cout << cube(x);
	cout << " = cube of " << x << endl;
	cout << refcube(x);
	cout << " = cube of " << x << endl;
	return 0;
}

double cube(double a)
{
	a *= a * a;
	return a;
}

double refcube(double &ra)
{
	ra *= ra * ra;
	return ra;
}
```

