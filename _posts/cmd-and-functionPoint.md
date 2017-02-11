---
title: 函数指针和命令行参数
date: 2016-12-03 10:42:44
tags: [functionPointer,cmd]
categories: [CPP]
---
## 函数指针的声明

类型名 (* 指针变量名)(参数类型1, 参数类型2, ……)
```C++
int (*typeOfSort)(const void *elem1, const void *elem2);
```
## 可以通过**strcmp函数**比较输入的命令行， 来决定升序或降序排序
```C++
if(strcmp(argv[1], "as"))
    typeOfSort = ascending;
if(strcmp(argv[1], "ds"))
    typeOfSort = dscending;
```
## qosrt用 法： 
```C++
void qsort(void *base,int nelem,int width,int (*fcmp)(const void *,const void *));
```

参数： 

1. 待排序数组首地址
2. 数组中待排序元素数量
3. 各元素的占用空间大小
4. 指向函数的指针，用于确定排序的顺序

## typeOfSort所指向的函数类型需要程序员自己编写
1. 如果 *elem1 在 *elem2之**前**返回**负**整数
2. 如果 *elem1 在 *elem2之**后**返回**正**整数
3. 如果 *elem1 与 elem2的**顺序无所谓**，返回**0*

## 在比较具体数字之前需要将const int * 类型的指针转化为const int *类型
```C++
const int *value1 = (const int *)elem1;
```

## 命令行参数**以空格区分**不同命令，如果要输入带有空格的字符串如 Hello World 需使用**双引号括起**

argc: 代表启动程序时， 命令行参数的个数， C/C++规定， **可执行程序本身的文件名， 也算作一个命令行参数**， 因此， **argc的值至少是1**
argv： 指针数组， 其中每个元素都是一个char* 类型的指针， 每个指针指向一个字符串， 若命令行参数内部用空格， 用双引号括起来即可， 如下实例中的"hello world"
如果输入的字符中带有双引号的话： 123"456 就是 123"""456 "A""B" 就是 """A""""""B""" ， 带有百分号的话：%号转义就是两个百分比：%%
```
example：myprogram "hello world"
```
---
我的代码：[github](https://github.com/ZhaoQiling/CplusplusLearn/blob/master/courseraPKU/functionPointer_cmd.cpp)