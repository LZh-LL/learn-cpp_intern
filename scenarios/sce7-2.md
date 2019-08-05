## 程序示例

1.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下是一个囊括函数定义、原型、调用三步的典型示例：

```r
#include <iostream>
void simple();

int main()
{
	using namespace std;
	cout << "main() will call the simple() function:\n";
	simple();
	
	cout << "main() is finished with the simple() function.\n";
	return 0;
}

void simple()
{
	using namespace std;
	cout << "I'm but a simple function.\n";
}
```

对应的输出：

```r
main() will call the simple() function:
I'm but a simple function.
main() is finished with the simple() function.
```

2. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下是一个关于函数原型和调用的典型示例：

```r
#include <iostream>
void cheers(int);			//原型：无返回值
double cube(double x);		//原型：返回一个double型
int main()
{
	using namespace std;
	cheers(5);				//函数调用
	cout << "Give me a number: ";
	double side;
	cin >> side;
	double volume = cube(side);		//函数调用
	cout << "A " << side << "-foot cube has a volume of ";
	cout << volume << " cubic feet.\n";
	cheers(cube(2));
	return 0;
}

void cheers(int n)
{
	using namespace std;
	for (int i = 0; i < n; i++)
		cout << "Cheers! ";
	cout << endl;
}

double cube(double x)
{
	return x * x * x;
}
```

对应的输出：

```r
Cheers! Cheers! Cheers! Cheers! Cheers!
Give me a number: 5			#5-input#
A 5-foot cube has a volume of 125 cubic feet.
Cheers! Cheers! Cheers! Cheers! Cheers! Cheers! Cheers! Cheers!
```

3. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下是一个接受两个参数的函数的典型示例：

```r
#include <iostream>
using namespace std;
void n_chars(char, int);
int main()
{
	int times;
	char ch;
	
	cout << "Enter a character: ";
	cin >> ch;
	while (ch != 'q')
	{
		cout << "Enter an integer: ";
		cin >> times;
		n_chars(ch, times);
		cout << "\nEnter another character or press the"
				" q-key to quit: ";
		cin >> ch;
	}
	
	cout << "The value of times is " << times << ".\n";
	cout << "Bye\n";
	return 0;
}

void n_chars(char c, int n)
{
	while (n-- > 0)
		cout << c;
}
```

对应的输出：

```r
Enter a character: W		#W-input#
Enter an integer: 50 		#50-input#
WWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWW
Enter another character or press the q-key to quit: a		#a-input#
Enter an integer: 20		#20-input#
aaaaaaaaaaaaaaaaaaaa
Enter another character or press the q-key to quit: q		#q-input#
The value of times is 20.
Bye
```












