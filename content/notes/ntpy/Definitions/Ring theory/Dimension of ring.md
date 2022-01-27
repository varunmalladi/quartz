---
title: "Dimension of ring"
---

# Definition
**Definition.** The _dimension_ of a ring is the maximum length of an ascending chain of [prime ideals](<notes/ntpy/Definitions/Ring theory/Prime ideal.md>) 
$$
\mathfrak{p}_0\subsetneq\mathfrak{p}_1\subsetneq\cdots\subsetneq\mathfrak{p}_n\subsetneq A.
$$

By the dimension of an ideal $I\subset A$, we mean the dimension of the quotient $A/I$.

# Properties
1. If $A$ is an [integral domain](<notes/ntpy/Definitions/Ring theory/Integral domain.md>) of dimension 0, then there are no prime maximal ideals except 0 and $A$.
2. (Krull ideal theorem) For $x\in A$, let $\mathfrak{p}$ be the minimal prime ideal containing $x$. Then $$\text{dim }A/\mathfrak{p}=\text{dim}(A)-1.$$