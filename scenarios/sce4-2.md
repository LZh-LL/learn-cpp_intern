## 程序示例

### 字符串常量的拼接

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下是三条输出语句：

```r
cout << "I'd give my right arm to be" " a great violinist.\n";
cout << "I'd give my right arm to be a great violinist.\n";
cout << "I'd give my right ar"
"m to be a great violinist.\n";
```

以上三条输出语句等效，这是因为C++允许拼接字符串字面值，即两个用引号括起的字符串合并为一个，所以不管是空格还是制表符和换行符，分隔的字符串常量会自动拼接成一个。


### 字符串在数组中的运用

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下程序演示了将字符串存储到数组中的两种方法：

```r
#include <iostream>
#include <cstring>
int main()
{
	using namespace std;
	const int Size = 15;
	char name1[Size];
	char name2[Size] = "C++owboy";
	
	cout << "Howdy! I'm " << name2;
	cout << "! What's your name?\n";
	cin >> name1;
	cout << "Well, " << name1 << ", your name has ";
	cout << strlen(name1) << "letters and is stored\n";
	cout << "in an array of " << sizeof(name1) << " bytes.\n";
	cout << "Your initial is " << name1[0] << ".\n";
	name2[3] = '\0';
	cout << "Here are the first 3 characters of my name: ";
	cout << name2 << endl;
	return 0;
}
```

对应的输出：

```r
Howdy! I'm C++owboy! What's your name?
Basicman		#input#
Well, Basicman, your name has 8 letters an is stored
in an array of 15 bytes.
Your initial is B.
Here are the first 3 characters of my name: C++
```

这两种方法就是将数组初始化为字符串常量、将键盘或文件输入读入到数组中。
同时可以看到，示例程序中最后使用了\0截断了name2字符串，即便第5位及以后还有其它字符也不再输出。

### 字符串输入

1. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
事实上，在编写代码后测试的过程中，如果有多个输入，正好在输入第一个后，不小心把第二个值也输入了，这时候会发生什么？
下面这个示例展示了这种现象，之后我们来分析原因：

```r
#include <iostream>
#int main()
{
	using namespace std;
	const int ArSize = 20;
	char name[ArSize];
	char dessert[ArSize];
	
	cout << "Enter your name:\n";
	cin >> name;
	cout << "Enter your favorite dessert:\n";
	cin >> dessert;
	cout << "I have some delicious " << dessert;
	cout << " for you, " << name << ".\n";
	return 0;
}
```

对应的输入输出：

```r
Enter your name:
Alistair Dreeb		#input#
Enter your favorite dessert:
I have some delicious Dreeb for you, Alistair.
```

可以看到，当提示第一个输入时把第二个输入的也输入了，最后直接立即显示最后一行。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
这是因为cin使用空白（空格、制表符和换行符）来确定字符串的结束位置。在这个例子中，Dreeb留在了输入队列中，cin在输入队列搜索用户喜欢的甜点时发现Dreeb便直接读取。

2.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
再来一个关于行读取的例子：

```r
#include <iostream>
int main()
{
	using namespace std;
	const int ArSize = 20;
	char name[ArSize];
	char dessert[ArSize];
	
	cout << "Enter your name:\n";
	cin.getline(name, ArSize);
	cout << "Enter your favorite dessert:\n";
	cin.getline(dessert, ArSize);
	cout << "I have some delicious " << dessert;
	cout << " for you, " << name << ".\n";
	return 0;
}
```

对应的输出：
```r
Enter your name:
Dirk Hammernose		#input#
Enter your favorite dessert:
Radish Torte		#input#
I have some delicious Radish Torte for you, Dirk Hammernose.
```

getline()函数每次读取一行，通过换行符确定行尾，但是存储时会替换成空字符

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
和它类似的有一个get()函数，它不会将换行符丢弃，而是留在输入队列中，因此如果要连续调用两次get来读取，第二次是读取不到的，如果想要读取到，有以下两种方式：

```r
cin.get(name, ArSize);
cin.get();
cin.get(dessert, ArSize);
```
或
```r
cin.get(name, ArSize).get();
```

3.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
最后来看一个由于getline()或get()函数读取空行产生问题的例子：

```r
#include <iostream>
int main()
{
	using namespace std;
	cout << "What year was your house built?\n";
	int year;
	cin >> year;
	cout << "What is its street address?\n";
	char address[80];
	cin.getline(address, 80);
	cout << "Year built: " << year << endl;
	cout << "Address: " << address << endl;
	cout << "Done!\n";
	return 0;
}
```

对应的输出是什么样子呢？我们来看看：

```r
What year was your house built?
1966		#input#
What is its street address?
Year built: 1966
Address
Done!
```

可以看到用户没有输入地址的机会,这是由于上一个例子中提到的换行符产生的问题，cin读取年份后会将换行符留在输入队列。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
这个换行符被cin.getline()认为是一个空行，从而给address数组赋一个空字符。
解决的方法第2个示例其实已经给出了：

```r
cin >> year;
cin.get();
```
或
```r
(cin >> year).get();
```



