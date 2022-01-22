---
title: "associated p-adic algebra"
---

# Extending definitions
- ([trace](<notes/ntpy/Definitions/Algebraic Number Theory/trace.md>)) We may extend the bilinear form $Tr_{K/k}(ab)$ from $K$ to $V_\mathfrak{p}$ by $\widehat{k_\mathfrak{p}}$-linearity. Using the notation $\langle \ , \ \rangle$ for the resulting form, $$\langle a,b\rangle=\sum Tr_{K_i/\widehat{k_\mathfrak{p}}}(\pi_i(a)\pi_i(b))$$
- ([Lattice](<notes/ntpy/Definitions/Algebraic Number Theory/Lattice.md>))
- (dual lattice)
- ([index of lattice](<notes/ntpy/Definitions/Algebraic Number Theory/index of lattice.md>))

# Properties
1. ([extensions of p-adic absolute values](<notes/ntpy/extensions of p-adic absolute values.md>))
2. Suppose $M$ and $N$ are $\mathcal{O}$-lattices in $K$. Then $M\widehat{\mathcal{O}}_\mathfrak{p}$ and $N\widehat{\mathcal{O}}_\mathfrak{p}$ are $\widehat{\mathcal{O}}_\mathfrak{p}$-lattices in $\mathbf{V}_\mathfrak{p}$ and
	1. $(M:N)_\mathcal{O}\widehat{\mathcal{O}}_\mathfrak{p}=(M\widehat{\mathcal{O}}_\mathfrak{p}:N\widehat{\mathcal{O}}_\mathfrak{p})_{\widehat{\mathcal{O}}_\mathfrak{p}}$
	2. $D_\mathcal{O}(N)\widehat{\mathcal{O}}_\mathfrak{p}=D_{\widehat{\mathcal{O}}_\mathfrak{p}}(N\widehat{\mathcal{O}}_\mathfrak{p})$
	3. $\mathfrak{d}_\mathcal{O}(N)\widehat{\mathcal{O}}_\mathfrak{p}=\mathfrak{d}_{\widehat{\mathcal{O}}_\mathfrak{p}}(N\widehat{\mathcal{O}}_\mathfrak{p})$
3. Suppose $M$ and $N$ are $\widehat{\mathcal{O}}_\mathfrak{p}$-lattices in $\mathbf{V}_p$ such that $M=\bigoplus\pi_i(M)$ and $N=\bigoplus\pi_i(N)$. Then
	1. $(M:N)_{\widehat{\mathcal{O}}_\mathfrak{p}}=\prod(\pi_i(M):\pi_i(N))_{\widehat{\mathcal{O}}_\mathfrak{p}}$
	2. $D_{\widehat{\mathcal{O}}_\mathfrak{p}}(N)=\bigoplus D_{\widehat{\mathcal{O}}_\mathfrak{p}}(\pi_i(N))$
	3. $\mathfrak{d}_{\widehat{\mathcal{O}}_\mathfrak{p}}(N)=\prod\mathfrak{d}_{\widehat{\mathcal{O}}_\mathfrak{p}}(\pi_i(N))$
4. Let $\mathcal{O}_i$ be the [Valuation ring](<notes/ntpy/Definitions/Ring theory/Valuation ring.md>) in $K_i$, $\|\cdot\|$ being the unique absolute value on $K_i$ which extends the $\mathfrak{p}$-adic absolute value on $\widehat{k_\mathfrak{p}}$. Then
	1. $\mathcal{O}_i$ is the [integral closure](<notes/ntpy/Definitions/Ring theory/integral extensions.md>) of $\widehat{\mathcal{O}}_\mathfrak{p}$ in $K_i$.
	2. The topological closure of $\mathcal{O}_K\mathcal{O}_\mathfrak{p}$ in $\mathbf{V}_\mathfrak{p}$ is $\mathcal{O}_K\widehat{\mathcal{O}}_\mathfrak{p}=\bigoplus\mathcal{O}_i$.
5. Suppose $I$ is an $\mathcal{O}_K$-[fractional ideal](<notes/ntpy/Definitions/Algebraic Number Theory/fractional ideal.md>) in $K$.
	1. $I\widehat{\mathcal{O}}_\mathfrak{p}$ fits the assumptions of (3)
	2. $N_{K/k}(I)\widehat{\mathcal{O}}_\mathfrak{p}=\prod N_{K_i/\widehat{k_\mathfrak{p}}}(\pi_i(I)\mathcal{O}_i)$
	3. $N_{K/k}:\mathcal{F}(\mathcal{O_K})\to\mathcal{F}(\mathcal{O})$ is a group homomorphism.
	4. $\pi_i(\mathfrak{D}_{K/k})\mathcal{O}_i=\mathfrak{D}_{K_i/\widehat{k_\mathfrak{p}}}$ (see [different](<notes/ntpy/Definitions/Algebraic Number Theory/different.md>))
	5. $\mathfrak{d}_{K/k}\widehat{\mathcal{O}}_\mathfrak{p}=\prod \mathfrak{d}_{K_i/\widehat{k_\mathfrak{p}}}$ (see [discriminant](<notes/ntpy/Definitions/Algebraic Number Theory/discriminant.md>)) 
	6. $N_{K/k}(\mathfrak{D}_{K/k})=\mathfrak{d}_{K/k}$

# Related
- [ring of integers](<notes/ntpy/Definitions/Algebraic Number Theory/ring of integers.md>)
