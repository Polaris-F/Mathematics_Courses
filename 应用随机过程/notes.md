- 课程名称: 应用随机过程
- 教材: 《应用随机过程》 (韩东,王桂, 熊德文 著)
- 简介: 


<!--![](figures/BMonSphere.jpg)-->

# 第一章 概率论精要
## 概率的公理化
## 条件分布与条件期望
## 随机变量序列的收敛性
## 大数定律与中心极限定理


# 第二章 随机过程的基本概念
## 严格定义
- 设给定的**概率测度空间**$(\Omega, F, P)$和**时间参数**$\mathbb{T} \subset \Re^+=[0, +\infty)$, 若对每一个$t \in \mathbb{T}$, 都有定义在$(\Omega, F, P)$上的随机变量$X(t, \omega), \omega \in \Omega$, 则称依赖于参数$t \in \mathbb{T}$的随机变量族$\{ X(t, \omega),  t \in \mathbb{T} \}$为一个定义在概率测度空间$(\Omega, F, P)$上的**随机过程**, 并称集合$t \in \mathbb{T}$为(时间)参数空间, $X(t)~(t \in \mathbb{T})$的所有可能取值的集合为**状态空间**, 常记为$\mathbb{E}$. 
- 可以把随机过程看做二元函数: $X(t, \omega), ~ (t, \omega) \in \mathbb{T}\times\Omega$
  - 固定$t$, $X(t, \cdot)$是$(\Omega, F, P)$上的随机变量
  - 固定$\omega$, $X(\cdot, \omega)$是关于$t$的函数, 常称为样本轨道

- 评论
  - 感觉从测度论出发, 还能写出更加简洁和深刻的定义.

## 刻画

# 第三章 泊松过程
## 定义
- **泊松过程是一个记数的随机过程**
- $N(t)$: $[0, t]$时间内事件发生的次数, 如: 某商场的顾客数, 某路口通过的汽车数,等等
- 我们称满足以下三个条件的记数过程$\{ N(t), t \geq 0 \}$为强度为$\lambda$的(时间齐次的)**泊松过程**:
  - (P1) $N(0) = 0$
  - (P2) $N(t)$具有**平稳独立增量性**, 即, (1)**平稳性**或时齐性: $N(t+s)-N(s)$与$N(t+r)-N(r)$同分布; (2)**独立增量性**: 设$u < s < t$, 则$N(s)-N(u)$与$N(t)-N(s)$独立
  - (P3) 普适性: 在充分小的时间间隔内, 最多只有一次呼叫, 即, $$P\big( N(\Delta t)=1 \big) = \lambda\Delta t + o(\Delta t)$$ $$ P\big( N(\Delta t)\geq2 \big) = o(\Delta t) $$
- 由(P1)(P2)(P3)可以推出一条非常重要的性质P(3)*: $$ P\big( N(t)=k \big) = e^{-\lambda t} \frac{(\lambda t)^k}{k!}, ~~ k=0,1,2,... $$
- 可以证明(P1)(P2)(P3)与(P1)(P2)(P3)*为等价定义. 后者在实际中更便于应用.
- 数字特征
  - $\mathbb{E}[N(t)] = \lambda t$
  - $D[N(t)] = \lambda t$
  - $Cov(N(s), N(t)) = \lambda\cdot\min(s,t)$

- 评论
  - 之前已经在初等概率论和数理统计课中遇到多次泊松过程分布和泊松过程过程, 一直觉得泊松分布的表达式长得特别不自然(我对高斯分布也有同感), 为什么这么奇怪的分布函数可以用来描述记数过程. 后来了解到[泊松分布可以看作二项分布的极限情况](https://www.le.ac.uk/users/dsgp1/COURSES/LEISTATS/poisson.pdf), 这样理解起来就自然很多了. 但这里推导出泊松分布的过程就更加自然了: 先定义一个符合直觉的随机过程, 然后由此定义导出随机变量的分布函数. 历史上关于泊松分布的由来还不清楚, 后续有时间再去了解.

## 到达时间
- 定义: 设$\tau_n~(n\geq1)$为第$n$次事件到达的时刻, 则$\tau_n = \inf \{ t > 0: N(t) \geq n \}$或$\tau_n = \inf \{ t > 0: N(t) = n \}$
- 定理: 设$\{ N(t), t \geq 0 \}$为强度为$\lambda$的泊松过程, 则
  - $\tau_n \sim Gamma(n, \lambda)$: 
$$ 
f_{\tau_n}(t) =
\begin{cases}
	\lambda e^{-\lambda t} \frac{(\lambda t)^{n-1}}{(n-1)!}, & t \geq 0\\
	0, & t < 0
\end{cases} 
$$
  - $(\tau_1, ..., \tau_n)$联合概率密度: 
$$ 
f_{\tau_{1:n}}(t1, ..., t_n) =
\begin{cases}
	\lambda^n e^{-\lambda t_n}, & 0 < t_1 < \cdots < t_n \\
	0, & otherwise
\end{cases} 
$$


## 到达时间间隔
## 极限定理
## 推广