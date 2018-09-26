---
title: 'Measure and Probability Theory'
date: 2018-09-25
permalink: /posts/2018/09/measure-theory/
tags:
  - Mathematics
---

- 课程名称: 测度与概率论
- 教材: 《测度论讲义》(第二版) 严加安著

<!--![](measure-theory.jpg)-->

# 第一章 集类与测度
## 1.1 集合运算与集类
- $\Omega$: 给定的非空集合(全空间)
- **集类**: 以$\Omega$的某些子集为元素的集合称为($\Omega$上的)集类
- **单调列**: 设$\{A_n, n\geq1\}$为一集合序列, 若$\forall n \geq 1$, 有$A_n \subset A_{n+1}$(相应地, $A_n \supset A_{n+1}$), 则称$(A_n)$**单调增**(相应地, **单调减**). 令$A=\cup_n A_n$或$A=\cap_n A_n$, 称 $A$为$(A_n)$的极限, 记为$A_n \uparrow A$或$A_n \downarrow A$
- **集合的极限**: 对一般的集列$(A_n)$, 令
  - **上极限**: $\lim\limits_{n\rightarrow\infty}\sup A_n = \overline{\lim}\limits_{n\rightarrow\infty} A_n = \cap_{n=1}^\infty \cup_{k=n}^\infty A_k$
  - **下极限**: $\lim\limits_{n\rightarrow\infty}\inf A_n = \underline{\lim}\limits_{n\rightarrow\infty} A_n = \cup_{n=1}^\infty \cap_{k=n}^\infty A_k$
  - 易证:  
$\overline{\lim}\limits_{n\rightarrow\infty} A_n = \{ \omega ~|~ \forall~ n\geq1, \exists~ k(n) \geq n, ~s.t.~ \omega \in A_{k(n)} \}$   
$\underline{\lim}\limits_{n\rightarrow\infty} A_n = \{ \omega ~|~ \exists~ n\geq1, \forall~ k \geq n, ~s.t.~ \omega \in A_k \}$  
$\underline{\lim}\limits_{n\rightarrow\infty} A_n \subset \overline{\lim}\limits_{n\rightarrow\infty} A_n$.  
上述关于集合极限的等价定义比原始定义更易理解.
  - 若 $\overline{\lim}\limits_{n\rightarrow\infty} A_n = \underline{\lim}\limits_{n\rightarrow\infty} A_n$, 则称集列$(A_n)$的极限存在, 用$\lim\limits_{n\rightarrow\infty}A_n$表示.
  - 例子: $A_1=\{0\}, A_2=\{2\}, A_n=\{(-1)^n\}~(n\geq3)$, 则$\overline{\lim}\limits_{n\rightarrow\infty} A_n = \{1, -1\}, \underline{\lim}\limits_{n\rightarrow\infty} A_n = \emptyset $
  - 例子: $A_1=\{1\}, A_2=[2,3], A_n=[-1, \frac{1}{n}]~(n\geq3)$, 则$\overline{\lim}\limits_{n\rightarrow\infty} A_n = [-1,0], \underline{\lim}\limits_{n\rightarrow\infty} A_n = [-1,0] $
- 集合的划分
  - 若$(A_n)$两两不相交(即$A_m \cap A_n = \emptyset, \forall m \neq n$), 则常用$\sum_n A_n$表示$\cup_n A_n$
  - 若$\sum_n A_n=\Omega$, 则称$(A_n)$为$\Omega$的一个**划分**
  - 对任一集列$(A_n)$, 令$B_1=A_1, B_n = A_nA_{n-1}^c \cdots A_1^c~ (n\geq2)$, 可以证明$(B_n)$两两不相交, 且$\cup_n B_n = \cup_n A_n$ (*此处暂省去证明*)
- **常用集类**
  - $\pi$类: 对有限交封闭
  - 半环
  - 半代数
  - 代数(或域): $\Omega \in C, \emptyset \in C$, 对有限交封闭, 对取余集封闭 (由此推知,对有限并和差运算也封闭)
  - $\sigma$代数: $\Omega \in C, \emptyset \in C$, 对可列交封闭, 对取余集封闭 (由此推知,对可列并和差运算也封闭)
  - 单调类: 对单调序列极限封闭
  - $\lambda$类: $\Omega \in C$, 对差运算封闭, 对单调增序列极限封闭
  - 易证: 

- 评论
  - 上这门课的目的, 是想对概率论有更深的认识. 第一节课下课问了下老师教学计划, 结果发现这门课可以改叫《测度论》了.
  - **集合**作为现代数学最基本的概念之一, 真是无处不在啊!
  - [这里](https://math.stackexchange.com/questions/476159/limits-of-sequences-of-sets)有一个关于集合极限很好的解释. 从直观上解释了我们为什么要引入集合的上下极限的概念?
  - **有限**的概念我们在日常生活中接触很多, 但**可数**的概念就需要引入极限, 从**有限**到**可数**是一个很大的跨度.

## 1.2 单调类定理






## 1.3 测度与非负集函数




## 1.4 外测度与测度的扩张







