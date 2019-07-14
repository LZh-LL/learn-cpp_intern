## 程序示例

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
以打印"Hello,World!"为例，结合之前在sec0-关于本课程中的Terminal部分，我们以此进行以下操作：
1. 打开Terminal，并更改输入方式
2. 在桌面创建文件夹cc：
```r
mkdir cc
```
进入cc：
```r
cd cc
```
创建并编辑hello.cpp文件：
```r
vi hello.cpp
```
3. 摁**”i“**键进入编辑模式，并输入以下代码：
```r
#include<iostream>
using namespace std;
int main(){
	cout<<"Hello,World!"<<endl;
	return 0;
}
```
4. 摁**”ESC“键**退出编辑，再摁**”shift“键**+**”:“键**，输入**wq**，保存修改
5. 使用g++编译器进行编译，输入以下指令：
```r
g++ hello.cpp
```
输入指令：
```r
ls
```
可以看到生成了一个a.out，即之前所说的可执行文件。
6. 执行a.out，输入以下指令：
```r
./a.out
```
其打印结果如下图所示：<br/>
	! [sce1-op1](/images/sce1-op1.png)<br/>
