---
title: 20210923 附加题一
layout: post
date: 2021-09-23 21:00:00 +0800
categories:
  extra-credit
mathjax: true
---

## 题目

$$ 1 + {1 \over 1 + 2} + {1 \over 1 + 2 + 3} + ... + {1 \over 1 + 2 + 3 + ... + 100} $$

## 解答

从 $$ {1 \over 1 + 2} $$ 到 $$ {1 \over 1 + 2 + 3 + 4 + ... + 100} $$ 的分母，都是多项式求和。求和公式是：

$$ { n (a_1 + a_n) \over 2 } $$ 

所以有：

$$ {1 \over a_1 + ... + a_n} = { 2 \over n (a_1 + a_n)} $$

其中 $$ a_1 = 1 $$，$$ a_n = n $$，于是有：

$$ { 1 \over n (a_1 + a_n) } = {1 \over n (n + 1)} $$

这里牵涉到一个裂项公式：

$$ {1 \over n (n + 1)} =  {1 \over n} - {1 \over (n + 1)} $$

> 推导如下：
> 
> $$
> \begin{align}
> { 1 \over n (n + 1) } 
> &= { {1 + n - n} \over {n (n + 1)} } \\
> &= { {(n + 1) - n} \over {n (n + 1)} } \\
> &= { (n + 1) \over n (n + 1) } - { n \over n (n + 1) } \\
> &= { 1 \over n } - { 1 \over (n + 1) } 
> \end{align}
> $$

故题目原式：

$$ 1 + {1 \over 1 + 2} + {1 \over 1 + 2 + 3} + ... + {1 \over 1 + 2 + 3 + ... + 100} $$

$$
\begin{align}
&= {1 + 2 [ ({1 \over 2} - {1 \over 3}) + ({1 \over 3} - {1 \over 4}) + ({1 \over 4} - {1 \over 5}) + ... + ({1 \over 100} - {1 \over 101}) ]} \\ 
&= {1 + 2 ({1 \over 2} - {1 \over 101})} \\
&= {1 + 1 - \frac{2}{101} } \\
&= 1 {99 \over 101} 
\end{align}
$$
