---
title: POJ3268 Silver Cow Party
date: 2016-11-27 12:38:52
tags: [Dijkstra, POJ]
categories: algorithm
---
## 带有反向图的Dijkstra
>题目描述
>[POJ3268 Silver Cow Party](http://poj.org/problem?id=3268)

知识点:
1. 求*其他cow*到*目标cow*， 再返回原本所在位置的本质： 正向求**目标cow到其他cow**的距离 加 **反向图**后**目标cow到其他cow**的距离
2. 反向图时，关于*对角线对称*的操作， 第二个for循环开始 **j = i**， 否则一个点被**倒置两次**，又**回到**了**开始**状态。
3. isVisit数组中的*要求的点partyPlace*， **在开始dijkstra前设置为true**

我的代码: [github](https://github.com/ZhaoQiling/Algorithm/blob/master/POJ/3268.cpp)