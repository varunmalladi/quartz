---
title: "Algebraic subset"
---

# Affine

Let $k$ be an algebraically closed field. Let $A=k[x_1,\dots,x_n]$. For $T\subset A$, and define $$Z(T)=\{P\in \mathbb{A}^n\mid f(P)=0 \text{ for all } f\in T\}.$$

**Definition.** An _algebraic subset_ $V\subseteq\mathbb{A}^n$ is a set of tuples satisfying some collection of polynomials:
$$
V=\{(a_1,\dots,a_n)\mid f_\alpha(a_1,\dots,a_n)=0, f_\alpha\in K[x_1,\dots,x_n]\}.
$$
Equivalently, a subset $Y$ of $\mathbb{A}^n$ is an _algebraic set_ if there exists $T\subseteq A$ such that $Y=Z(T)$.

Examples:
- $V=\emptyset$ where $f_\alpha$ is any subset of the nonzero constant polynomials
- $V=\mathbb{A}^n$ where $f_\alpha=0$. 
- The only algebraic subsets of $\mathbb{A}^1$ are the empty set, the entire set, or finite collections of points. This is due to polynomials in one variable splitting over $K$.

These determine a topology in which they are precisely the closed sets, the [Zariski topology](<notes/ntpy/Definitions/Algebraic geometry/Zariski topology.md>).

**Definition.** An algebraic subset $V\subseteq\mathbb{A}^n$ is called _reducible_ if $V=V_1\cup V_2$, where each $V_i$ is a proper algebraic subset. Otherwise $V$ is called _irreducible_. This is an [Affine variety](<notes/ntpy/Definitions/Algebraic geometry/Affine variety.md>).

Although similar to the notion of connectedness in topology, the two are different. Namely there are reducible but connected algebraic subsets.

**[Theorem](<notes/ntpy/Key Ideas/Algebraic geometry/Algebraic subsets can be decomposed.md>).** Every algebraic subset can be decomposed into finitely many components.

# Quasi-affine
**Definition.** An open subset of an algebraic subset is a _quasi-affine algebraic subset_.

# Projective
**Definition.** A subset $Y$ of $\mathbb{P}^n$ ([Projective space](<notes/ntpy/Definitions/Algebraic geometry/Projective space.md>)) is an *algebraic set* if there exists a set $T$ of homogeneous elements of $S$ such that $Y=Z(T)$. 

See [Projective space](<notes/ntpy/Definitions/Algebraic geometry/Projective space.md>) for details.