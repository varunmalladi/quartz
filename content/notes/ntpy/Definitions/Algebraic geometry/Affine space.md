---
title: "Affine space"
---

Let $K$ be an algebraically closed field. Let $A=K[x_1,\dots,x_n]$.

**Definition.** The _affine space_ of dimension $n$, denoted $\mathbb{A}_K^n$ (or just $\mathbb{A}^n$ if context is clear) is defined to be the set of $n$-tuples of $K$:
$$
\mathbb{A}^n=\{(a_1,\dots,a_n)\mid a_i\in K\}
$$

Notice that the above differs from an $n$-dimensional $K$-vector space in that it does not say anything about the vector space structure.

## Subsets
1. [Algebraic subset](notes/ntpy/Definitions/Algebraic geometry/Algebraic subset.md), [Affine variety](notes/ntpy/Definitions/Algebraic geometry/Affine variety.md)
2. For any subset $Y\subseteq\mathbb{A}^n$, we can define the ideal of $Y$ in $A$ by $$I(Y)=\{f\in A\mid f(P)=0\text{ for all }P\in Y\}.$$ This is spiritually a converse construction to (1). This does not, however, imply that every subset is an algebraic subset. The $I(Y)$ may have more zeros than just the elements of $Y$, for example.