# 离散数学第二次小测复习



[TOC]

<!--more-->

## Set Theory

extension（外延）：像是列举法

intension（内涵）:像是描述法

empty set :空集

universal set :全集

Cardinality : 基数

​		Card(A): the number of elements of set A

几个概念:

| 概念名               | 中文                | 符号                           |
| -------------------- | ------------------- | ------------------------------ |
| equivalent           | 相等                | $=$                            |
| subset               | 子集                | $\subseteq$                    |
| proper-subset        | 真子集              | $\subset$                      |
| not subset           | 不是子集            | $\nsubseteq$                   |
| union                | 并集                | $\bigcup$                      |
| intersection         | 交集                | $\bigcap$                      |
| difference           | 差集                | $-$                            |
| complement           | 余集（A的绝对补集） | $A^{c}=E\textbackslash{A}$     |
| symmetric difference | 对称差              | $A\oplus{B}=(A-B)\bigcup(B-A)$ |

a family of sets 集合族：A is a family set of sets over S if each element in A is a subset of S.

$\bigcup{A}$：A的广义并：$\bigcup{A}=\{x:(\exist{z})(z\in{A}\and{x\in{z})}\}$

$\bigcap{A}$：A的广义交：$\bigcap{A}=\{x:(\forall{z})(z\in{A}\rightarrow{x\in{z}})\}$

*注：$\bigcap{\empty}$ is undefined while $\bigcup{\empty}=\empty$ 

power set :幂集

相关结论：

(1) $A \subseteq B \Leftrightarrow 2^A \subseteq 2^B$  

(2) $2^A \in 2^B \Rightarrow A \in B$：$\Leftarrow$的反例：

(3) $2^A \cap 2^B=2^{A \cap B}$

(4) $2^A \cup 2^B \subseteq 2^{A \cup B}$：（比如$A=\{1,2,3,4\}$$B=\{1,2,5,6\}$很显然$2^A \cup 2^B$ 和$2^{A \cup B}$不一样大

