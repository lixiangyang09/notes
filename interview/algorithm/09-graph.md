# 图

## 图的表示

表示图的三种方法

1. 边的列表 O(E)

```
 [ [0,1], [0,6], [0,8], [1,4], [1,6], [1,9], [2,4], [2,6], [3,4], [3,5], [3,8], [4,5], [4,9], [7,8], [7,9] ]
```

2. 临接矩阵 O(V^2) 

```
    [ [0, 1, 0, 0, 0, 0, 1, 0, 1, 0],
    [1, 0, 0, 0, 1, 0, 1, 0, 0, 1],
    [0, 0, 0, 0, 1, 0, 1, 0, 0, 0],
    [0, 0, 0, 0, 1, 1, 0, 0, 1, 0],
    [0, 1, 1, 1, 0, 1, 0, 0, 0, 1],
    [0, 0, 0, 1, 1, 0, 0, 0, 0, 0],
    [1, 1, 1, 0, 0, 0, 0, 0, 0, 0],
    [0, 0, 0, 0, 0, 0, 0, 0, 1, 1],
    [1, 0, 0, 1, 0, 0, 0, 1, 0, 0],
    [0, 1, 0, 0, 1, 0, 0, 1, 0, 0] ]
```


3. 临接表 


```
[ [1, 6, 8],
  [0, 4, 6, 9],
  [4, 6],
  [4, 5, 8],
  [1, 2, 3, 5, 9],
  [3, 4],
  [0, 1, 2],
  [8, 9],
  [0, 3, 7],
  [1, 4, 7] ]
```

鉴于现实世界中，图一般是稀疏的，我们可以认为邻接表是图的标准表示形式。有些算法可能需要使用

## 四个基础算法

深度优先和广度优先遍历和树的遍历完全一样，只需要多一个 visited set 用于保存访问过的节点就可以了。

### Floyd-Warshall 多源最短路径算法

如果要让任意两点（例如从顶点 a 点到顶点 b）之间的路程变短，只能引入第三个点（顶点 k），并通过这个顶点 k 中转即 a->k->b，才可能缩短原来从顶点 a 点到顶点 b 的路程。当然也不止一个点，可能是很多个点，也就是说每个顶点都有可能使得另外两个顶点之间的路程变短。

- Floyd-Warshall 求的是任意两点之间的最短距离
- 不能处理负边
- 复杂度 O(N^3)
- 使用了动态规划的思想

### Dijkstra 单源最短路径算法

### 最小生成树

寻路算法

Dijkstra

A*


https://www.cnblogs.com/aiyelinglong/archive/2012/03/26/2418707.html

## BFS

什么时候需要用广度优先搜索？距离问题、连通问题、求最短路径

图的广度优先搜索需要有一个 visited set，记录哪些节点已经走过了。


如何求最长路径呢？

    

## 参考资料

1. [Union-Find 并查集算法详解](https://mp.weixin.qq.com/s?__biz=MzAxODQxMDM0Mw==&mid=2247484751&idx=1&sn=a873c1f51d601bac17f5078c408cc3f6)
2. https://www.khanacademy.org/computing/computer-science/algorithms/graph-representation/a/representing-graphs