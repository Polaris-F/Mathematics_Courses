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
- **定义**: 设$\tau_n~(n\geq1)$为第$n$次事件到达的时刻, 则$\tau_n = \inf \{ t > 0: N(t) \geq n \}$或$\tau_n = \inf \{ t > 0: N(t) = n \}$
- **定理**: 设$\{ N(t), t \geq 0 \}$为强度为$\lambda$的泊松过程, 则
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
f_{\tau_{1:n}}(t_1, ..., t_n) =
\begin{cases}
	\lambda^n e^{-\lambda t_n}, & 0 < t_1 < \cdots < t_n \\
	0, & otherwise
\end{cases} 
$$
  - 已知$N(t)=n$的条件概率密度:
$$
f_{\tau_{1:n}}(t_1, ..., t_n | N(t)=n) =
\begin{cases}
	\frac{n!}{t^n}, & 0 < t_1 < \cdots < t_n \leq t \\
	0, & otherwise
\end{cases}
$$
设$U_i \sim U[0, t],~ i=1,...,n$且独立同分布, $U_{(1)}, ..., U_{(n)}$为顺序统计量, 可以证明$U_{(1)}, ..., U_{(n)}$和$\{\tau_1, ..., \tau_n | N(t)=n \}$同分布

## 到达时间间隔
- **定理**: 设$\{ N(t), t \geq 0 \}$为强度为$\lambda$的泊松过程, 我们用$T_n = \tau_n - \tau_{n-1},~(n=1,2,..)$表示到达时间间隔, 则$\{T_n, n \geq 1\}$独立同分布, 且$T_i~(n\geq1)$服从参数为$\lambda$的指数分布, 即$T_i \sim Exp(\lambda),~ (n\geq1)$
- **定理**: 记数过程$\{ N(t), t \geq 0 \}$是强度为$\lambda$的泊松过程 $\iff$ 其记数的时间间隔$\{T_n, n \geq 1\}$独立且均服从参数为$\lambda$的指数分布.

## 极限定理
- **定理**: 设$\{ N(t), t \geq 0 \}$为强度为$\lambda$的泊松过程, 则$$ \lim\limits_{t \rightarrow\infty} \frac{N(t)}{t} = \lambda ~~a.e. $$

## 推广
### 复合泊松过程

### 非时齐泊松过程

### 空间泊松过程

### 更新过程

## 评论
- 泊松过程为什么在自然界中如此常见?
