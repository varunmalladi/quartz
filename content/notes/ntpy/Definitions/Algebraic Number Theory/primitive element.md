---
title: "primitive element"
---

# Dedekind domains
Let $\mathcal{O}$ be a [dedekind domain](notes/ntpy/Definitions/Algebraic Number Theory/dedekind domain.md), $k$ its field of fractions, $K$ a finite separable [extension](notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Field extension.md). Let $\mathcal{O}_K$ denote the [integral closure](notes/ntpy/Definitions/Ring theory/Integral element.md).

$x\in\mathcal{O}_K$ is a primite element if $K=k(x)$.

## Properties
Let $D_\mathcal{O}(N)$ be the dual [module](notes/ntpy/Definitions/Ring theory/Module.md), $\mathfrak{d}$ the [discriminant](notes/ntpy/Definitions/Algebraic Number Theory/discriminant.md), $\mathfrak{D}$ the [different](notes/ntpy/Definitions/Algebraic Number Theory/different.md).
1. Let $P_x\in\mathcal{O}[T]$ be the [minimal polynomial]() corresponding to the primitive element  $x$. Then 
	1. $\mathcal{O}[x]$ is an $\mathcal{O}$-[lattice](notes/ntpy/Definitions/Algebraic Number Theory/Lattice.md).
	2. $D_\mathcal{O}(\mathcal{O}[x])=(P'(x))^{-1}\mathcal{O}[x]$
	3. $\mathfrak{d}_\mathcal{O}(\mathcal{O}[x])=(N_{K/k}(P_x'(x))=(\Delta_{P_x})$
	4. $\mathcal{O}_K=\mathcal{O}[x]$ iff $\mathfrak{D}_{K/k}=(P_x'(x))$