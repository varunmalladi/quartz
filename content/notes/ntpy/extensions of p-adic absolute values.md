---
title: "extensions of p-adic absolute values"
---

Let 
- $\mathcal{O}$ be a [[dedekind domain]]
- $\mathfrak{p}\subset\mathcal{O}$ a nonzero prime ideal
- $k$ its field of fractions
- $\widehat{k_\mathfrak{p}}$ the completion of $k$ with respect to the [[Absolute value|absolute value]] corresponding to the [[Valuation ring|valuation]] $v_\mathfrak{p}$
- $K/k$ a finite separable extension 
- $\mathcal{O}_K$ the [[Integral element|integral closure]] 
- $\mathbf{V}_\mathfrak{p}$ denote both sides of the isomorphism $K\otimes_k \widehat{k_\mathfrak{p}}\cong \oplus K_i$ (see property 8 [[Separable extension|here]])

Then three sets below are in one-to-one correspondence:
1. Different prime ideals $\mathfrak{B}_i\subset\mathcal{O}_K$ [[Prime ideal|lying over]] $\mathfrak{p}\subset\mathcal{O}$
2. Different absolute value functions $\|\cdot\|:K\to\mathbb{R}_{\geq 0}$ extending the $\mathfrak{p}$-adic absolute value
3. Components $K_i$ of the direct sum $V_\mathfrak{p}=\oplus K_i$

# Corollaries
1. The decomposition of $V_\mathfrak{p}$ respects these automorphisms: $$\bigcup_i \sum_{K_i/\widehat{k_\mathfrak{p}}}^{\overline{\widehat{k_\mathfrak{p}}}/\widehat{k_\mathfrak{p}}}\overset{\simeq}{\longrightarrow} \sum_{K/k}^{\bar{k}/k}$$
2. Suppose $K/k$ is normal. so that $K/k$ is a [[Galois extension]]. Let $G=\text{Gal}(K/k)$. Then
	1. $G$ acts transitively on the ideals $\mathfrak{B_i}$ lying over $\mathfrak{p}$. All the numbers $e_i$ in the product $\mathfrak{p}\mathcal{O}_K=\prod\mathfrak{B}_i^{e_i}$ are the same.
	2. Let $G_\mathfrak{B}=\{g\in G\mid g\mathfrak{B}=\mathfrak{B}\}$ be the stationary subgroup of $\mathfrak{B}$ under the action of $G$, also called the decomposition group of $\mathfrak{B}$. Then the subgroups $G_{\mathfrak{B}_i}$ are conjugate.
	3. Let $\pi_i(K)=K_i$ be the natural projection. Then $K_i=\pi_i(K)\widehat{k_\mathfrak{p}}$.
	4. The extensions $K_i/\widehat{k_\mathfrak{p}}$ are all isomorphic and Galois, and $\text{Gal}(K_i/\widehat{k_\mathfrak{p}})\cong G_\mathfrak{B}$.
