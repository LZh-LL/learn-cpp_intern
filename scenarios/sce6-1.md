## 知识概要

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
之前我们学过for循环，这一章节我们来了解具有同样功能的while循环。

### while循环的组成

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
while循环可以看作没有初始化和更新部分的for循环，其一般形式如下：

```r
while (test-condition)
		bofy
```

和for循环一样，while循环也是一个入口条件循环。假设测试条件一开始便是false，则程序直接跳过循环体。假设为为真，则执行循环体的语句（一条语句或由花括号定义的语句块），然后返回测试条件重新判断，直到该测试条件为false为止。

### while循环与for循环的转换

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
C++中while循环和for循环本质上是一样的，可以进行相互转换，例如以下的for循环：

```r
for (init-expression; test-expression; update-expression)
{
	statement(s)
}
```

可改写成：

```r
init-expression;
while (test-expression)
{
	statement(s);
	update-expression;
}
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
同样地，例如以下的while循环：

```r
while (test-expression)
	body
```

可改写成：

```r
for ( ; test-expression; )
	body
```

语法规定for循环需要三个表达式，不过可以为空语句，但两个分号是必需的。而测试表达式省略时，此处默认为true，除非循环体中有类似于break或return的语句，否则循环将一直运行下去。

### 循环设计原则

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
主要有以下几条指导原则：

* 指定循环终止的条件
* 首次测试前初始化条件
* 条件被再次测试前更新条件

### do while循环

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
这里提一下do while循环，与前述的for循环和while循环不同，它是一种出口条件循环，也就是说会先执行循环体，再判定测试表达式。
其句法如下：

```r
do
	body
while (test-expression)
```


