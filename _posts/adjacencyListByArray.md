---
title: 邻接表的数组实现
date: 2016-11-23 09:23:24
tags: [aha]
categories: algorithm
---
### 书没有博客详细系列
> [啊哈磊的博客园](http://www.cnblogs.com/ahalei/p/3651334.html)

比较难以理解的部分
1. 利用**i给各个边编号**。
2. first存储了每个*点*第一条**边**的序号(i)
3. next存储第i*边*的下一条**边**的序号(i)
4. 因为是*有向图*，每条边**只能**在一个邻接表中

```
#include <iostream>
using namespace std;
int main()
{
    int nPoint, nSide;
    cin >> nPoint >> nSide;
    int u[10], v[10], w[10];
    int first[10], next[10];
    for(int i = 1; i <= nPoint; i++)
    {
        first[i] = -1;
    }
    // i 是每条边的序号
    //first存储了每个点第一条 边的序号
    //next存储了第i边下一条边的序号
    //因为是有向图， 所以每一边的只可能是一个点的第一条边或者下一条边
    for(int i = 1; i <= nSide; i++)
    {
        cin >> u[i] >> v[i] >> w[i];
        next[i] = first[u[i]];
        first[u[i]] = i;
    }
    for(int i = 1; i <= nPoint; i++)
    {
        int k = first[i];
        while(k != -1)
        {
            cout << u[k] << v[k] << w[k] << endl;
            k = next[k];
        }
    }
    return 0;
}
```