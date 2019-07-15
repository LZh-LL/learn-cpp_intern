## 程序示例

### 整型
1. 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下是一个关于检查整型长度的典型示例：
```r
// limits.cpp -- some integer limits
#include <iostream>
#include <climits>				// use limits.h for older systems
int main()
{
	using namespace std;
	int n_int = INT_MAX;			// initialize n_int to max int value
	short n_short = SHRT_MAX;		// symbols defined in climits file
	long n_long = LONG_MAX;
	long long n_llong = LLONG_MAX;
	
	// sizeof operator yields size of type or of variable
	cout << "int is " << sizeof (int) << " bytes." << endl;
	cout << "short is " << sizeof n_short << " bytes." << endl;
	cout << "long is " << sizeof n_long << "bytes." << endl;
	cout << "long long is " << sizeof n_llong << "bytes." <<endl;
	cout << endl;
	
	cout << "Maximum values:" << endl;
	cout << "int: " << n_int << endl;
	cout << "short: " << n_short << endl;
	cout << "long: " << n_long << endl;
	cout << "long long: " << n_llong << endl << endl;
	
	cout << "Minimum int value = " << INT_MIN << endl;
	cout << "Bits per byte = " << CHAT_BIT << endl;
	return 0;
}
```
对应的输出（64为Windows7系统）：
```r
int is 4 bytes.
short is 2 bytes.
long is 4 bytes.
long long is 8 bytes.

Maximum values:
int: 2147483647
short: 32767
long: 2147483647
long long: 9223372036854775807

Minimum int value = -2147483648
Bits per byte = 8
```
不妨思考一个问题：超越了这些限制，变量将会如何取值？（ps:C++不保证符号整型上溢和下溢时不出错）


2.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
不同于存储数字，存储字母需要使用字母的数值编码，
以下是一个关于char型及ASCII码的经典程序：
```r
// morechar.cpp -- the char type and int type contrasted
#include <iostream>
int main()
{
	using namespace std;
	char ch = 'M';				// assign ASCII code for M to ch
	int i = ch;					// store
	cout << "The ASCII code for " << ch << "is " << i << endl;
	
	cout << "Add one to the character code: " << endl;
	ch = ch + 1;				// change character code in cd
	i = ch;						// save new character code in in
	cout << "The ASCII code for " << ch << "is " << i << endl;
	
	// using the cout.put() member function to display a char
	cout << "Displaying char ch using cout.put(ch): ";
	cout.put(ch);
	
	// using cout.put() to display a char constant
	cout.put('!');
	cout << endl << "Done"
}
```












