---
title: "direct limit"
---

# Idea
A direct limit is a special kind of [[(co)limit|colimit]]. It's naming is a consequence of them being defined before categorical formalism, and also for the fact that one can guess what diagram the colimit is over, etc.

# Definition
- A *directed set* is a partially ordered set where each finite subset has an upper bound.
- A *directed system* of (say) abelian groups $(A_i, f_{ij})_{i,j\in I}$ is
	- an abelian group $A_i$ for eachh $i\in I$
	- a homomorphihsm $f_{ij}:A_i\to A_j$ whenever $i\leq j$
	- $f_{ii}=\text{id}_{A_i}$
	- $f_{ij}=f_{jk}\circ f_{ij}$, i.e. the following diagram commutes:
	<img align="center" src="https://i.upmath.me/svg/%5C%5B%5Cbegin%7Btikzcd%7D%0A%09%7BA_i%7D%20%26%20%7BA_j%7D%20%5C%5C%0A%09%26%20%7BA_k%7D%0A%09%5Carrow%5B%22%7Bf_%7Bik%7D%7D%22'%2C%20from%3D1-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7Bf_%7Bij%7D%7D%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7Bf_%7Bjk%7D%7D%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D%5C%5D" alt="\[\begin{tikzcd}
	{A_i} &amp; {A_j} \\
	&amp; {A_k}
	\arrow[&quot;{f_{ik}}&quot;', from=1-1, to=2-2]
	\arrow[&quot;{f_{ij}}&quot;, from=1-1, to=1-2]
	\arrow[&quot;{f_{jk}}&quot;, from=1-2, to=2-2]
\end{tikzcd}\]" />
- A *direct limit* the colimit. Explicitly, it is the universal object $A$ equipped with morphisms $\phi_i:A_i\to A$ such that the following diagram commutes:
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%7BA_i%7D%20%26%20%7B%7D%20%26%20%7BA_j%7D%20%5C%5C%0A%09%26%20A%0A%09%5Carrow%5B%22%7Bf_%7Bij%7D%7D%22%2C%20from%3D1-1%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22%7B%5Cphi_i%7D%22'%2C%20from%3D1-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7B%5Cphi_j%7D%22%2C%20from%3D1-3%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	{A_i} &amp; {} &amp; {A_j} \\
	&amp; A
	\arrow[&quot;{f_{ij}}&quot;, from=1-1, to=1-3]
	\arrow[&quot;{\phi_i}&quot;', from=1-1, to=2-2]
	\arrow[&quot;{\phi_j}&quot;, from=1-3, to=2-2]
\end{tikzcd}" />

# Morphisms
Consider two directed systems $(A_i,f_{ij})$, $(B_i, g_{ij})$ indexed by the same set $I$. A morphism $$\phi:(A_i,f_{ij})\to (B_i, g_{ij})$$ is a natural transformation between the directed systems, regarded as categories. Explicitly, 
- for eachh $i\in I$, a morphism $\phi_i:A_i\to B_i$ such that the following diagram commutes:
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%7BA_i%7D%20%26%20%7BA_j%7D%20%5C%5C%0A%09%7BB_i%7D%20%26%20%7BB_j%7D%0A%09%5Carrow%5B%22%7Bf_%7Bij%7D%7D%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7Bg_%7Bij%7D%7D%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7B%5Cphi_i%7D%22'%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22%7B%5Cphi_j%7D%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	{A_i} &amp; {A_j} \\
	{B_i} &amp; {B_j}
	\arrow[&quot;{f_{ij}}&quot;, from=1-1, to=1-2]
	\arrow[&quot;{g_{ij}}&quot;', from=2-1, to=2-2]
	\arrow[&quot;{\phi_i}&quot;', from=1-1, to=2-1]
	\arrow[&quot;{\phi_j}&quot;, from=1-2, to=2-2]
\end{tikzcd}" />

This indduces a homomorphism between the direct limits
$$\lim_\to\phi:\lim_\to A_i\to \lim_\to B_i.$$

# Examples
**1** [[P-adic numbers]]

**2** (subextensions) 
Given an algebraic extension $K/F$, the set of all subextensions $K/L/F$ (we can exclude $K$) is a partially ordered set under inclusions. Furthermore, it is 
- directed: $L,L'\subseteq LL'$
- a directed system: wrt inclusion maps

The direct limit of this system is $K$ itself. It expresses the fact that $K$ is the union of all intermediate fields $K/L/F$. 

**2(b)** (Galois extensions)
Let $K/k$ be Galois. Then for every $\alpha\in K$, the minimal polynomial $P_\alpha$ is separable and all of its roots are contained in $K$. Hence $k_{P_\alpha}\subset L$, whence $k_{P_\alpha}/k$ is finite Galois. Thus $$K/k\cong\lim_\to L/k$$ indexed over all $L/k$ finite Galois.

**3** (uniqueness of algebraic closure)
By Example 2, 

**4** (uniqueness of separable closure)