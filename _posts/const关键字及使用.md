---
title: const关键字及使用
date: 2017-02-11 11:26:39
tags:
categories: CPP
---
## 定义常量
* const int MAX_VAL = 23;
* const string SCHOOL_NAME = "QDU";

## 定义常量指针
>不可通过常量指针修改其所指向的内容

```
int n, m;
const int *p = &n;
*p = 5;//error
n = 4; // ok
p = &m; //ok
//常量指针可通过强制类型转化 转化为非常量指针
int * p1 = (int *)p;//ok
```

## 定义常应用
```
int n;
const int &r = n;
r = 5;
n = 4;
```