# 第三章 积分和$L^p$空间
## 3.1 积分的基本性质
- 在本节中, 我们将一步一步定义(数值)可测函数的积分
  - 首先定义非负简单可测函数关于测度的积分, 并研究其性质(命题3.1.2)
  - 然后定义非负数值可测函数关于测度的积分
  - 最后定义(数值)可测函数关于测度的积分, 并研究其性质(定理3.1.6)

- 给定一完备测度空间$(\Omega, \mathscr{F}, \mu)$, 令
  - $S^+ = \{\Omega上非负可测简单函数全体\}$
  - $L = \{\Omega上实值可测函数全体\}$
  - $\bar{L} = \{\Omega上数值可测函数全体\}$
  - $L^+ = \{\Omega上非负实值可测函数全体\}$
  - $\bar{L}^+ = \{\Omega上非负数值可测函数全体\}$

- **定义** 3.1.1 设$f=\sum_{i=1}^n a_i 1_{A_i} \in S^+$, 其中$a_i \geq 0, A_i \in \mathscr{F}$, 则我们定义$\int_\Omega fd\mu = \sum_{i=1}^m a_i \mu(A_i)$. 我们用$\mu(f)$简记$\int_\Omega fd\mu$.

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
  - 设$f \in \bar{L}$, 有$f = f^+ - f^-$, 若$\mu(f^+) < +\infty$或$\mu(f^-) < +\infty$, 则称$f$关于$\mu$的**积分存在**, 并定义$\mu(f) = \mu(f^+)-\mu(f^-)$. 若$\mu(f^+) < +\infty$且$\mu(f^-) < +\infty$, 则称$f$关于$\mu$**可积**.

- **定义** 3.1.5: 设$f \in \bar{L}$, 若$\mu(f)$存在, 则对$\forall A \in \mathscr{F}, f1_A$可积. 定义$\int_A f d\mu = \int_\Omega f 1_A d\mu = \mu(f1_A)$

- **定理** 3.1.6 设$\mu(f), \mu(g)$存在.
  - $\forall \alpha \in \Re, \alpha f$积分存在, 且$\mu(\alpha f) = \alpha \mu(f)$
  - 设$f+g$处处有定义, 且$\mu(f)+\mu(g)$处处有意义(即不出现$\infty-\infty$), 则$f+g$积分存在, 且$\mu(f+g) = \mu(f) + \mu(g)$.
  - $|\mu(f)| \leq \mu(|f|)$
  - 若$N$为一零测集, 则$\mu(f1_N) = 0$
  - 若$f \leq g ~~a.e.$, 则$\mu(f) \leq \mu(g)$
  - 若$f \in \bar{L}^+$, 则$f = 0 ~~a.e. \iff \mu(f)=0$
  - 若$f \in \bar{L}^+$, 且$\mu(f) < \infty$, 则$f < \infty ~~ a.e.$且$[f>0]$关于$\mu$为$\sigma$有限

- 注记
  - 非负简单可测函数的积分是定义在测度空间$(\Omega, \mathscr{F}, \mu)$上的. 定义可测函数只需要可测空间$(\Omega, \mathscr{F})$, 并不需要定义在其上的测度$\mu$.
  - 定义3.1.4是well-defined, 可以证明$\lim\limits_{n \rightarrow \infty} \mu(f_n)$不依赖于$\{f_n\}$的选取, 即如果$f_n \uparrow f$且$g_n \uparrow f$, 则$\lim\limits_{n \rightarrow \infty} \mu(f_n)= \lim\limits_{n \rightarrow \infty} \mu(g_n)$.
  - 回顾我们定义(数值)可测函数积分的过程: 我们首先定义非负简单可测函数的积分, 然后利用定理2.1.8和前面积分的性质定义了任意非负可测函数的积分, 最后我们使用将函数将分解为正部和负部的技巧, 然后定义了一般可测函数的积分.

## 3.2 积分号下取极限
- 在本节中, 我们将介绍三个非常重要的有关积分下取极限的定理, 分别是
  - 单调收敛定理
  - Fatou引理
  - 控制收敛定理

<!--待证明-->
- **引理** 3.2.1 设$f_n, f  \in \bar{L}_+$
  - 若$f_n \leq f_{n+1} ~a.e.~  \forall n \geq 1$, 且$f_n \xrightarrow{a.e.} f$, 则$\lim\limits_{n\rightarrow\infty}\mu(f_n) = \mu(f)$
  - 若$f_n \geq f_{n+1} ~a.e.~  \forall n \geq 1$, 且$f_n \xrightarrow{a.e.} f$, 且$\mu(f_1)<\infty$, 则$\lim\limits_{n\rightarrow\infty}\mu(f_n) = \mu(f)$

