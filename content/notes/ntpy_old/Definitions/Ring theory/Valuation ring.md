---
title: "Valuation ring"
---

Let $K$ be a field and $\|\cdot\|:K\to\mathbb{Z}_{\geq 0}$ a nonarchimedean [absolute value](ntpy/Definitions/Ring theory/Absolute value.md).

**Definition.** The _valuation ring_ of $K$ consists of all elements with absolute value $\leq 1$:
$$
O=\{x\in K:\|x\|\leq 1\}
$$

Let $U=O^\ast=O\setminus p$ (see properties), i.e. those elements with absolute value 1. Then $U$ is a subgroup of $K^\ast$ and $\|\cdot\|:K^\ast/U\to\mathbb{R}^\ast_{>0}$ is an inclusion.

**Definition.**  $\|\cdot\|$ is called _discrete_ when $\|K^\ast\|$ under the above map is a discrete subgroup of $\mathbb{R}^\ast_{>0}$, i.e. is trivial or infinite cyclic.

### Properties
- The maximal ideal of $O$ is all elements with absolute value $<1$: $$p=\{x\in K\mid\|x\|<1\}$$
	- $p\neq (0)$ if and only if $\|\cdot\|$ is nontrivial
- For every nonzero $x\in K$, either $x\in O$ or $x^{-1}\in O$ (possibly both).
- $O$ is [local](ntpy/Definitions/Ring theory/Local ring.md) and $K=O_{(0)}$
- $O$ is [integrally closed](ntpy/Definitions/Ring theory/Integral element.md).
- $\|\cdot\|$ is discrete if and only if $p$ is a principal ideal.
