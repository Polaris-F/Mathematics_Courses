# 第三章 积分和$L^p$空间
## 3.1 积分的基本性质
- 在本节中, 我们将一步一步定义(数值)可测函数的积分
  - 首先定义非负简单可测函数关于测度的积分, 并研究其性质
  - 然后定义非负数值可测函数关于测度的积分
  - 最后定义数值可测函数关于测度的积分

- 给定一完备测度空间$(\Omega, \mathscr{F}, \mu)$, 令
  - $S^+ = \{\Omega上非负可测简单函数全体\}$
  - $L = \{\Omega上实值可测函数全体\}$
  - $\bar{L} = \{\Omega上数值可测函数全体\}$
  - $L^+ = \{\Omega上非负实值可测函数全体\}$
  - $\bar{L}^+ = \{\Omega上非负数值可测函数全体\}$

- **定义** 3.1.1 设$f=\sum_{i=1}^n a_i 1_{A_i} \in S^+$, 其中$a_i \geq 0, A_i \in \mathscr{F}$, 则我们定义$\int_\Omega fdu = \sum_{i=1}^m a_i \mu(A_i)$. 我们用$\mu(f)$简记$\int_\Omega fdu$.

<!--(5)(6)(7)待证明-->
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
  - 设$f \in \bar{L}$, 有$f = f^+ - f^-$, 若$\mu(f^+) < +\infty$或$\mu(f^-) < +\infty$, 则称$f$关于$\mu$的积分存在, 并定义$\mu(f) = \mu(f^+)-\mu(f^-)$. 若$\mu(f^+) < +\infty$且$\mu(f^-) < +\infty$, 则称$f$关于$\mu$可积.

- 注记
  - 非负简单可测函数的积分是定义在测度空间$(\Omega, \mathscr{F}, \mu)$上的. 定义可测函数只需要可测空间$(\Omega, \mathscr{F})$, 并不需要定义在其上的测度$\mu$.
  - 定义3.1.4是well-defined, 可以证明$\lim\limits_{n \rightarrow \infty} \mu(f_n)$不依赖于$\{f_n\}$的选取, 即如果$f_n \uparrow f$且$g_n \uparrow f$, 则$\lim\limits_{n \rightarrow \infty} \mu(f_n)= \lim\limits_{n \rightarrow \infty} \mu(g_n)$.
  - 回顾我们定义(数值)可测函数积分的过程: 我们首先定义非负简单可测函数的积分, 然后利用定理2.1.8和前面积分的性质定义了任意非负可测函数的积分, 最后我们使用将函数将分解为正部和负部的技巧, 然后定义了一般可测函数的积分.

## 3.2 积分号下取极限
## 3.3 不定积分与测度符号
## 3.4 空间$L^p$及其对偶
## 3.5 空间$L^\infty(\Omega, \mathscr{F})$和$L^\infty(\Omega, \mathscr{F}, m)$的对偶
