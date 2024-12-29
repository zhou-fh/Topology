# 拓扑空间与连续映射
## 1.1 拓扑空间的定义
**度量公理：**
设$X$是非空集合,$d：X\times X\rightarrow \R,\forall x,y,z\in X$,有
$(1)$ (正定性) $d(x,y)\geq0,d(x,y)=0\Leftrightarrow x = y$ 
$(2)$ (对称性) $d(x,y) = d(y,x)$
$(3)$ (三角不等性) $d(x,y) \leq d(x,z)+d(y,z)$
则称$d$为$X$的一个度量。

**开集公理：**
设$X$是一个非空集合,$\mathcal{J}\subset X$，如果：
$\left(1\right)X,\varnothing\in\mathcal{J}$
$\left(2\right)A,B\in\mathcal{J}$,则$A\cap B\in\mathcal{J}$
$\left ( 3\right )$设$\mathcal{J}_1\subset \mathcal{J}$, 则 $\cup _{A\in \mathcal{J}_1}A\in \mathcal{J}$
则称$\mathcal{J}$为$X$的一个拓扑。

**拓扑空间与开集的定义：**
设$X$是一个非空集合,$\mathcal{J}\subset X$,如果 $\mathcal{J}$ 满足开集公理，则称  $\mathcal{J}$ 为 $X$ 的一个拓扑,  $\mathcal{J}$ 中的元是$X$上的开集，$(X, \mathcal{J})$ 是拓扑空间。

**问题1.1.1:** 对于一个非空集合$X$，只有一个拓扑吗？（答案显然是NO）
>例：设$X$是一个非空集合：
$\left(1\right)\mathcal{J}=2^X(幂集)\rightarrow $ 离散拓扑空间
$\left(2\right)\mathcal{J}=\{\varnothing,X\}\rightarrow $ 平凡拓扑空间
$\left(3\right)\mathcal{J}=\{\varnothing,A,A^{c},X\}(A\subset X,A\neq\varnothing)$

>一些拓扑的符号： $\mathcal{J}_{e}$ (欧氏拓扑)，$\mathcal{J}_d$（度量拓扑）


****************

## 1.2 拓扑空间中的点集
**由开集诱导出的一系列定义**
设$(X,\mathcal{J})$是拓扑空间，
**领域：** $x\in X$，$U\subset X$，如果存在开集$V$，使得$x\in V\subset U$，则称 $U$ 是 $x$ 的领域。
**内点：** $x\in X$，如果存在 $x$ 的领域$U$，使得$U\cap X^c = \varnothing$，则称 $x$ 是 $X$ 的内点。
**内部：** 全体内点构成的集合，记作 $int(E)$。
**聚点：** $x\in X$，如果任取 $x$ 的领域$U$，使得$U\cap (X-\{x\}) \neq \varnothing$，则称 $x$ 是 $X$ 的聚点。
**导集：** 全体聚点构成的集合,记作 $d(E)$。
**孤立点：**$x\in X$，如果存在 $x$ 的领域$U$，使得$U \cap \left(X-\{x\}\right) = \varnothing$，则称 $x$ 是 $X$ 的孤立点。
**边界点：**$x\in X$，如果任取 $x$ 的领域$U$，使得$U\cap X\neq \varnothing$ 且 $U\cap X^c\neq \varnothing$，则称 $x$ 是 $X$ 的聚点。
**边界：** 全体边界点构成的集合,记作 $\partial(E)$。
**闭包：** 集合和其导集的并，记作 $\overline E$。
**闭集：** 补集是开集的集合。

**点集的一些性质:**
$\left(1\right)V\in \mathcal{J} \Leftrightarrow \forall x\in V$，$V$ 是 $x$ 的领域。 
$\left(2\right)E$ 是闭集$\Leftrightarrow d(E)\subset E$。
$\left(3\right)$ 集合的内部是含于集合最大的开集，集合的闭包是包含集合小的最闭集。

由拓扑空间中的点集，可以定义以下两种拓扑：
>**有限补拓扑**
设$X$是非空集合，设$X$的子集$\mathcal{J} = \{ \varnothing \}\cup\{A\subset X: A^c$是有限集$\}$，易证$\mathcal{J}$是$X$的拓扑，称$\mathcal{J}$为$X$的有限补拓扑，称$(X,\mathcal{J})$为有限补拓扑空间。
**可数补拓扑**
设$X$是非空集合，设$X$的子集$\mathcal{J} = \{ \varnothing \}\cup\{A\subset X: A^c$是可数集$\}$，易证$\mathcal{J}$是$X$的拓扑，称$\mathcal{J}$为$X$的可数补拓扑，称$(X,\mathcal{J})$为可数补拓扑空间。

