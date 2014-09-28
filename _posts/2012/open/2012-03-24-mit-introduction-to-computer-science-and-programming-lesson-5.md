---
layout: post
title: 麻省理工《计算机科学及编程导论》第五课
category: open
---
##浮点数和逐次近似

Python与其他语言不同，它有一种“任意精度整数”。也就是说，你想让它有多大，它就能有多大（小数则不行，最多精确到17位）。例如2的1000次方：

```python
2 ** 1000
```

二分法的基本思路：所有可能的答案构成一个线性排列的空间。若在某处取猜想值，如果答案不正确，我将能够知道正确答案在在猜想值的左侧还是右侧。某种意义上，递归也是这种思路，通过每一步减小问题规模来解决问题。