Transitive Set(传递集):![quicker_1cf7e292-61f2-4aaf-8bae-57df5b3094c0.png](http://p.ananas.chaoxing.com/star3/origin/bcae765b8c29d1c23c42f70acd260bfd.png?rw=994&rh=133&_fileSize=31386&_orientation=1)

相关性质：![quicker_4432c48c-ef1d-4f48-a985-914a8f0843bf.png](http://p.ananas.chaoxing.com/star3/origin/e92e294504db0cf0987faa55c5888b0f.png?rw=860&rh=142&_fileSize=32925&_orientation=1)

[证明](http://p.ananas.chaoxing.com/star3/origin/70105befe931e2fc9364b5ad7ec31c5a.png?rw=1127&rh=683&_fileSize=171067&_orientation=1)

## 有序对:

1.$\langle x, y\rangle:=\{\{x\},\{x, y\}\}$

2.$\langle a, b, c, d\rangle=\langle\langle a, b, c\rangle, d\rangle=\langle\langle\langle a, b\rangle, c\rangle, d\rangle$

3.Cartisian Product (笛卡尔积) 

4.![quicker_c403fe6c-abf0-4c2b-94da-4f6d126c10ea.png](http://p.ananas.chaoxing.com/star3/origin/77f66ade0f9d64420fd0504ccf2984f7.png?rw=1092&rh=99&_fileSize=24497&_orientation=1)

5.$A \times B \subseteq C \times D$ iff $A \subseteq C$ and $B \subseteq D$ [Proof](http://p.ananas.chaoxing.com/star3/origin/72fdb929a0cd64ff1f5091c3e947cb32.png?rw=1049&rh=327&_fileSize=61937&_orientation=1)

## 关系

1.<a,b>$\in$R $\Leftrightarrow$aRb

2.Identity Relation（恒等关系）：

3.Universal Relation（全域关系）：

4.Empty Relation（空关系）：

5.$\operatorname{fld}(R)=\bigcup \bigcup R$ --[证明](http://p.ananas.chaoxing.com/star3/origin/1b9a4ccb6fa8359b8b30ca157ff66492.png?rw=1067&rh=242&_fileSize=73895&_orientation=1)

6.某个关系的一些运算：

| 运算        | 汉译 | 含义                                                         |
| ----------- | ---- | ------------------------------------------------------------ |
| converse    | 逆   | $R^{-1}=\{\langle x, y\rangle:\langle y, x\rangle \in R\}$   |
| restriction | 限制 | $R \mid A=\{\langle x, y\rangle:\langle x, y\rangle \in R \wedge x \in A\}$ |
| image       | 象   | $R[A]=\{y:(\exists x)(x \in A \wedge\langle x, y\rangle \in R)\}$ |
| composite   | 合成 | $S \circ R=\{\langle x, z\rangle:(\exists y)(\langle x, y\rangle \in R \wedge\langle y, z\rangle \in S)\}$ |

7.结论

(1) $R \circ(S \cup W)=(R \circ S) \cup(R \circ W)$
(2) $(R \cup S) \circ W=(R \circ W) \cup(S \circ W)$
(3) $R \circ(S \cap W) \subseteq(R \circ S) \cap(R \circ W)$
(4) $(R \cap S) \circ W \subseteq(R \circ W) \cap(S \circ W)$

8.关系的一些性质：

| 性质          | 汉译   | 等价条件                           |
| ------------- | ------ | ---------------------------------- |
| reflexive     | 自反的 | $I_{A}\subseteq{R}$                |
| inreflexive   | 反自反 | $I_{A}\bigcap R=\empty$            |
| symmetric     | 对称   | $R^{-1}\subseteq R$ iff $R^{-1}=R$ |
| antisymmetric | 反对称 | $R\bigcap R^{-1}=I_A$              |
| transitive    | 传递   | $R\circ R\subseteq R$              |

性质：---[proof](http://p.ananas.chaoxing.com/star3/origin/c12d561f1b486b93d04007b5e509d4c5.png?rw=1081&rh=235&_fileSize=75644&_orientation=1)

(1) If $R_1, R_2 \subseteq A \times A$ are reflexive, then $R_1^{-1}, R_1 \cap R_2, R_1 \cup R_2$ are reflexive.
(2) If $R_1, R_2 \subseteq A \times A$ are symmetric, then $R_1^{-1}, R_1 \cap R_2, R_1 \cup R_2$ are symmetric.
(3) If $R_1, R_2 \subseteq A \times A$ are transitive, then $R_1^{-1}, R_1 \cap R_2$ are transitive.
(4) If $R_1, R_2 \subseteq A \times A$ are antisymmetric, then $R_1^{-1}, R_1 \cap R_2$ are antisymmetric.

## 闭包

| 类型               | 汉译     | 构造方法                                   | 表示   |
| ------------------ | -------- | ------------------------------------------ | ------ |
| reflexive closure  | 传递闭包 | $R\bigcup I_A$                             | $r(R)$ |
| symmetric closure  | 对称闭包 | $R\bigcup R^{-1}$                          | $s(R)$ |
| transitive closure | 传递闭包 | $\displaystyle\bigcup_{n=1}^{\infty}{R^n}$ | $t(R)$ |

性质：[proof](http://p.ananas.chaoxing.com/star3/origin/4e476af15a5cf6fb500c3ac2a5a1cd7e.png?rw=1125&rh=479&_fileSize=128359&_orientation=1)

(1) If $R$ is symmetric/reflexive/transitive, then $s(R)=R$ or $r(R)=R$ or $t(R)=R$.
(2) If $R_1 \subseteq R_2$, then $r\left(R_1\right) \subseteq r\left(R_2\right), s\left(R_1\right) \subseteq s\left(R_2\right)$ and $t\left(R_1\right) \subseteq t\left(R_2\right)$
(3) $r\left(R_1\right) \cup r\left(R_2\right)=r\left(R_1 \cup R_2\right)$
(4) $s\left(R_1\right) \cup s\left(R_2\right)=s\left(R_1 \cup R_2\right)$
(5) $t\left(R_1\right) \cup t\left(R_2\right) \subseteq t\left(R_1 \cup R_2\right)$

more: [proof](http://p.ananas.chaoxing.com/star3/origin/807e0c650d338f7b8e783684c59d585b.png?rw=1095&rh=649&_fileSize=109427&_orientation=1)

(1) If $R$ is reflexive, then $s(R)$ and $t(R)$ are also reflexive.
(2) If $R$ is symmetric, then $r(R)$ and $t(R)$ are also symmetric.
(3) If $R$ is transitive, then $r(R)$ is also transitive.

other:

(1) $r(s(R))=s(r(R))$
(2) $r(t(R))=t(r(R))$
(3) $s(t(R)) \subseteq t(s(R))$

## 等价关系：Equivalence Relation

1.一些概念

| 概念              | 汉译     | 含义                                                         | 符号                                  |
| ----------------- | -------- | ------------------------------------------------------------ | ------------------------------------- |
| equivalence class | 等价类   | [~~~~](http://p.ananas.chaoxing.com/star3/origin/a6f67fc83523ae1fde47c66d440dc9c6.png?rw=1081&rh=228&_fileSize=66099&_orientation=1) | $[x]_R=\{y: y \in A \wedge x R y\}$   |
| quotient set      | 商集     |                                                              | $A / R=\left\{[x]_R: x \in A\right\}$ |
| partition         | 划分     | [~~~~](http://p.ananas.chaoxing.com/star3/origin/f158b8db51c5b17af7d8498bcb5e8bbb.png?rw=1003&rh=97&_fileSize=30901&_orientation=1) |                                       |
|                   | 相容关系 | 自反且对称                                                   |                                       |

## 相容关系：Tolerance Relation

1.reflexive and symmetric

2.tolerance class 相容类

3.maximal tolerance class 最大相容类

## 覆盖：cover

1. [definition](http://p.ananas.chaoxing.com/star3/origin/141405140a5f74525bc22f9433d0a2e8.png?rw=1076&rh=185&_fileSize=30348&_orientation=1)

## 偏序： Partial Order

1.poset 偏序集 ：$<A,R>$ 

2.we say y covers x if :

$(x \leq y) \wedge(x \neq y) \wedge \neg(\exists z)(z \in A \wedge x \leq z \wedge z \leq y \wedge z \neq x \wedge z \neq y)$

3.$\operatorname{cov}_R(A)=\{\langle x, y\rangle \in R: y$ covers $x\}$

4.Hasse Diagram(哈斯图)

5.一些概念 (都是一些元素)

- the least element (最小元) of $B$ if $(\forall y)(y \in B \rightarrow x \leq y)$

- the greatest element (最大元) of $B$ if $(\forall y)(y \in B \rightarrow y \leq x)$
- a minimal element (极小元) of $B$ if $(\forall y)(y \in B \wedge y \leq x \rightarrow x=y)$
- a maximal element (极大元) of $B$ if $(\forall y)(y \in B \wedge x \leq y \rightarrow x=y)$
- the upper bound (上界) of $B$ if $(\forall y)(y \in B \rightarrow y \leq x)$
- the lower bound (下界) of $B$ if $(\forall y)(y \in B \rightarrow x \leq y$ )
- least upper bound (最小上界/上确界)  
- greatest lower bound (最大下界/下确界)  

## 函数：[Function](http://p.ananas.chaoxing.com/star3/origin/47f8cfa1784184d521b6d7ad2acb8f07.png?rw=780&rh=144&_fileSize=28738&_orientation=1)

1. 

| total function       | 全函数       |
| -------------------- | ------------ |
| **partial function** | **部分函数** |

2. [写法](http://p.ananas.chaoxing.com/star3/origin/036a4f56b2f4f2d94c2dae8164a8bd3b.png?rw=1038&rh=185&_fileSize=49943&_orientation=1)：$f: A \rightarrow B, f: x \mapsto y$
3. all functions from A to B: $A_B =\{f:(f : A \rightarrow B)\}$  
4. Indicator Function (特征函数): Let $A \subseteq E$. Then $\mathcal{X}_A: E \rightarrow\{0,1\}$ is defined by $\mathcal{X}_A(x)=1$ iff $x \in A$.
5. - injection (单射): if $\left(\forall x_1 \in A\right)\left(\forall x_2 \in A\right)\left(x_1 \neq x_2 \rightarrow f\left(x_1\right) \neq f\left(x_2\right)\right)$
   - surjection (满射) : if $\operatorname{ran}(f)=B$
   - bijection (双射): if it is both an injection and a surjection.

6. only when f is a bijection, we have that $f^{-1} : B \rightarrow A$ is a function, and we call $f^{-1}$ the inverse function (逆函数)  

7. (1) If $f$ and $g$ are bijections (respectively, injections or surjections), then $f \circ g$ is also a bijection (respectively, injection or surjection).
   (2) If $f \circ g$ is a surjection, then $f$ is a surjection.
   (3) If $f \circ g$ is an injection, then $g$ is an injection.
   (4)IF $f \circ g$ is an bijection, then $f,g$ are both bijections.

## 基数和等势

1.the cardinality (基数) of A: $|A|$ or card(A)  :the number of element in A

2.无穷的大小：

- $|\mathbb{N}|=\aleph_0$, where $\aleph_0$ is called the Aleph Zero (阿列夫零);
- If $\left|A_k\right|=\aleph_k$, then $\left|2^{A_k}\right|=\aleph_{k+1}$, where $\aleph_k$ is called the Aleph $k$ (阿列夫 $k$ ).

3.dominated（支配）：A is dominated by B means $A\preceq B$ 

​	we say $A\prec B$ : if $A \preceq B$ and $A\not\approx B $

4.Theorem: Schröder-Berstein's Theorem
If $A \preceq B$ and $B \preceq A$, then $A \approx B$.

5.for any set A, we have $A\not\approx2^{A}$

6.$2^{\N}\approx \R$

