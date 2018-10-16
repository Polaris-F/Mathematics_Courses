# 第二章 可测映射
## 2.1 定义及基本性质
- 在本节中, 我们将会
  - 定义可测映射

- 定义
  - 设$(\Omega, F)$和$(E, \mathscr{E})$是两个可测空间. $f: \Omega \rightarrow E$, 如果对一切$A \in \mathscr{E}$有$f^{-1}(A) \in F$, 则称$f$为F可测映射. 记$f^{-1}(\mathscr{E}) = \{ f^{-1}(A) | A\in\mathscr{E} \}$. 则$f$为F可测映射 $\iff$ $f^{-1}(\mathscr{E}) \subset F$
  - 令$\bar{\Re} = \Re \cup \{-\infty, +\infty\}$. $B(\bar{\Re})$为$\bar{\Re}$上的Borel $\sigma$代数.
  - 令$(\Omega, F)$为一可测空间. $f: \Omega \rightarrow \bar{\Re}$, 若$f^{-1}(\bar{\Re}) \subset F$, 则称f为**数值可测函数**, 或**Borel可测函数**. $f: \Omega \rightarrow \bar{\Re}$, 若$f^{-1}(\Re) \subset F$, 则称f为**实值可测函数**

- **命题**: 设$(\Omega, F)$和$(E, \mathscr{E})$是两个可测空间, $C \subset \mathscr{E}$, 满足$\sigma(C) = \mathscr{E}$. 若$f^{-1}(C) \subset F$, 则f可测.