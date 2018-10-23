# 第二章 随机过程的基本概念
## 严格定义
- 设给定的**概率测度空间**$(\Omega, F, P)$和**时间参数**$\mathbb{T} \subset \Re^+=[0, +\infty)$, 若对每一个$t \in \mathbb{T}$, 都有定义在$(\Omega, F, P)$上的随机变量$X(t, \omega), \omega \in \Omega$, 则称依赖于参数$t \in \mathbb{T}$的随机变量族$\{ X(t, \omega),  t \in \mathbb{T} \}$为一个定义在概率测度空间$(\Omega, F, P)$上的**随机过程**, 并称集合$t \in \mathbb{T}$为(时间)参数空间, $X(t)~(t \in \mathbb{T})$的所有可能取值的集合为**状态空间**, 常记为$\mathbb{E}$. 
- 可以把随机过程看做二元函数: $X(t, \omega), ~ (t, \omega) \in \mathbb{T}\times\Omega$
  - 固定$t$, $X(t, \cdot)$是$(\Omega, F, P)$上的随机变量
  - 固定$\omega$, $X(\cdot, \omega)$是关于$t$的函数, 常称为样本轨道

- 评论
  - 感觉从测度论出发, 还能写出更加简洁和深刻的定义.

## 刻画