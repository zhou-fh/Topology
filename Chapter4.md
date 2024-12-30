# 第四章 分离性公理
## 4.1 $T_0$, $T_1$, $T_2(Hausdorff)$空间
**$T_0$空间：** 
设 $X$ 是一个拓扑空间, $\forall x,y\in X$, $x\neq y$,$\exist U_x$, $s.t. y\notin U_x$ 或 $\exist U_y$, $s.t. x\notin U_y$ 

**命题4.1.1：** 设$X$ 是 $T_0 $ 空间$\iff$ $x,y\in X$, $x\neq y$, 则 $\overline{\{x\}}\neq\overline{\{y\}}$.

**$T_1$空间：**
设 $X$ 是一个拓扑空间, $\forall x,y\in X$, $x\neq y$,$\exist U_x$, $s.t. y\notin U_x$.
>易知$T_1$空间是$T_0$的，反之不然
例子：$X = {0,1},\mathcal{J}=\{\varnothing,\{0\},A\}$

**命题4.1.2：**
设 $X$ 是拓扑空间, 则以下条件等价：
$(1)$ $X$是$T_1$的
$(2)$ $X$的单点集是闭集
$(3)$ $X$的有限子集是闭集

**命题4.1.3：**
设 $X$ 是 $T_1$ 的, 则 $x$ 是 $A\subset X$ 的聚点 $\iff$ $\forall U_x$, $U_x\cap A$ 是无限集。

**命题4.1.4：**
设 $X$ 是 $T_1$ 的, 则有限个点构成的序列 $\{x_i\}_{i\geq1}\in X$ 收敛于 $x\in X$ $\iff$ $\exist N$, $s.t. \forall i\geq N$, $x_i=x$.

**$T_2(Hausdorff)$空间：**
设 $X$ 是一个拓扑空间, $\forall x,y\in X$, $x\neq y$,$\exist U_x, U_y$, $s.t. U_x\cap U_y=\varnothing$.
>易知$T_2$空间是$T_1$的，反之不然
例子：无限多个点的有限补空间。

**命题4.1.5：**
$T_2$空间收敛序列只有一个收敛点。

**命题4.1.6：**
收敛序列极限点唯一的第一可数空间是$T_2$的。

---

## 4.2 正则, 正规, $T_3$, $T_4$ 空间
**集合领域：**
设 $X$ 是拓扑空间, $A,U\subset X$, $A\subset int(U)$, 则称 $U$ 是 $A$ 的领域。

**正则空间：**
设 $X$ 是拓扑空间, $x\in X$, 闭集 $A\subset X$, $x\notin A$, $\exist U_x,U_A$, $s.t. U_x\cap U_A=\varnothing$, 则称 $X$ 正则。

**命题4.2.1：**
设 $X$ 是拓扑空间, $X$ 正则$\iff$ $\forall x\in X$ 和 $x$ 的开领域 $U$, $\exist x$ 的开领域 $V$, $s.t.$ $\overline V=U$.

**正规空间：**
设 $X$ 是拓扑空间, 闭集 $A,B\subset X$, $A\cap B = \varnothing$, $\exist U_A,U_B$, $s.t. U_A\cap U_B=\varnothing$, 则称 $X$ 正规。

**命题4.2.1：**
设 $X$ 是拓扑空间, $X$ 正规$\iff$ $\forall$  闭集 $A\subset X$ 和 $A$ 的开领域 $U$, $\exist A$ 的开领域 $V$, $s.t.$ $\overline V=U$.

>正则且正规非$T_0$的例子：
$X=\{1,2,3\}$, $\mathcal{J}=\{\varnothing,\{1\},\{2,3\},\{1,2,3\}\}$

>$T_2$非正则, 非正规的例子：
$\mathbb{R}$ 的通常拓扑 $\mathcal{J}$
$K=\{\frac{1}{n}:n\in\mathbb{Z}_+\}$
$\mathcal{J}_1=\{G-E:G\in\mathcal{J},E\in K\}$
$(\mathbb{R},\mathcal{J}_1)$为例子。

**$T_3$ 空间：** 正则且$T_1$

**$T_4$ 空间：** 正规且$T_2$

**命题4.2.2：** 度量空间是$T_4$的

---

## 4.3 Uryshon引理和Tietze扩张定理

**Uryshon引理：**
设 $X$ 是一个拓扑空间, $[a,b]$ 是闭区间, 则 $X$ 正规 $\iff$ $X$ 中任意两个不交闭集 $A,B$, 存在连续的 $ f:X\to [a,b]$, 使得 $f|_A=a,f|_B=b$.

**命题4.3.1：**
设 $X$ 是 $T_4$ 的, $C$ 是 $X$ 的连通子集, $|C|>1$, 则 $C$ 是不可数集。

**引理：**
设 $X$ 是一个正规空间, $A$ 是 $X$ 的一个闭子集, $\lambda$ 是一个正实数, 则对于任何一个连续映射：$g：A\to[-\lambda,+\lambda]$, 存在着一个连续映射：$g^*:X\to[-\frac{1}{3}\lambda,+\frac{1}{3}\lambda]$, 使得对于任何的 $a\in A$, 有 $|g(a)-g^*(a)|\leq\frac{2}{3}\lambda$

**Tietze扩张定理：**
设 $X$ 是一个拓扑空间, $[a,b]$ 是闭区间, 则 $X$ 正规 $\iff$ $X$ 中不交闭集 $A$, 连续的 $ f:A\to [a,b]$, 有一个连续映射 $g:X\to[a,b]$ 是 $f$ 的扩张。

---

## 4.4 完全正则空间, Tychonoff空间
**完全正则空间：**
设 $X$ 是拓扑空间, $x\in X$, 闭集$B\subset X$, $x\notin B$, 存在一个连续映射 $f:X\to[0,1]$, 使得 $f(x)=0$, $f|_B=1$, 则称 $X$ 是完全正则空间。

**Tychonoff空间：** 完全正则的$T_1$空间

**命题4.1.1：** 完全正则空间是正则的。

> Tychonoff空间是$T_3$的。
$T_4$空间是Tychonoff的。

**命题4.1.2：** 正则且正规的空间是完全正则空间。

**Tychonoff定理：** 正则的$Lindel{\"o}f$ 空间是正规的。

---

## 4.5 分离性公理的性质

**性质4.5.1：** 都有拓扑不变性

**性质4.5.2：** 除了正规和$T_4$都有遗传性质,这两个有闭子空间遗传性质。

**性质4.5.3：** 除了正规和$T_4$都有可积性质

---

## 4.6 可度量化空间

