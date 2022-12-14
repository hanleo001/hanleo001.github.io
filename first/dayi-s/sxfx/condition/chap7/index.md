# 定积分

[TOC]

## 定积分的概念

1. 定义：

   ​	(1) 分割

   ​	(2) 作近似和

   ​	(3) 取极限

## 可积的条件

1. 几个充分条件

   >(1). $f\in C[a,b]$
   >
   >(2). 仅有有限个间断点
   >
   >(3). 单调
   >
   >(4). 间断点自变量数列收敛

## 定积分的性质

1. 线性性，乘积性，保号性，单调性，估值性，绝对性只要求$f,g\in R[a,b]$
2. 可加性要求$f$在最大的区间上收敛

### 积分第一中值定理

1. 要求提出去的$f\in C[a,b]$，剩下的$g$需要有$g\in R[a,b]$且g不变号

### 变限积分

1. 若$f\in R[a,b]$，则$\int_a^xf(t)dt \in C[a,b]$
2. 若$f$在$x_0$处连续，则$\int_a^xf(t)dt$在$x_0$初可导

## 微积分基本定理

1. N-L公式：要求$f\in C[a,b]$，且$F^\prime(x)=f(x)$

## 定积分的计算

1. 换元积分法：$f\in C[a,b]$
2. 分部积分：$u,v\in C^{(1)}[a,b]$

### 积分余项泰勒公式

1. $R_n= \frac{1}{n!}\int_a^xf^{(n+1)}(t)(x-t)^ndt$

#### Cauchy 余项泰勒公式

1. $R_n=\frac{f^{(n+1)(\xi)}}{n!}(x-\xi)^n(x-a)=\frac{f^{(n+1)}(a+\theta h)}{n!}(1-\theta)^nh^{n+1}$

## 积分第二中值定理和Riemann引理

1.积分第二中值定理：f可积 g单调（Bonnet型要求非负）

