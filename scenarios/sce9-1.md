## 知识概要

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
前面介绍过函数的相关内容，本章节将介绍它的一个特点——调用自己，这种功能称为递归。
（ps：C语言中main()函数可以调用自己，但C++中不行）

### 递归条件

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
构成递归需要具备一些条件：

1. 子问题与原始问题做同样的工作，且分化得更简单
2. 代码中包含终止调用链的内容

关于第二点，通常的方法是将递归调用放在if语句中，例如，void类型的递归函数recurs()如下：

```r
void recurs(argumentlist)
{
	statements1
	it (test)
		recurs(arguments)
	statements2
}
```

不妨思考下，它的执行顺序。

