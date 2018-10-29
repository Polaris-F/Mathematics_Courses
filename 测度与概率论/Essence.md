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
- **定理** 3.2.5 (控制收敛定理)
## 3.2 积分号下取极限
## 3.3 不定积分与测度符号
## 3.4 空间$L^p$及其对偶
## 3.5 空间$L^\infty(\Omega, \mathscr{F})$和$L^\infty(\Omega, \mathscr{F}, m)$的对偶