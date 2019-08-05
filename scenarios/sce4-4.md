## 参考答案

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以下为供以参考的代码：

```r
#include <iostream>
int main()
{
	using namespace std;
	char fname[30];
	char lname[30];
	char grade;
	int age;
	
	cout << "What is your first name? ";
	cin >> fname;
	
	cout << "What is your last name? ";
	cin >> lname;
	
	cout << "What letter grade do you deserve? ";
	cin >> grade;
	
	cout << "What is your age? ";
	cin >> age;
	
	cout << "Name: " << lname << ", " << fname << endl;
	cout << "Grade: " << ++grade << endl;
	cout << "Age: " << age << endl;
	
	return 0;
}
```

