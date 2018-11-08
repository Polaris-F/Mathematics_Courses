# 第一章 集类与测度
## 1.1 集合运算与集类

## 1.2 单调类定理(集合形式)
- **定理** 1.2.1 设$C$为一集类
  - 若$C$为代数, 则$m(C) = \sigma(C)$
  - 若$C$为$\pi$类, 则$\lambda(C) = \sigma(C)$


## 1.3 测度与非负集函数
- **定理**1.3.3 设$(\Omega, F, \mu)$为一测度空间, 则$\mu$满足
  - 单调可减性: $A, B \in F, A \subset B, \mu(B) < \infty \Rightarrow \mu(B \backslash A) = \mu(B) - \mu(A)$
  - 从下连续, 从上连续


## 1.4 外测度与测度的扩张 
- **定理** 1.4.7 (**Caratheodory测度扩张定理**): 设$C$为$\Omega$上的一半环, $\mu$为$C$上的一$\sigma$可加非负集函数, 则$\mu$可扩张成$\sigma(C)$上的一测度. 若进一步$\mu$在$C$上为$\sigma$有限,  且$\Omega \in C_\sigma$, 则这一扩张是唯一的, 并且扩张所得的测度在$\sigma(C)$上也是$\sigma$有限的. 

## 1.5 $\Re^n$中的Lebesgue-Stieltjes测度

# 第二章 可测映射
## 2.1 定义及基本性质
- **定理** 2.1.8 设$(\Omega, \mathscr{F})$为一可测空间, $f$为一(数值)可测函数.
  - 存在可测简单函数序列$\{f_n\}_{n\geq 1}$, 使得$\forall n \geq 1, |f_n| \leq |f|$, 且$\lim_\limits{n \rightarrow \infty} f_n = f, \forall \omega \in \Omega$ (点点收敛)
  - 若$f$非负, 则存在可测简单函数序列$\{f_n\}_{n\geq 1}$, 使得 $f_n \uparrow f$

## 2.2 单调类定理(函数形式)

## 2.3 可测函数序列的几种收敛形式
- **定义** 2.3.1
- **定理** 2.3.4
- **定理** 2.3.5 

# 第三章 积分和$L^p$空间
## 3.1 积分的基本性质
- **定义** 3.1.1 设$f=\sum_{i=1}^n a_i 1_{A_i} \in S^+$, 其中$a_i \geq 0, A_i \in \mathscr{F}$, 则我们定义$\int_\Omega fd\mu = \sum_{i=1}^m a_i \mu(A_i)$. 我们用$\mu(f)$简记$\int_\Omega fd\mu$.

- **命题** 3.1.2 设$f_n, g_n , f, g \in S^+$, 则
  - $\mu(1_A) = \mu(A), \forall A \in \mathscr{F}$ 
  - $\mu(\alpha f) = \alpha \mu(f), \forall \alpha \in \Re_+$
  - $\mu(f+g) = \mu(f) + \mu(g)$
  - $f \leq g \Rightarrow \mu(f) \leq \mu(g)$
  - $f_n \downarrow f, \mu(f_1) < \infty \Rightarrow \mu(f_n) \downarrow \mu(f)$
  - $f_n \uparrow f \Rightarrow \mu(f_n) \uparrow \mu(f)$
  - $f_n \uparrow, g_n\uparrow, \lim\limits_{n\rightarrow\infty}f_n \leq \lim\limits_{n\rightarrow\infty}g_n \Rightarrow \lim\limits_{n\rightarrow\infty}\mu(f_n) \leq \lim\limits_{n\rightarrow\infty} \mu(g_n) $

- **定义** 3.1.4 (任意数值可测函数的积分)
  - 设$f \in\bar{L}^+$,任取$\{f_n | f_n \in S_+\}$, 满足$f_n \uparrow f$, 我们定义$\mu(f) = \lim\limits_{n \rightarrow \infty} \mu(f_n)$ (定理2.1.8保证了这样的$\{f_n\}$的存在)
  - 设$f \in \bar{L}$, 有$f = f^+ - f^-$, 若$\mu(f^+) < +\infty$或$\mu(f^-) < +\infty$, 则称$f$关于$\mu$的**积分存在**, 并定义$\mu(f) = \mu(f^+)-\mu(f^-)$. 若$\mu(f^+) < +\infty$且$\mu(f^-) < +\infty$, 则称$f$关于$\mu$**可积**.

- **定理** 3.1.6 设$\mu(f), \mu(g)$存在.
  - $\forall \alpha \in \Re, \alpha f$积分存在, 且$\mu(\alpha f) = \alpha \mu(f)$
  - 设$f+g$处处有定义, 且$\mu(f)+\mu(g)$处处有意义(即不出现$\infty-\infty$), 则$f+g$积分存在, 且$\mu(f+g) = \mu(f) + \mu(g)$.
  - $|\mu(f)| \leq \mu(|f|)$
  - 若$N$为一零测集, 则$\mu(f1_N) = 0$
  - 若$f \leq g ~~a.e.$, 则$\mu(f) \leq \mu(g)$
  - 若$f \in \bar{L}^+$, 则$f = 0 ~~a.e. \iff \mu(f)=0$
  - 若$f \in \bar{L}^+$, 且$\mu(f) < \infty$, 则$f < \infty ~~ a.e.$且$[f>0]$关于$\mu$为$\sigma$有限

## 3.2 积分号下取极限


## 3.3 不定积分与测度符号
## 3.4 空间$L^p$及其对偶
## 3.5 空间$L^\infty(\Omega, \mathscr{F})$和$L^\infty(\Omega, \mathscr{F}, m)$的对偶