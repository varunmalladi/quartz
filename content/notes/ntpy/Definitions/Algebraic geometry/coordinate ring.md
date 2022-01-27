---
title: "coordinate ring"
---

# Definition
Let $V$ be an [Algebraic subset](notes/ntpy/Definitions/Algebraic geometry/Algebraic subset.md) of $k^n$, $k$ algebraically closed. 
- The *coordinate ring* of $V$, denoted $k[V]$, is the $k$-algebra of $k$-valued functions on $V$ obtained by restricting polynomial functions to $V$.

# Properties
1. Letting $I(V)$ be the ideal of functions which vanish on $V$, $$k[V]\cong k[X]/I(V).$$
2. As sets, \begin{gather}\text{ev}:V\overset{\simeq}{\rightarrow}\text{Hom}_{k-\text{alg}}(k[V],k),\\ x\mapsto \text{ev}_x \\ (x_i=\phi(X_i|_V))\leftarrow \phi\end{gather} where the hom-set consists of $k$-algebra homomorphisms.
	1. Let $\text{Specm}(A)$ denote the set of maximal ideals of $A$. By [Nullstellensatz](notes/ntpy/Theorems/Ring Theory/Nullstellensatz.md), the above says \begin{gather}\text{Hom}_{k-\text{alg}}(k[V],k)\cong\text{Specm}(k[V]), \\ f\mapsto\text{ker}(f).\end{gather} (Indeed, $\text{Specm}(k[V])\cong V$.)
	2. 
3. $k[V]$ is finitely generated and reduced (i.e. does not contain non-zero nilpotent elements).

*Proofs*
**2**
