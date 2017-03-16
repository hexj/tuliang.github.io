---
layout: post
title: 麻省理工《计算机科学及编程导论》
category: open
---
课程介绍: 

这门课程适用于那些拥有很少或没有编程经验的学生,它致力于使学生理解计算机在解决问题中的作用,并且帮助学生，不论其专业，使他们对于能够完成有用的小程序的目标充满信心。这门课程将使用Python语言进行教学。

课程类型:  计算机

<img class="cover" title="Prof. Eric Grimson教授 Prof. John Guttag教授" src="/images/2012/02/20110330162757dd152-300x180.jpg" alt="Prof. Eric Grimson教授 Prof. John Guttag教授" width="300" height="180" />

课程主讲人: Prof. Eric Grimson 教授 Prof. John Guttag 教授

埃里克格里姆森是美国麻省理工学院计算机科学与工程系的教授，并在麻省理工学院的伯纳德持的戈登医学工程主席。 教授格里姆森在麻省理工学院曾担任教育科学部主任，电气工程和计算机副系主任。 自2005年以来，他一直担任计算机科学和电机工程学系的院长。 在1975年，他获得了里贾纳大数学 （高荣）和学物理学士， 1980年，麻省理工学院数学博士学位。 格里姆森教授是麻省理工学院计算机科学和人工智能实验室成员，他的集团已率先领域和许多其他国家的艺术系统和行为识别活动，对象和人识别，图像数据库索引，图像引导手术，现场模拟计算机视觉。 格里姆森教授协会是IEEE的资深会员，并在麻省理工学院获得了玻色教学卓越奖。

