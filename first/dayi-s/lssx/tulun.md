# Graph Theory

[TOC]

## Basic Definitions

1. $G=\langle V, E, \mathcal{E}\rangle$ $V=\{v_1,\cdots,v_n\}$ $E=\{e_1,e_2,\cdots,e_m\}$ 

   >1. 对于不同种类的图可以适当简化。
   >
   >2. 有时，我们写$G=<V,E>$ 边与点的连接关系由图直观的表现出来

2. special graphs:

   > - empty graph：no edges
   > - complete graph: each pair of vertices are connected

3. 一些概念：

   > - adjacent:相邻的
   >
   > - edge $e$ is incident（关联）with $v$ and $v'$
   >
   > - $e=<v,v'>$, v is predecessor（前驱）,$v'$ is successor（后继）
   >
   > - degree：out-degree + in-degree(directed)
   >
   > - $\displaystyle\sum_{v\in V}d(v)=2m(m是总边数)$
   >
   > - 对于有向图：出度和=入度和
   >
   > - sub-graph：子图；sub-graph induced by $V'$：由$v'$生成的诱导子图
   >

4. isomorphic：同构 $\text { denoted by } G_1 \cong G_2$

   >关键：找双射
   >
   >几个必要条件：
   >
   >- $\left|V_1\right|=\left|V_2\right|$ and $\left|E_1\right|=\left|E_2\right|$.
   >2. The non-increasing sequences of vertices degrees of $G_1$ and $G_2$ are the same.（度相同）
   >3. For any induced graph of $G_1$, there is an induced sub-graph of $G_2$ such that these two induced sub-graphs are isomorphic.（腰斩后都相同）
   >
   >口诀：大图找小图，小图找度

5. path（道路）：

   > - simple path: no repeated edges
   > - elementary path: no repeated vertices
   > - circuit：回路

6. connected(连通的)

   > - connected component: 连通分支
   > - strongly connected(for directed graph): 强连通的——考虑方向的连通

7. 欧拉回路与欧拉道路：

   > - 欧拉回路:a **simple** circuit containing all edges.
   >
   > - 欧拉道路
   >
   > - A connected pseudo-graph $G=\langle V, E\rangle$ has an Euler circuit $\Leftrightarrow \forall v \in V: d(v)$ is even
   >
   > - A connected pseudo-graph $G=\langle V, E\rangle$ has an Euler path if and only if
   >   $$
   >   \mid\{v \in V: d(v) \text { is odd }\} \mid \leq 2
   >   $$
   >   
   > - [directed](http://p.ananas.chaoxing.com/star3/origin/c143922b6034eb4bcc3f8c70bbc10fd8.png?rw=1075&rh=425&_fileSize=92530&_orientation=1)
   >
   > - 找法：不走割边/桥
   >

8. 哈密顿回路与哈密顿道路

   > - elementary circuit or path
   > - np-Hard 问题
   > - 几个充分条件：
   >   - Lemma: 
   >     Let $P=v_1 v_2 \cdots v_l$ be a maximal elementary path. If $d\left(v_1\right)+d\left(v_l\right) \geq l$, then there must exist an elementary circuit that passes through $v_1, v_2, \cdots, v_l$.
   >   - theorem:Sufficient Condition for Hamilton Path
   >     a simple-graph $G = \left( V , E \right)$ has a Hamilton path if 
   >     $\forall u, v ^ { \prime } \in V : d \left( v \right) + d \left( v ^ { \prime } \right) \geqslant n - 1$
   >   - theorem:Sufficient Condition for Hamilton Circuit
   >     a simple-graph $G = \left( V , E \right)$ has a Hamilton circuit if 
   >     $\forall u, v ^ { \prime } \in V : d \left( v \right) + d \left( v ^ { \prime } \right) \geqslant n$

## Trees

1. 几个等价定义：

   >  $T=\langle V, E\rangle$
   > (1) $T$ is a connected and $|E|=|V|-1$;
   > (2) $T$ has no circuit and $|E|=|V|-1$;
   > (3) $T$ is connected and each edge is a bridge;
   > (4) $T$ has no circuit and by adding any edge, we will have a circuit;
   > (5) the path between any two vertices is unique.

2. 几个概念：

   > 1.vertices with degree one leaves (树叶). 
   >
   > 2.Disconnected graphs with no circuit are called forest (森林).  

3. Theorem:

   > (1) For tree $T$ w ith $|V| \geq 2$, there are at least two leaves,
   >
   > (2) For forest $F$ with $|V|=n$ and $k$ connected components, we have $|E|=n-k$.

4.  Spanning Trees（生成树）
   A sub-graph of $G$ is called a spanning tree (生成树) of $G$ if 

   > (i) it is a tree; and 
   >
   > (ii) it contains all vertices of $G$.

5. Depth-First Search (深度优先搜索)  

   > (i) keep adding new edges until no edge can be
   > added
   >
   > (ii) track back to the vertice at which some edge can be added, and repeat.  

6. Breadth-First Search (广度优先搜索)  

   > - start from a vertex 
   >
   > - at the kth iteration, add all vertices that are k-close to the initial vertex.   

7. weighted graph (加权图) 

   > - The weight of a graph, denoted by w(G)  
   > - a minimum spanning tree (最小生成树) T is spanning tree such that, for any spanning tree T′, we have $w(T) ≤ w(T')$  
   > - Kruskal’s Algorithm: ![quicker_320a5c19-9315-49bc-abe9-f56c612a3333.png](http://p.ananas.chaoxing.com/star3/origin/984f947d0e1ae23d5c56d4ff80484ce5.png?rw=1085&rh=472&_fileSize=77029&_orientation=1)
   > - Prim’s Algorithm![quicker_b06dfd16-f9fe-46d1-af16-613a22e2ab06.png](http://p.ananas.chaoxing.com/star3/origin/3cd8ef27cc9f93d0258adde8cb3f656e.png?rw=1091&rh=520&_fileSize=77356&_orientation=1)
