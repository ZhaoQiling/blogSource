---
title: POJ3278 Catch That Cow
date: 2016-11-09 14:06:14
tags: [BFS,POJ]
categories: algorithm
---
## BFS搜索
>题目描述
>[POJ3278 Catch That Cow](http://poj.org/problem?id=3278)

遇到的坑：
1. 统计步数的BFS题，建一个**结构体数组**，其中的step统计*步数*
2. 每走一步的步数，新的节点的步数，一定是**head节点的步数 +1 ！！**！,切记不是自己的步数自增1， 被这个坑了好长时间
3. 尝试三种不同方式可以使用*一个for循环嵌套三个if*
4. **巨坑0**: 考虑 开始时 农夫和牛在同一位置的情况
5. **巨坑1**：在poj上数组不能开到100000， 也不能开到100001要不会报错， 考虑了半天改成了100010，AC。

我的代码: [github](https://github.com/ZhaoQiling/Algorithm/blob/master/POJ/3278.cpp)