**连续映射的定义:**
设$X$和$Y$是两个拓扑空间,$f:X\rightarrow Y$,如果$Y$中每一个开集$U$的原像$f^{-1}(U)$是中$X$的开集,则称$f$连续.

**同胚的定义:**
设$X$和$Y$是两个拓扑空间,如果$f:X\rightarrow Y$是一个双射，并且$f$和$f^{-1}$连续,则称$f$是一个同胚映射，称$X$和$Y$同胚.
>同胚是一个等价关系.

>由此提出**拓扑学的研究内容：**
$(1)$ 判断两个拓扑空间是否同胚
$(2)$ 可度量化空间

## 1.3 映射诱导拓扑
由连续映射，我们可以诱导出以下拓扑：
$(1)$ 设$X$是一个非空集合,$Y$是一个拓扑空间,$f:X\rightarrow Y$,给$X$定义一个极小拓扑,$\mathcal{J}=\{f^{-1}(V):V\in\mathcal{J}_Y\}$,使得$f$连续.
$(2)$ 设$X$是一个拓扑空间,$Y$是一个非空集合,$f:X\rightarrow Y$,给$Y$定义一个极大拓扑$\mathcal{J}=\{V:f^{-1}(V)\in\mathcal{J}_X\}$,使得$f$连续.

以上两个命题易证,由此可引出以下空间的拓扑：
**子空间拓扑** 
 设$X$是一个拓扑空间,$A\subset X$,定义包含映射：
 $i:A\rightarrow X,i(x) = x,x\in A.$
 则使$i$连续的$A$的极小拓扑为$\mathcal{J}=\{i^{-1}(V):V\in\mathcal{J}_X\}=\{V\cap A:V\in\mathcal{J}_X\}$,
 则称$(A,\mathcal{J})$为$X$的拓扑子空间,$\mathcal{J}$为$A$关于$X$的子空间拓扑.
 >子空间拓扑的性质：
 $(1)U\in\mathcal{J}_A\Leftrightarrow\exist\ V\in\mathcal{J}_X,s.t.\ U=V\cap A.$
 $(2)U$是$A$的闭子集$\Leftrightarrow\exist \ X$的闭子集$V,s.t.\ U = V\cap A.$
 $(3)$(遗传性质)设$A\subset B\subset X,$则$A$关于$X$的子空间拓扑 $=A$ 关于的$B$子空间拓扑.<a name="遗传性质"></a>
 >>证明：$(1),(2)$由子空间拓扑的定义易得.
 $(3):\mathcal{J}_A^B=\{V\cap A:V\in\mathcal{J}_B\}=\{V\cap B\cap A:V\in\mathcal{J}_X\}=\{V\cap A:V\in\mathcal{J}_X\}=\mathcal{J}_A^X.$
 

**乘积空间拓扑**
设$X_1$和$X_2$是两个拓扑空间,投影映射$\rho_i = X_1\times X_2\rightarrow X_i,i=1,2.$则使投影映射$\rho_1,\rho_2$连续的极小拓扑的拓扑子基为$\mathscr{S}=\{U\times V:U\in\mathcal{J}_{X_1},V\in\mathcal{J}_{X_2}\}.$
>**命题 1.3.1：**
设$X,Y,Z$为拓扑空间，则$f:X\to Y\times Z$连续$
\Leftrightarrow \rho_1\circ f,\rho_2\circ f$连续

>**命题 1.3.2**
设$X,Y,Z$为拓扑空间,则$(X\times Y)\times Z$与$X\times Y\times Z$同胚.

**商空间拓扑**
设$X$拓扑空间,$\sim$为$X$上的一个等价关系,$X/_\sim$是商集,映射$\pi:X\to X/_\sim$,则使映射$\pi$连续的极大拓扑为$\mathcal{J}=\{V\in X/_\sim:\pi^{-1}(V)\in\mathcal{J}_X\}.$
>**命题 1.3.3**
设$X$和$Y$为拓扑空间,映射$f:X\to Y$满射,由此定义等价关系$\sim$,则$X/_\sim$与$Y$同胚.

## 1.4 拓扑基与拓扑子基

