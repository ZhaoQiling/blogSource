---
title: STLPart1
date: 2017-2-19 15:15:41
tags:
categories: CPP
---
## stringstream及其用法
> 包含在头文件 sstream 中

1. 声明stringstream
```C++
stringstream ss;
```
2. 给stringstream对象赋值
```C++
//可以在定义时赋值
string s;
cin >> s;
stirngstream ss(s);
//利用stringstream::str()进行赋值
stringstream ss;
ss.str("hello stringstream");
//利用流
string s;
stringstream ss;
cin >> s;
ss <<　ｓ;
```
3. stringstream的清空
```
stringstream ss;
ss.str("");//right
ss.clear; //error
```

## std::lower_bound()和std::lower_bound()

>ForwardIter lower_bound(ForwardIter first, ForwardIter last,const _Tp& val)算法返回一个非递减序列[first, last)中的第一个**大于等于**值val的位置。
>ForwardIter upper_bound(ForwardIter first, ForwardIter last, const _Tp& val)算法返回一个非递减序列[first, last)中第一个**大于**val的位置。

|1 |2 | 2|3 |4 | 4|4 |5 |6 |7 |9 |9|10|&nbsp;|
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
|first|&nbsp;|&nbsp;|&nbsp;|lower_bound(first, last, 4)|&nbsp;|&nbsp;|&nbsp;|upper_bound(first, last, 4)|&nbsp;|&nbsp;|&nbsp;|&nbsp;|last|

```C++
//查找相应的值的位置
int loc = lower_bound(first, last, 4) - first;
```
## 不定长数组： vector()

若a是一个vector，可以用a.size( )读取它的大小，a.resize( )改变大小，a.push_back( )向尾部添加元素，a.pop_back( )删除最后一个元素

## set()用法
