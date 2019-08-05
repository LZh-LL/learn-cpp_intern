## 小试牛刀

### 问题描述

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下程序试图检查一个存储了测验成绩的数组，在遇到第一个不为20的成绩时停止，但在使用循环时存在一个错误，另外还有一个重大的设计错误，请找到这些错误，并分析如何修复。
代码如下：

```r
#include <iostream>
int main()
{
	using namespace std;
	int quizscores[10] = 
		{ 20, 20, 20, 20, 20, 19, 20, 18, 20, 20};
	
	cout << "Doing it right:\n";
	int i;
	for (i = 0; quizscores[i] == 20; i++)
		cout << "quiz " << i << " is a 20\n";
		
	cout << "Doing it dangerously wrong:\n";
	for (i = 0; quizscores[i] = 20; i++)
		cout << "quiz " << i << " is a 20\n";

	return 0;
}
```













