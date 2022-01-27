---
title: "Projective space"
---

# Algebraic sets
Recall that a polynomial $F\in k[x_0,\dots,x_n]$ is called _homogeneous_ of degree $d$ if $F(\lambda x_0,\dots,\lambda x_n)=\lambda^d\cdot F(x_0,\dots,x_n)$. 

If $T$ is a set of homogeneous elements of $S$, define the zero set of $T$: $$Z(T)=\{P\in\mathbb{P}^n\mid f(P)=0\text{ for all }f\in T\}.$$

Let $S$ denote the polynomial ring $k[x_0,\dots,x_n]$ regarded as a graded ring. (See [Polynomial ring](notes/ntpy/Definitions/Ring theory/Polynomial ring.md) for details.)

**Definition.** A subset $Y$ of $\mathbb{P}^n$ is an _algebraic set_ if there exists a set $T$ of homogeneous elements of $S$ such that $Y=Z(T)$. 

One can show that these are closed under finite unions and arbitary intersections, allowing us to define the [Zariski topology](notes/ntpy/Definitions/Algebraic geometry/Zariski topology.md).

**Definition.** A *quasi-projective algebraic set* is an open subset of a (projective) algebraic set.

## Examples
- On $\mathbb{P}^1$, the projective algebraic sets are $\emptyset$, $\mathbb{P}^1$, and finite collections of homogeneous points $\{p_1,\dots,p_n\}$.