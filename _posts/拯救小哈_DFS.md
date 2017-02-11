---
title: 解救小哈
date: 2016-11-07 13:42:43
tags: [DFS,aha]
categories: algorithm
---
## 简单的dfs搜索
***
>题目描述：
> [添柴，拯救小哈](http://www.tianchai.org/problem-12032.html)

	一道比较水的DFS搜索题目，需要注意的是
1. 运用next数组进行下一步的加减，与八皇后问题可以*斜着走*的问题区别开，只能上下左右运动的需要定义一个next[4][2]的数组进行保存。
2. 编写DFS只关心当前这一步要做什么，并且注意边界条件的判断，如此题的是否出界和是否有障碍物
3. 标记数组的处理，为了防止死递归，所以需要标记数组，而下一步的决策取决于上面的标记，但是不能影响其他平行的决策，所以标记数组要**及时**复原。
我的代码： [github](https://github.com/ZhaoQiling/Algorithm/blob/master/%E5%95%8A%E5%93%88%E7%AE%97%E6%B3%95/%E8%A7%A3%E6%95%91%E5%B0%8F%E5%93%88.cpp)