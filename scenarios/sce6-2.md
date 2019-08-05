## 程序示例

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下是一个关于while循环的典型示例：

```r
#include <iostream>
const int ArSize = 20;
int main()
{
	using namespace std;
	char name[ArSize];
	cout << "Your first name. please: ";
	cin >> name;
	cout << "Here is your name, verticalized and ASCIIized:\n";
	int i = 0;
	while (name[i] != '\0')
	{
		cout << name[i] << ": " << int(name[i]) << endl;
		i++;
	}
	return 0;
}	
```

对应的输出：

```r
Your first name, please: Muffy		#Muffy-input#
Here is your name, verticalized and ASCIIized:
M: 77
u: 117
f: 102
f: 102
y: 121
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下是一个关于do while循环的典型示例：

```r
#include <iostream>
int main()
{
	using namespace std;
	int n;
	
	cout << "Enter numbers in the range 1-10 to find ";
	cout << "my favorite number\n";
	do
	{
		cin >> n;
	}while (n !=7);
	cout << "Yes, 7 is my favorite.\n";
	return 0;
}
```

对应的输出：

```r
Enter numbers in the range 1-10 to find my favorite number
9		#input#
4		#input#
7		#input#
Yes, 7 is my favorite.
```



















