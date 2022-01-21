---
title: "sheaf"
---

# Idea

# Definition
**Definition 1 (topological)**
Let us operate in a topological space $X$. Let $U$ be an open set with an open covering $\mathcal{U}$.

A *sheaf* $F$ is a presheaf such that
1. (locality) if $s,t\in F(U)$ are such that $s|_{U_i}=t|_{U_i}$ for each $U_i\in\mathcal{U}$, then $s=t$.
2. (gluing) if for each $i\in I$ there is a section $s_i\in F(U_i)$ such that $s_i|_{U_i\cap U_j}=s_j|_{U_i\cap U_j}$ for all $i,j\in I$, then there exists a section $s\in F(U)$ such that $s|_{U_i}=s_i$ for each $i\in I$.

**Definition 2 (abstract, componentwise)** 
Let $(C,J)$ be a small [site](notes/ntpy/site.md) (with coverage $J$).

A *sheaf* $A$ is a presheaf such that
- for every covering family $J(U)=\{p_i:U_i\to U\}_{i\in I}$
- for every compatible family of elements, i.e. $(s_i\in A(U_i))_{i\in I}$ such that for every square on the below left we have $A(f)(s_j)=A(g)(s_k)$: <img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09K%20%26%20%7BU_k%7D%20%26%26%20%7BA(K)%7D%20%26%20%7BA(U_k)%7D%20%5C%5C%0A%09%7BU_j%7D%20%26%20U%20%26%26%20%7BA(U_j)%7D%0A%09%5Carrow%5B%22f%22'%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22g%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7Bp_k%7D%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7Bp_j%7D%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7BA(f)%7D%22%2C%20from%3D2-4%2C%20to%3D1-4%5D%0A%09%5Carrow%5B%22%7BA(g)%7D%22'%2C%20from%3D1-5%2C%20to%3D1-4%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	K &amp; {U_k} &amp;&amp; {A(K)} &amp; {A(U_k)} \\
	{U_j} &amp; U &amp;&amp; {A(U_j)}
	\arrow&quot;f&quot;', from=1-1, to=2-1[]()
	\arrow&quot;g&quot;, from=1-1, to=1-2[]()
	\arrow&quot;{p_k}&quot;, from=1-2, to=2-2[]()
	\arrow&quot;{p_j}&quot;', from=2-1, to=2-2[]()
	\arrow&quot;{A(f)}&quot;, from=2-4, to=1-4[]()
	\arrow&quot;{A(g)}&quot;', from=1-5, to=1-4[]()
\end{tikzcd}" />

then 
- there exists a unique element $s\in A(U)$ such that $A(p_i)(s)=s_i$ for all $i\in I$ (completing the square on the above right)

# Examples

**Sections of continuous maps**
Let $f:Y\to X$ be a continuous map of topological spaces. This determines a sheaf $\Gamma(Y/X)$, whose value on an open subset $U\subset X$ is $$\Gamma(Y/X)(U)=\{s:U\to Y\mid f\circ s=1_U\}.$$

Let us verify that this is a sheaf:
- (presheaf) we can regard $\Gamma(Y/X)$ as a functor $$\Gamma(Y/X):\text{Op}(Y)^\text{op}\to \text{Set},$$ where an inclusion $U\hookrightarrow V$ induces $\Gamma(Y/X)(V)\to\Gamma(Y/X)(U)$ by precomposition: $$\begin{gather} s:V\to Y, f\circ s=1_V \\ \mapsto \\ t:U\hookrightarrow V\to Y, f\circ t=f\circ s\circ i=1_U.\end{gather}.$$
- (locality) if two functions agree on every open cover, they are equal
- (gluing)

**Structure sheaf of manifold**
Let $M$ be an $n$-dimensional $C^k$-manifold. Let $\mathcal{O}_M^j$ (with $j\leq k$) denote the sheaf whose values on an open subset $U$ (i.e. its sections) are $C^j$-functions $U\to\mathbb{R}$. This is a sheaf much for the same reasons as above.

When $j=k$, this sheaf is called the *structure sheaf* and denoted $\mathcal{O}_M$. Even after removing zero functions we obtain a sheaf: the nonzero $CC^k$ functions also form a sheaf, denoted $\mathcal{O}_X^\times$.

**Differential forms**
Letting $M$ be an $n$-dimensional $C^k$-manifold as above, the differential forms (of degree $p$) form a sheaf, denoted $\Omega_M^p$.

**Holomorphic functions**
Let $X$ be a complex manifold. Given an open set $U\subset X$, a holomorphic function $f:U\to\mathbb{C}$ is one such that $f$ is complex differentiable at every $z\in U$. 

To each $U$ we can associate a set(?) $F(U)$ of holomorphic function $U\to\mathbb{C}$. This determines a presheaf: if $V\subset U$ then by restriction every holomorphic $U\to\mathbb{C}$ determines a holomorphic $V\to \mathbb{C}$. Hence the inclusion $V\hookrightarrow U$ induces a map $F(U)\to F(V)$. 

This is a sheaf because:
- (locality) Suppose $\{U_i\}_{i\in I}$ is an open cover of $U$, and $s,t\in F(U)$ are such that $s|_{U_i}=t|_{U_i}$ for all $U_i$. This means the restrictions of the holomorphic $s,t$ to $U_i$ are all equal. So there value on every point in $U$ is identical, and so $s=t$.
- (gluing) Suppose for each $i\in I$ there exists a section $s_i\in F(U_i)$ such that $s_i|_{U_i\cap U_j}=s_j|_{U_i\cap U_j}$ for all $i,j\in I$. We need to construct a holomorphic $s:U\to\mathbb{C}$ whose restriction to $U_i$ is $s_i$. To begin, for any $z\in U$ define $s(z)=s_i(z)$ where $z\in U_i$. If $z\in U_j$ with $i\neq j$, $z\in U_i\cap U_j$ so by assumption  $s_i(z)=s_j(z)$ and this is well-defined. 

How might we interpret the [stalk]() $F_z$ for some $z\in X$? It is the set of all functions holomorphic at $z$ (meaning there exists some neighborhood of $z$ such that the function is differentiable at every point in that neighborhood). To see this, consider the definition $$F_z\coloneqq \lim_{\underset{z\in U}{\rightarrow}}F(U).$$
This is isomorphic to $$\left(\bigsqcup F(U)\right)/\sim$$
where we identify elements that are eventually equal in the directed system. In our case, if $s\in F(U_i)$, $t\in F(U_j)$ become equal in some $F(V)$, firstly this means that $V\in U_i\cap U_j$. Why would we want to identify $s$ and $t$ just because they agree on this open subset? A key property of complex functions is that the behavior of the function locally (i.e. the germ) is enough to reconstruct the function on any connected open subset on which the function is everywhere defined (analytic continuation).

- is every restriction $F(U)\to F(V)$ injective? No, we cannot assume $U$ is connected.

See: [Holomorphic function](notes/ntpy/Definitions/Holomorphic function.md)

**Regular functions on a variety**
Given 

[Regular map](notes/ntpy/Definitions/Algebraic geometry/Regular map.md)


