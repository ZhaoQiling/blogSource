---
title: 再解炸弹人
date: 2016-11-09 10:32:29
tags: [BFS,aha]
categories: algorithm
---
## 简单的BFS搜索
>题目描述
>[再解炸弹人](http://www.tianchai.org/problem-12034.html)

心得：
1. 利用一个结构体数组，对每个点进行出入队列操作
2. 编写getNum时, 按照向**四个**不同方向扩展的思路，而不是*两条*交叉的直线
3. 对每个head点的*四个方向*进行扩展，并且**先判断**是否可以加入队列，**然后再**加入队列
4. 每有一个点加入队列后便**tail++**每判断四个点后便**head++**
5. 在对startX 和 startY 进行**加入第一个节点**操作时，虽然head 和 tail都可以进行相同的操作，但是**入队操作需要使用tail**

我的代码: [github](https://github.com/ZhaoQiling/Algorithm/blob/master/%E5%95%8A%E5%93%88%E7%AE%97%E6%B3%95/%E5%86%8D%E8%A7%A3%E7%82%B8%E5%BC%B9%E4%BA%BA.cpp)