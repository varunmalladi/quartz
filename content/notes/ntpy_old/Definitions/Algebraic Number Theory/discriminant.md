---
title: "discriminant"
---

# Dedekind domains

Let $\mathcal{O}$ be a [dedekind domain](ntpy/Definitions/Algebraic Number Theory/dedekind domain.md) and $k$ its field of fractions, $K$ a finite separable [extension](ntpy/Definitions/Algebraic Number Theory/Field Theory/Field extension.md). Suppose $N$ is an $\mathcal{O}$-[lattice](ntpy/Definitions/Algebraic Number Theory/Lattice.md) in $K$. 

The discriminant of $N$ is the $\mathcal{O}$-[fractional ideal](ntpy/Definitions/Algebraic Number Theory/fractional ideal.md) in $k$ $$\mathfrak{d}_\mathcal{O}(N)\coloneqq (D_\mathcal{O}(N):N)_\mathcal{O}$$ We may just write $\mathfrak{d}_{K/k}$ for $\mathfrak{d}_\mathcal{O}(\mathcal{O}_K)$. The latter is an ideal in $\mathcal{O}$.

## Properties
Suppose $N,M\subset K$ are $\mathcal{O}$-lattices. Then
1. If $N=\langle\{e_i\}\rangle$ is a free $\mathcal{O}$-module, then $$\mathfrak{d}_\mathcal{O}(N)=(\text{det }Tr(e_ie_j))$$ *Notation:* The generating element on the right is denoted $\Delta_\mathcal{O}(N)\in k^\ast/(\mathcal{O}^\ast)^2$. If $\mathcal{O}=\mathbb{Z}$, then we may just write $\Delta(N)$, and $\Delta_K$ for $N=\mathcal{O}_K$.
2. $$\mathfrak{d}_\mathcal{O}(N)=\mathfrak{d}_\mathcal{O}(M)(M:N)^2_\mathcal{O}$$
3. Suppose $N\subset M$. Then $\mathfrak{O}(N)\subset\mathcal{O}(M)$, with equality iff $M=N$.
4. $$\mathfrak{d}_\mathcal{O}(N)=\prod_\mathfrak{p}\mathfrak{p}^{v_\mathfrak{p}(\mathfrak{d}_{\mathcal{O}_\mathfrak{p}}(N_\mathfrak{p}))}$$
