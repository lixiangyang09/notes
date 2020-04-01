这个文档用来加快你做题的速度，减少不必要的思考

## 变量名规范

统一使用：`ans`, `lo`, `hi`

## 如果有一个数为0，返回另一个

```py
if n * m == 0:
    return n + m
```

##  生成数组

```py
dp = [False for _ in range n]
dp = [False] * n
```

## deque

```py
from collections import deque
deque.append(x)  # 从后面添加
deque.appendleft(x)  # 从前面添加
deque.clear()
deque.insert(i, x)
deque.pop()
deque.popleft()
```


## 生成 m*n 的空矩阵

常用在二维 DP 中

```py
d = [ [0] * m for _ in range(n)]
```

## 最大值，最小值

```py
max_num = float("inf")
min_num = float("-inf")
```

## 素数筛子

```py
```

## Python 的优缺点

内置 queue，内置 Counter

- 没有 TreeMap，也就是内置的二叉查找树
- 没有 Linkedlist
- 对于字符串来说，实际上 Python 是由 internization 的，所以可能不需要 hash 函数。                   