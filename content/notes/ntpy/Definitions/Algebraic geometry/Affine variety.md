---
title: "Affine variety"
---

**Definition.** A [algebraic subset](<notes/ntpy/Definitions/Algebraic geometry/Algebraic subset.md>) $A\subset\mathbb{A}^n$ is called an _affine variety_ if it is irreducible.

**Definition.** The dimension of an affine variety $X$ is defined as
$$
\dim(X)=\max\{k\in\mathbb{N}\mid X\supsetneq X_1\supsetneq \cdots\supsetneq X_k\}
$$
where each $X_i$ is a nonempty affine variety.

# Quasi-varieties

**Definition.** An open subset of an affine variety (wrt to the subspace topology induced from the Zariski topology) is called a _quasi-affine variety_.

Note that every affine variety is a quasi-affine variety, since the whole space is open (and closed).

# Normal
For $X$ an affine variety, we say that it is normal if $K[X]$ is [integrally closed](<notes/ntpy/Definitions/Ring theory/Integral element.md>) in its field of fractions.
# Properties
1. If $X$ is an affine variety, then $I(X)$ is prime.
2. Let $X$, $Y$ be affine varieties and $A(X)$, $A(Y)$ their [coordinate rings](<notes/ntpy/Definitions/Algebraic geometry/Affine coordinate ring.md>). Then $X\cong Y$ iff $A(X)\cong A(Y)$.
	1. Hence $A(-)$ is a (contravariant) functor witnessing that the category of affine varieties and the category of f.g. integral domains over $k$ are equivalent.
3. Not every quasi-variety is a variety, e.g. $\mathbb{A}^2\setminus (0,0)$.
