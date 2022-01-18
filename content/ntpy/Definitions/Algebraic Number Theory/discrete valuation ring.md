---
title: "discrete valuation ring"
---

# Idea
There is a direct analogy to complex analysis. Given a pole, we are often interested in its order. The structure of a DVR axiomatizes this notion of order. The formal Laurent series at that point forms a DVR, for example, as do the germs of meromorphic functions.

In algebraic number theory, rather than the orders of poles we are interested in the number of times a prime divides an algebraic number.

# Defintions
The following are equivalent characterizations of a DVR:
1. A Noetherian integrally closed domain with exactly one nonzero prime ideal (with Krull dimension 1)
2. A [[Principal ideal domain|PID]] that is also [[Local ring|local]]
3. A valuation ring with value group isomorphic to the integers under addition

# Complete d.v.r.'s
Suppose 
- $\mathcal{O}$ is a complete dvr
- $\mathfrak{p}$ its maximal idea
- $k$ its field of fractions, 
- $K/k$ a finite separable extension of degree $n$
- $\mathcal{O}_K$ its valuation ring (to which the $\mathcal{p}$-adic absolute value uniquely extends)
- $\mathfrak{B}\subset\mathcal{O}_K$ a unique maximal ideal
- $k_\mathfrak{p}$ and $K_\mathfrak{B}$ the residue fields, e.g. $k_\mathfrak{p}=k/\mathfrak{p}$.
- $K_\mathfrak{B}/k_\mathfrak{p}$ a separable extension
- $f=f(\mathfrak{B}/\mathfrak{p})$ and $e=e(\mathfrak{B}/\mathfrak{p})$ (see [[residue class degree, ramification index]]).

We will use the bar symbol to denote the residue of an element of $\mathcal{O}_K$ modulo $\mathfrak{B}$.

1. For all $x\in K$, we have $$v_\mathfrak{B}(N(x))=nv_\mathfrak{B}(x)$$
2. The unque extension of the absolute value $\|x\|_\mathfrak{p}=s^{-v_\mathfrak{p}(x)}$ from $k$ to $K$ is given by the formula $$\|x\|\coloneqq \|N(x)\|^{1/n}$$
3. $f$ is finite, and $$ef=n$$
4. Suppose $x\in \mathcal{O}_K$.
	1. $\overline{Tr_{K/k}(x)}=eTr_{k_\mathfrak{B}/k_\mathfrak{p}}(\overline{x})$.
	2. $\overline{N_{K/k}(x)}=(N_{K_\mathfrak{B}/k_\mathfrak{p}}(\overline{x}))^e$
5. $v_\mathfrak{B}(\mathfrak{D}_{K/k})\geq e-1$ (see [[different]])

# Related
- [[Valuation ring]]
- [[Noetherian ring]]