- **定理** 3.2.3 (**单调收敛定理**) 设$f_n \in \bar{L}$, 且$\mu(f_n)$存在
  - $f_n \uparrow f ~a.e.~$, 且$\mu(f_1) > -\infty$, 则$\mu(f)$存在, 且$\mu(f_n) \uparrow \mu(f)$ 
  - $f_n \downarrow f ~a.e.~$, 且$\mu(f_1) < +\infty$, 则$\mu(f)$存在, 且$\mu(f_n) \downarrow \mu(f)$ 

- **引理** 3.2.4 (**Fatou引理**) 设$f_n \in \bar{L}$, 且$\mu(f_n)$存在
  -  若$\exists g \in \bar{L}, \mu(g) > -\infty$, 使得$f_n \geq g ~a.e.~\forall n\geq1$, 则$\lim\limits_{n\rightarrow\infty}\inf\limits_{k \geq n}f_k$存在, 且$\mu\big(\lim\limits_{n\rightarrow\infty}\inf\limits_{k \geq n}f_k\big) \leq \lim\limits_{n\rightarrow\infty}\inf\limits_{k \geq n}\mu(f_k)$
  -  若$\exists g \in \bar{L}, \mu(g) < +\infty$, 使得$f_n \leq g ~a.e.~\forall n\geq1$, 则$\lim\limits_{n\rightarrow\infty}\sup\limits_{k \geq n}f_k$存在, 且$\mu\big(\lim\limits_{n\rightarrow\infty}\sup\limits_{k \geq n}f_k\big) \geq \lim\limits_{n\rightarrow\infty}\sup\limits_{k \geq n}\mu(f_k)$

<!--待证明-->
- **定理** 3.2.5 (**控制收敛定理**) 设$f_n \in \bar{L}, f \in \bar{L}$, 且$f_n \xrightarrow{a.e.}f$或$f_n \xrightarrow{\mu}f$. 若存在$g \in \bar{L}_+, \mu(|g|)<\infty$, 使得$\forall n \geq 1$有$|f_n|<g~a.e.$, 则$f$可积, 且有$\lim\limits_{n\rightarrow\infty}\mu(f_n) = \mu(f)$ 

- **定理** 3.2.7

- **定理** 3.2.9

- 注记
  - 单调收敛定理, Fatou引理, 控制收敛定理都是在讲什么情况下可以交换求极限和求测度的顺序

## 3.3 不定积分与测度符号
- 在本节中, 我们将
  - 定义符号测度, 不定积分

- **引理** 3.3.1 设$f \in \bar{L}$, 且$f$的积分存在, 令$$\nu(A) = \mu(f1_A), A \in \mathscr{F},$$ 则$\nu$为$\mathscr{F}$上的$\sigma$可加集函数, 此外, 令$$ \nu^+(A) = \mu(f^+1_A),~ \nu^-(A) = \mu(f^-1_A), A \in \mathscr{F}, $$ 则$\nu^+, \nu^-$为$(\Omega, \mathscr{F})$上的测度, 其中之一为有限测度, 且有$\nu = \nu^+ - \nu^-$. 

- **定义** 3.3.2 $(\Omega, \mathscr{F})$为一可测空间
  - 设$\nu$为$\mathscr{F}$上的一$\sigma$可加集函数, 称$\nu$为**符号测度**
  - $f\in\bar{L}$, 且$f$的积分存在, 则由引理3.3.1中定义的符号测度$\nu$称为$f$关于$\nu$的**不定积分**, 并记为$\nu = f\cdot\mu$

- **注** 3.3.3 设$\nu$为$(\Omega, \mathscr{F})$上一符号测度
  - $\forall A \in \mathscr{F}$, 要么$-\infty \leq \nu(A) < \infty$, 要么$-\infty < \nu(A) \leq \infty$, 不会出现$\nu(A)=-\infty, \nu(B)=\infty$.
  - $\nu(\emptyset)=0$

<!--待证明-->
- **定理** 3.3.4 (**Jordan-Hahn 分解定理**) 设$\nu$为$(\Omega, \mathscr{F})$上的一符号测度. 
  - **Jordan分解**: 对$A \in \mathscr{F}$, 令$$ \nu^+(A) = \sup\{ \nu(B) | B \subset A, B \in \mathscr{F} \}, $$ $$ \nu^-(A) = \sup\{ -\nu(B) | B \subset A, B \in \mathscr{F} \}. $$ 则$\nu^+, \nu^-$为测度, 其中之一为有限测度. 且有$\nu = \nu^+ - \nu^-$.
  - **Hahn分解**: 存在$D \in \mathscr{F}$, 使得$$ \nu^+(A) = \nu(A \cap D),~ \nu^-(A) = \nu(A \cap D^c). $$

