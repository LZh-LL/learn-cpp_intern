## 程序示例

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
来看一个关于递归执行的典型示例：

```r
#include <iostream>
void countdown(int n);

int main()
{
	countdown(4);
	return 0;
}

void countdown(int n)
{
	using namespace std;
	cout << "Counting down ... " << n << endl;
	if (n > 0)
		countdown(n-1);
	cout << n << ": Kaboom!\n";
}
```

对应的输出：

```r
Counting down ... 4
Counting down ... 3
Counting down ... 2
Counting down ... 1
Counting down ... 0
0: Kaboom!
1: Kaboom!
2: Kaboom!
3: Kaboom!
4: Kaboom!
```

从程序的输出可知前五句都是一层层往下，到第六句开始向上层回退。值得注意的是每个递归调用都创建自己的一套变量，所以每一个n都是独立的，你可以尝试下将每一个n的地址也输出来。