[第 1 课 课程简介及数据类型](#section-1)

[第 2 课 分支、条件和循环](#section-2)

[第 3 课 循环式程序样式](#section-3)

[第 4 课 函数抽象、递归简介](#section-4)

[第 5 课 浮点数和逐次近似](#section-5)

[第 6 课 二分法、牛顿法、列表简介](#section-6)

[第 7 课 列表和可变性、字典、效率简介](#section-7)

[第 8 课 算法复杂度: 对数、线性、二次、指数](#section-8)

[第 9 课 折半搜索、泡沫排序和选择排序](#section-9)

[第 10 课 归并排序、哈希函数、异常处理](#section-10)

[第 11 课 测试和调试](#section-11)

[第 12 课 调试、背包问题、动态规划简介](#section-12)

[第 13 课 动态规划: 重复子问题、最优子结构](#section-13)

[第 14 课 面向对象编程简介](#section-14)

[第 15 课 抽象数据类型、类、方法](#section-15)

[第 16 课 封装、继承、遮蔽](#section-16)

[第 17 课 计算模型: 随机游走模拟](#section-17)

[第 18 课 表示模拟结果、Pylab作图](#pylab)

[第 19 课 有偏随机游走、分布](#section-18)

[第 20 课 蒙特卡洛模拟、估算π](#section-19)

[第 21 课 验证模拟结果、曲线拟合、线性回归](#section-20)

[第 22 课 正态、均匀和指数分布](#section-21)

[第 23 课 股市模拟](#section-22)

[第 24 课 课程总回顾: 按计算机科学家那样思考](#section-23)

## 笔记

---

### 第 1 课 课程简介及数据类型

没有一个问题的提出，是要命的。我们不会用他们来淘汰你们，而是用他们来帮助你们学习。

我们不会发课件。事实证明学生在自己做笔记的时候学得更好，讽刺的是即使他们永远不看那些笔记。

我们的目标都是为了帮助你像一个计算机科学家一样思考。换一种说法就是，我们想赋予你一种能力，以让你可以用计算机做你想做的任何事。我们希望每当你要面对一些技术问题的时候，你们的本能之一将会是: “我怎么才能编写一个代码来帮我解决这问题？”

知识分为两种: 陈述性（declarative）的知识和程序性（imperative）的知识。 陈述性的知识用叙述事实来思考它，它维护了真相。它告诉你怎么才可能去检查一些事儿，但是它没有说怎样检查。而这就是程序性的知识。程序性的知识是对推论过程的描述。

你在课堂上应该学会如何设计菜谱，如何构建菜谱，如何在Python语言的模式中设计东西，而不是一些细节问题。

---

### 第 2 课 分支、条件和循环

无论我们创建一种多么复杂的数据结构，都是基于字符串，数字以及布尔类型。

解释器实际上是机器内置的按照我们描述的规则，来推算出结果值并把值显示出来的一个东西。

---

### 第 3 课 循环式程序样式

流程图是一种代码结构视觉化的工具。因为它让我们看到了，循环在什么地方、那里初始化变量以及什么时候条件判断等等。它的意义在于，如果你开始按照流程图往下走，你就是将抽象的代码操作给视觉化和直观化，它能帮助构思代码结构以及理清你的思路。

对于简单分支式程序，运行程序花费的总时间，受限于指令（instructions）的数目，毕竟每个指令最多执行一次。而其他程序，例如一个循环程序，它所花费的时间取决于循环的次数，即指令执行次数取决于循环是次数。

模拟执行，指的是取一下简单值，过一遍，看看会怎么样。

对于任何循环，有两点是必须检测的。必须保证程序能够终止并且必须保证结果是合理的。

防御式编程（defensive programming）必须能够: 保证遍历了代码中所有分支；保证对每个分支，打印或返回的结果有意义；保证所有可能的输入数据都能对应一个分支，并且不会产生错误或无限循环。

元组（tuple）指的是有序的元素列。它是不可变的（而数组则是可以改变的）。例子: 

{% highlight python %}
test = (1, 2, 3, 4, 5)
{% endhighlight %}

---

### 第 4 课 函数抽象、递归简介

到现在为止，我们学习了赋值语句、条件语句、输入/输出、循环结构以及各种数据类型。我们使用这些就可以称为图灵完全（Turing-complete），也就是说，有了这些以后，就可以写出任何程序了。

农场中有一群猪和一群鸡，有一天农场主看到有x个头和y个脚，求该农场有多少头猪和多少只鸡: 

{% highlight python %}
def solve(numLegs, numHeads):
  for numChicks in range(0, numbeads + 1)
    numPigs = numHeads - numChicks
    totLegs = 4*numPigs + 2*numChicks
    if totLegs == numLegs
      return [numPigs, numChicks]
    return [None, None]

def barnYard():
  heads = int(raw_input('Enter number of heads: '))
  legs =  int(raw_input('Enter number of legs: '))
  pigs, chickens = solve(legs, heads)
  if pigs == None:
    print 'There is no solution'
  else:
    print 'Number of pigs:'.pigs
    print 'Number of chickens:'.chickens
{% endhighlight %}

递归: 只要基础情况正确，递归步骤正确，就能将问题简化为更简单的相同问题，最终代码收敛并给出答案。
斐波那契（Fibonacci）数列，给出两个数，后面产生的数都是在自己之前的两个数的和，即`x_3 = x_1 + x_2, x_4 = x_2 + x_3 ...`

{% highlight python %}
def fib(x):
  if x == 0 or x == 1: return 1
  else: return fib(x - 1) + fib(x - 2)
{% endhighlight %}

---

### 第 5 课 浮点数和逐次近似

Python与其他语言不同，它有一种“任意精度整数”。也就是说，你想让它有多大，它就能有多大（小数则不行，最多精确到17位）。例如2的1000次方: 

{% highlight python %}
2 ** 1000
{% endhighlight %}

二分法的基本思路: 所有可能的答案构成一个线性排列的空间。若在某处取猜想值，如果答案不正确，我将能够知道正确答案在在猜想值的左侧还是右侧。某种意义上，递归也是这种思路，通过每一步减小问题规模来解决问题。

---

### 第 6 课 二分法、牛顿法、列表简介

回归测试（regression testing），这个测试就是为了保证来重复检测整个程序是否运行良好。

收敛速度（speed of convergence）

牛顿法，先设定一个初始猜测值guess，然后求得该值对应函数的切点斜率。在绝大多数情况下，不是所有的情况，切线在解的附近，是曲线很好的近似。因此，切线在X轴上的截距会比先前更接近正确的解。如果初始guess是最下面这一点，即guess=0，切线与X轴平行并没有相交，后面自然做不下去了。这种情况是数值计算程序中最需要关注的。相对于二分法，牛顿法的效率要高很多。

计算机的答案不一定正确，毕竟在计算机中终归都是人写的程序。保持疑问是个好习惯。

列表和字符串有两处不同: 一是它可变，二是其值不一定要由字符组成。

---

### 第 7 课 列表和可变性、字典、效率简介

除了拼写单词，永远不要使用小写的l，你很难将它和数字1分别开。

在一般情况下: 

{% highlight python %}
a=1
b=a
a=2
{% endhighlight %}

最后结果是`a=2，b=1`。而在列表中赋值是通过不同路径指向同一对象，并不是像上面的a指向了一个新的2，列表会把之前的1修改为2。

同列表一样，字典类型也是可变的。也具有多样性，但与列表不同的是字典的元素没有顺序。 另外，它包含一般化的索引。列表和字符串只能通过整数获取其元素，而字典里的任意元素都可以考虑为一对键和值，其中键用作索引（字典类型运用到了哈希表（Hash table）技术，其实就是PHP中的数组）。

效率显然是编写代码需要重点考虑的内容，我们经常首先关注的是代码功能的实现，然后再来找更高效的实现方法。

---

### 第 8 课 算法复杂度: 对数、线性、二次、指数

如果你想成为一个好的设计师（designer）就要学会用已学知识处理未知问题。碰到新问题时，你应该想想它和什么最像？以及哪类算法可以应用到这类问题上，然后从这些可能有用的算法中选用什么算法最为合适？

我们主要关注问题规模变大造成的增长率。

大O符号,它表示增长的上界，随着输入规模增加，函数增长的上界。

在各种算法中复杂度分为对数 < 线性 < 二次 < 指数，对数是每次将问题分解成一个小问题（除法），线性是每次将问题减少常数次（加减法），二次是每次将问题增加（乘法） ，线性是每次将问题进行指数性的增加（指数）

---

### 第 9 课 折半搜索、冒泡排序和选择排序

折半搜索的前提是有一个有序列表
一、取中点
二、判别中点是否为要找的结果
三、如果不是，将问题减半，然后重复
本质上，这个模板体现了对数算法（分治算法）

选择排序又名为单元排序，每一趟从待排序的数据元素中选出最小（或最大）的一个元素，顺序放在已排好序的数列的最后，直到全部待排序的数据元素排完。

冒泡排序，依次比较相邻的两个数，将小数放在前面，大数放在后面。即在第一趟: 首先比较第1个和第2个数，将小数放前，大数放后。然后比较第2个数和第3个数，将小数放前，大数放后，如此继续，直至比较最后两个数，将小 数放前，大数放后。至此第一趟结束，将最大的数放到了最后。在第二趟: 仍从第一对数开始比较（因为可能由于第2个数和第3个数的交换，使得第1个数不再小 于第2个数），将小数放前，大数放后，一直比较到倒数第二个数（倒数第一的位置上已经是最大的），第二趟结束，在倒数第二的位置上得到一个新的最大数（其 实在整个数列中是第二大的数）。如此下去，重复以上过程，直至最终完成排序。由于在排序过程中总是小数往前放，大数往后放，相当于气泡往上升，所以称作冒泡排序。

---

### 第 10 课 归并排序、哈希函数、异常处理

归并排序是建立在归并操作上的一种有效的排序算法。该算法是采用分治法（Divide and Conquer）的一个非常典型的应用。将已有序的子序列合并，得到完全有序的序列；即先使每个子序列有序，再使子序列段间有序。若将两个有序表合并成一个有序表，称为二路归并。

分治算法如果只是一个劲地分，而不考虑合的复杂性，也许会得不偿失。所以真正好的分治算法，不仅分起来简单，合起来也需要不太复杂。

有一种搜索算法它甚至比折半搜索还好，它就是哈希（hash或译作“散列”）

在计算机科学中很多情况下，效率可以通过牺牲空间取得。

---

### 第 11 课 测试和调试

单元测试，单独确认程序每段代码。
集成测试，将整个程序集成后，看是否运行正确。

首先研究既有数据，你需要用一种怀疑的眼光来看问题。然后形成一种假设，让它与所有数据一致。从而设计并开始一个可重复的实验。

---

### 第 12 课 调试、背包问题、动态规划简介

大体上说，最优化问题（optimization problem）都差不多。包括两部分，一些你想获得最大或最小值的函数，还必须符合一些约束条件。典型的最优化问题，其中一个最著名的是最短路径问题。另一类的最优化问题是旅行商问题（traveling salesman problem）。装箱问题（bin packing），用大小不同形状不同的东西填装容器。 序列比问题（sequence alignment），例如DNA序列，RNA序列。还有一个最优化问题，背包问题（knapsack problem）。

背包问题具体来说是，你有一堆东西，东西比较多背包放不下，你需要选择带什么，留下什么。你需要在背包能带东西有限的情况下，最大化你所带东西的价值。

在贪婪算法中，需要在每一步最大化你的值。不用提前计划，做好当前的事情就好。就像是有些人吃东西时先吃甜点，这样能够保证在吃饱前吃到最好的东西。

局部的最优化并不能保证全局的最优化。所以，你不能重复的进行局部优化，期望得到全局的最优。

动态规划（dynamic programming），不要在这个名字上花费精力。这个方法由数学家贝尔曼发明，国防部曾经让他帮忙做一些工作，他不想让他们知道他在做什么，所以他编造了一个与此毫不相关的名字。不幸的是，我们一直沿用至今。所以不要认为，它特指任何动态的东西。它能解决很多表面上是指数增长的问题，关键有两点，一是找到重叠子问题，二是所谓最优子结构。

---

### 第 13 课 动态规划: 重复子问题、最优子结构

斐波那契数列

{% highlight python %}
def fib(n):
  global numCalls
  numCalls +=1
  #print 'fib调用', n
  if n<=1:
    return 1
  else:
    return fib(n-1)+fib(n-2)
numCalls = 0
n = 6
res = fib(n)
print 'fib_', n, '=', res, '调用次数为', numCalls

def fastFib(n, memo):
  global numCalls
  numCalls +=1
  #print 'fib1调用', n
  if not n in memo:
    memo[n]=fastFib(n-1, memo) + fastFib(n-2, memo)
  return memo[n]

def fib1(n):
  memo = {0:1, 1:1}
  return fastFib(n, memo)

numCalls = 0
n = 6
res = fib1(n)
print 'fib_', n, '=', res, '调用次数为', numCalls
{% endhighlight %}

我们看到加上memo这个缓存后，算法的复杂度减少了不少，根本原因就是我们找到重叠子问题，并且将结果缓存起来，避免重复计算。整个算法的的核心就是: 

{% highlight python %}
#如果memo中不存在斐波那契数列的第n个数
#则计算该数
if not n in memo:
  memo[n]=fastFib(n-1, memo) + fastFib(n-2, memo)
#如果存在就直接返回该数
return memo[n]
{% endhighlight %}

把之前解决了的问题作为数据储存起来。依赖表查找查询之前数据，而缓存法是一种特殊情况。表查找是一种常见的方式，当你解决复杂的问题时，保存答案然后供以后使用。看到算法刚开始时间复杂度是1700万，增加缓存后变为1800，是相当令人震惊的。缓存这种方法其实就是我们常说的空间换时间。

---

### 第 14 课 面向对象编程简介

对象表示一系列的数据和函数。这里关键的思想在于将数据和处理数据的函数当作一体。这样的好处在于把对象传给程序其他部分时，那部分程序也有能力处理这个对象。这种数据及相应处理函数的组合是面向对象编程的本质。

---

### 第 15 课 抽象数据类型、类、方法

可以将类考虑为创造对象实例的模板。

Python中的`self`关键字是其他语言中的`this`关键字。

数据隐藏是只能通过定义的方法，来访问实例值。很遗憾，Python没有强制数据隐藏。

---

### 第 16 课 封装、继承、遮蔽

Python中的`__init__`是其他语言中的构造函数。

映射也常常称为重载。

---

### 第 17 课 计算模型: 随机游走模拟

从一个不太正式的问题描述去得到一个更加正式的问题。从某种程度上来说，就是我们如何来进行问题优化的。

创造计算模型。我们几乎写的每个有意义的程序在某种意义上来说都是对真实世界的建模。如果我们要写一个帮助我们决定买还是卖股票的程序，在某种意义上就是在尝试对股票市场进行建模。

---

### 第 18 课 表示模拟结果、Pylab作图

学会问自己答案是不是合理。是不是违反直觉？是不是和事实相符？

---

### 第 19 课 有偏随机游走、分布

好设计的关键: 将你程序的各个部分进行独立决策，当你遇到什么不可避免的事情时，你就可以加强代码，或者你发现什么错误时，你所需要的改变都是有限的。（PS: 我们使用的面向对象的那些策略和各种设计模式大多原理中就包含了这个。）

---

### 第 20 课 蒙特卡洛模拟、估算π

随机模拟程序会有一些有趣的问题，我们要运行多少次才能相信答案是正确的呢？

蒙特卡洛(Monte Carlo)模拟，某种程度上是演绎统计学的应用。一个随机选择的样例，一般能够体现出它所在分类的一些性质。

---

### 第 21 课 验证模拟结果、曲线拟合、线性回归

通过取样我们不可能得到完美的精确度，除非你取样是整个群体。无论你取多少样本，除非你判断每个元素，否则你是不可能确定这个样本集合是典型的。没办法确定是否选择了一个不公正的样本，除非查看了整个群体。所以我们不可能知道我们的预测是否正确。

一个答案是统计可靠地，但并不代表它就是正确答案。这是因为它的一些影响判断的基础假设是错误的。这个时候我们就需要去通过和物理事实相比检查答案的正确性。

大多数情况都能靠某个模型来解释，而有一些情况不能解释。在那些不能解释的情况中往往是**潜在变量（lurking variable）**在影响结果。当你在建立模型的时候需要去寻找这些潜在变量，在寻找潜在变量时你要小心**过度拟合**。

---

### 第 22 课 正态、均匀和指数分布

数据滥用

*  注意是谁给你的数据，而不是数据本身。
*  共存即原因。它的意思是关联性，并不代表因果性 ，你需要寻找潜在变量（lurking variable） 。（即因果关系过度单纯化 ）
*  非响应性倾向（non-response bias）。实际上它就是无代表意义的样本。
*  数据提升（data enhancement）。它的意思是在数据中读出来超过它原有意义的东西。（即过分解读）

---

### 第 23 课 股市模拟

泊松（Poisson），人们常常用泊松过程来对事物进行建模，也就是说过去行为的过程，对未来的行为是没有影响的，也就是说它是无记忆性的。

---

### 第 24 课 课程总回顾: 按计算机科学家那样思考

首先理解这个问题，然后想一想解决方案的整体架构，然后不考虑怎么实现的前提下去考虑算法。这是个和用Python还是Java或者C++无关的决定。事实上，把一个拥有良好的架构的程序，从一种编程语言转为另外一种是很容易的。