- **注** 3.3.5
  - 令$|\nu| = \nu^+ + \nu^-$, 称$|\nu|$为$\nu$的**变差(测度)**, 称$|\nu|(\Omega)$为$\nu$的**全变差**, 记为$\|\nu\|_{var}$. 
  - 若$|\nu|$为$\sigma$有限测度, 则称$\nu$为**$\sigma$有限符号测度**

- **命题** 3.3.6 设$\nu$为$(\Omega, \mathscr{F})$上的一符号测度. $\Omega = D \cup D^c$为其Hahn分解, 则$$ \nu(D) = \sup\{ \nu(B) | B \in \mathscr{F} \}, \nu(D^C) = \inf\{ \nu(B) | B \in \mathscr{F} \}. $$

- **定义** 3.3.7 设$\nu_1, \nu_2$为$(\Omega, \mathscr{F})$上的两个符号测度. 
  - 如果$A \in \mathscr{F}, |\nu_2|(A)=0 \Rightarrow |\nu_1|(A)=0$, 则称$\nu_1$关于$\nu_2$**绝对连续**(记为$\nu_1 \ll \nu_2$). 
  - 若$\nu_1 \ll \nu_2$且$\nu_2 \ll \nu_1$, 则称$\nu_1$与$\nu_2$**等价**.
  - 若存在$N \in \mathscr{F}$, 使得$|\nu_1|(N^c) = |\nu_2|(N) = 0$, 则称$\nu_1$与$\nu_2$**相互奇异**(记为$\nu_1 \perp \nu_2$)
  - 设$\nu$为$(\Omega, \mathscr{F})$上的一符号测度, 若$N \in \mathscr{F}$, 使得$|\nu|(N^c) = 0$, 则称$N$为$\nu$的**支撑**. 

- **注** 3.3.8
  - $\nu_1 \ll \nu_2 \iff A \in \mathscr{F}, |\nu_2|(A)=0 \Rightarrow \nu_1(A)=0 $
 - 设$\nu_1 \ll \nu_2, \nu_1 \perp \nu_2$, 则$\nu_1=0$(即对$\forall A \in \mathscr{F}$, 有$\nu_1(A)=0$).

- **引理** 3.3.9

- **定理** 3.3.10 (**Lebesgue分解**) 设$\mu$与$\nu$为$(\Omega, \mathscr{F})$上的两个$\sigma$有限符号测度, 则$\nu$有如下唯一分解(称为**Lebesgue分解**): $\nu = \nu_s + \nu_c$, 其中$\nu_s \perp \nu_c, \nu_c \ll \mu$. 此外, $\nu_s$及$\nu_c$均为$\sigma$有限的, 并且存在$N \in \mathscr{F}, g \in L$, 使得$|\mu|(N)=0, \nu_s(A) = \nu_s(A\cap N)$, $g$关于$|\mu|$的积分存在, $\nu_c$为$g$关于$\mu$的不定积分.

- **定理** 3.3.11 (**Radon-Nikodym定理**) 设$(\Omega, \mathscr{F})$为一可测空间, $\mu$为一$\sigma$有限测度, $\nu$为一符号测度(不必为$\sigma$有限). 如果$\nu$关于$\mu$绝对连续, 则存在一关于$\mu$积分存在的可测函数$g$, 使得$\nu = g\cdot\mu$. 此外, $g$在$\mu$等价意义下是唯一的(称$g_1, g_2$为$\mu$等价的, 是指$\mu([g_1 \neq g_2]) = 0$), 为要$g$是$\mu$-a.e.有限, 必须且只需$\mu$为$\sigma$有限的. 

- **定义** 3.3.12 我们用$\frac{d\nu}{d\mu}$表示定理3.3.11中的$g$(它在$\mu$等价意义下唯一确定), 并称$\frac{d\nu}{d\mu}$为$\nu$关于$\mu$的**Radon-Nikodym导数**.

- **定理** 3.3.13 

<!--- **定理** 3.3.15 (**Vitali-Hahn-Saks定理**)-->

- 注记
  - 不定积分是一类特殊的符号测度
  - [Hahn decomposition theorem](https://en.wikipedia.org/wiki/Hahn_decomposition_theorem)

## 3.4 空间$L^p$及其对偶
- 在本节中, 我们将

- **定义**

## 3.5 空间$L^\infty(\Omega, \mathscr{F})$和$L^\infty(\Omega, \mathscr{F}, m)$的对偶
