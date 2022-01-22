---
title: "scheme"
---

# Idea
According to [Nullstellensatz](<notes/ntpy/Theorems/Ring Theory/Nullstellensatz.md>), there is a one-to-one correspondence...

... generalize varieties so that on the left we may take arbitrary commutative rings.

# Definition
Let $R$ be a commutative ring, and $X$ a locally [ringed space](<notes/ntpy/ringed space.md>).
- $X$ is an *affine scheme* if it isomorphic to $\text{Spec}(R)$ (for some $R$).
- $X$ is a *scheme* if it admits a covering $\{U_i\}$ such that each $U_i$ is an affine scheme.

# Examples
**1** ($\mathbb{A}^n_k$, affine)
The maximal ideals of $k[x_1,\dots,x_n]$ are of the form $x_i-\alpha$ for some $\alpha\in\mathbb{A}^n_k$. Hence $\mathbb{A}^n_k$ is the spectrum of the commutative ring $k[x_1,\dots,x_n]$, and is therefore an affine scheme.

In fact one may take this as the definition of affine $n$-space, and for any commutative ring $R$ define affine $n$-space as $\text{Spec}(R[x_1,\dots,x_n])$.
