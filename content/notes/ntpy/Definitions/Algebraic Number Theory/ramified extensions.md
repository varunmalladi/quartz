---
title: "ramified extensions"
---

# Definition
Suppose 
- $\mathcal{O}$ is a complete [discrete valuation ring](<notes/ntpy/Definitions/Algebraic Number Theory/discrete valuation ring.md>)
- $\mathfrak{p}$ its maximal idea
- $k$ its field of fractions, 
- $K/k$ a finite separable extension of degree $n$
- $\mathcal{O}_K$ its [valuation ring](<notes/ntpy/Definitions/Ring theory/Valuation ring.md>) (to which the $\mathcal{p}$-adic absolute value uniquely extends)
- $\mathfrak{B}\subset\mathcal{O}_K$ a unique maximal ideal
- $k_\mathfrak{p}$ and $K_\mathfrak{B}$ the residue fields, e.g. $k_\mathfrak{p}=k/\mathfrak{p}$.
- $K_\mathfrak{B}/k_\mathfrak{p}$ a separable extension
- $f=f(\mathfrak{B}/\mathfrak{p})$ and $e=e(\mathfrak{B}/\mathfrak{p})$ (see [residue class degree, ramification index](<notes/ntpy/Definitions/Algebraic Number Theory/residue class degree, ramification index.md>)).

The [extension](<notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Field extension.md>) $K/k$ is called
1. unramified iff $e=1$
2. tamely ramified iff $\text{char}(k_\mathfrak{p})\nmid e$
3. totally ramified iff $f=1$

# Properties
1. TFAE:
	1. $K/k$ is tamely ramified
	2. $Tr_{K/k}(\mathcal{O}_K)=\mathcal{O}$
	3. $v_\mathfrak{B}(\mathfrak{D}_{K/k})=e-1$
2. (totally ramified extensions)
	1. Suppose $K=k_P$ where $P\in\mathcal{O}[T]$ is an [Eisenstein polynomial](<notes/ntpy/Definitions/Algebraic Number Theory/Eisenstein polynomial.md>). Then $K/k$ is totally ramified. Also, if $\Pi\in K$ and $P(\Pi)=0$, then $v_\mathfrak{B}(\Pi)=1$.
	2. Conversely, Suppose $K/k$ is totally ramified, $\Pi\in\mathcal{O}_K$, $v_\mathfrak{B}(\Pi)=1$. Then $P_\Pi$ is Eisenstein and $K=k(\Pi)$ and $\mathcal{O}_K=\mathcal{O}[\Pi]$.
3. (unramified extensions)
	1. Suppose $K=k_P$, $P\in\mathcal{O}[T]$ is monic of degree $n$, such that $\overline{P}\in k_\mathfrak{p}[T]$ (the residue mod $\mathfrak{p}$) is irreducible and separable. Then $K/k$ is unramified and $K_\mathfrak{B}=(k_\mathfrak{p})_{\overline{P}}$.
	2. Suppose $K/k$ is unramified. Then there exists $x\in\mathcal{O}_K$ such that $K_\mathfrak{B}=k_\mathfrak{p}(\overline{x})$. If this is the case then $K=k(x)$, $\mathcal{O}_K=\mathcal{O}[x]$, $\overline{P_x}\in k_\mathfrak{p}[T]$ is irreducible and separable.
4. Suppose $K/k$ is unramified, $K'/k$ any finite separable extension. Then the natural map $\sum_{K/k}^{K'/k}\to\sum_{K_\mathfrak{B}/k_\mathfrak{p}}^{K'_{\mathfrak{B}'}/k_\mathfrak{p}}$ is a one-to-one corespondence. If $K_\mathfrak{B}/k_\mathfrak{p}\simeq K'_\mathfrak{B}/k_\mathfrak{p}$ and $K'/k$ is unramified then $K/k\simeq K'/k$.
5. (maximal unramified subextension)
	1. There exists a unique subfield $k\subset K_0\subset K$ which is unramified and contains any other unramified subfield. Any subfield $K\subset K_1\subset K_0$ is unramified. $(K_0)_{\mathfrak{B}_0}=K_\mathfrak{B}$.
	2. (inertia group) If $K/k$ is [normal](<notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Normal extensions.md>), so is $K_0/k$. Suppose $G=\text{Gal}(K/k)$. Then $K_0/k$ corresponds to the subgroup $G_0\subset G$ defined as $G_0\coloneqq\{g\in G\mid\forall x\in\mathcal{O}_K,\ v_\mathfrak{B}(g(x)-x)>0\}$.
	3. The group $G_0$ is called the inertia group. There exists a decreasing chain of subgroups $G\supset G_0\supset G_1\supset\dots$ which are called ramification groups.