**拓扑基的定义：**
设$X$是拓扑空间,$\mathscr{B}\subset X$,如果:
$(1)\cup_{B\in\mathscr{B}}B=X.$
$(2)\forall B_1,B_2\in\mathscr{B},\forall x\in B_1\cap B_2,\exist B\in \mathscr{B}, s.t.\ x\in B \subset B_1 \cap B_2.$
则称$\mathscr{B}$为$X$的一个拓扑基.
>$(2)$的等价描述：
$\forall B_1,B_2\in \mathscr{B},\exist\mathscr{B}_1\subset\mathscr{B},s.t.\ B_1\cap B_2 = \cup_{B\in\mathscr{B}_1}B.$

>**定理 1.4.1：**
设$\mathscr{B}$是拓扑空间$X$的开集族,$\mathscr{B}$是的一个基$\iff$对于每一个$x$和$x$的每一个领域$U_x,\exist V_x\in \mathscr{B},s.t. \ V_x\subset U_x.$

>**生成拓扑：**
设$X$是非空集合,$\mathscr{B}$为$X$的一个拓扑基,设$X$的子集$\mathcal{J} = \{ \varnothing \}\cup\{A\subset X: \exist\mathscr{B}_A\subset\mathscr{B},s.t.\ A = \cup_{B\in\mathscr{B}_A}B\}$，易证$\mathcal{J}$是$X$的拓扑，称$\mathcal{J}$为$\mathscr{B}$生成的拓扑.

**拓扑子基的定义**
设$X$是拓扑空间,$\mathscr{S}\subset X$,如果: $\cup_{S\in\mathscr{S}}S=X.$
则称$\mathscr{S}$为$X$的一个拓扑子基.

>**生成拓扑基：**
设$X$是非空集合,$\mathscr{S}$为$X$的一个拓扑子基,设$X$的子集$\mathscr{B} =\{S_1\cap S_2\cap\cdots\cap S_n：S_j\in\mathscr{S},0\leq j\leq n\}$,易证$\mathscr{B}$是$X$的拓扑基,称$\mathscr{B}$为$\mathscr{S}$生成的拓扑基,由$\mathscr{B}$生成的拓扑也称为由$\mathscr{S}$生成的拓扑.

>**命题1.4.1:**
设$X$和$Y$是两个拓扑空间,$Y$的拓扑由子基$\mathscr{S}$生成,$f:X\rightarrow Y$,则$f$连续$\Leftrightarrow\forall V\in \mathscr{S},f^{-1}(V)\in\mathcal{J}_X$.
>>证明：
"$\Rightarrow:$" 由连续的定义,易证.
"$\Leftarrow:$" $\forall\  U\in\mathcal{J}_Y,\ \exist\ \mathscr{B}_U\subset\mathscr{B}_Y,s.t.\ U = \cup_{B\in\mathscr{B}_U}B.$
$\forall \ B\in \mathscr{B}_U$,又$\mathcal{J}_Y$由$\mathscr{S}$生成,则 $\exist\{S_i\}_{0\leq i\leq n}\subset\mathscr{S},s.t. \ \cap_{i=0}^{n} S_i = B.$
又$f^{-1}(S_i)\in\mathcal{J}_X$，则$f^{-1}(B)=f^{-1}(\cap_{i=0}^{n} S_i)\in\mathcal{J}_X$，则$f^{-1}(U)=f^{-1}( \cup_{B\in\mathscr{B}_U}B)\in\mathcal{J}_X$.
所以$f$连续.

## 1.5 拓扑空间中的序列
**定义 1.5.1：**
设$X$是一个拓扑空间,$\{x_n\}_{n=1}^\infty$是$X$的一个点列,$x_0\in X$,如果$\forall x_0$的领域$U,\exist N,\forall n>N$,有$x_n\in U$ ,则称$\{x_n\}_{n=1}^\infty$收敛于$x_0$,记为$x_n\to x_0(n\to \infty)$.
>同一点列收敛的点不唯一（例：平凡拓扑空间）

**命题 1.5.2：**
设$X$是一拓扑空间,$x\in X,X-\{x\}$中有一点列收敛于$x$,则$x$是聚点.

**命题 1.5.3：**
设$X$是不可数集 给$X$定义可数补拓扑，则$\exist x_0\in X,s.t. \ x_n\to x_0(n\to \infty)\iff \{x_n\}_{n=1}^\infty$.是最终常点列.
>推论：在这个空间中,若$A$是不可数集,则每个点$x\in A$都是聚点.

**命题 1.5.4：**
设$X$是拓扑空间,$x_0\in X,f$连续,若$f$在$x_0$连续,则$\forall x_n\to x_0$,有$f(x_n)\to f(x_0).$
>逆命题不一定成立.