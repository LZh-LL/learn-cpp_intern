## 知识概要

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
本章节来讨论字符串，首先，我们要知道，C++处理字符串的方式有二：

1. C-风格字符串
2. 基于string类库

关于string类的部分我们放到后边的类中进行说明。

### 声明

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
C-风格字符串具有一个特殊性质：以空字符——\0结尾，也就是我们常说的尾零，其ASCII码为0，用以标记字符串的结尾。

声明方式如下：

1.
```r
char name[12] = { 'L', 'i', 'u', 'Z', 'h', 'u', 'h', 'u', 'a', 'n', 'g', '\0'};
```

2.
```r
char name[13] = "Liu Zhuhuang";
```

**ps：确定存储字符串所需要的最短数据时，别忘了将结尾的空字符计算在内**

### 区别字符串常量与字符常量

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
直观来看，字符串常量为双引号圈定，字符常量为单引号圈定。以'L'与"L"为例，后者实际上是S和\0两个字符串组合的字符串，所以字符常量是可以赋给char变量，但是字符串常量不行，不可以将一个内存地址赋给char常量。

下一步我们将通过一些文字或示例来熟悉以下要点：

* 字符串常量的拼接
* 字符串在数组中的运用
* 字符串输入


