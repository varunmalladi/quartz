---
title: "Projective variety"
---



# Definition
Let $k$ be an algeraically closed field. 

## Projective space
The _projective $n$-space_, denoted $\mathbb{P}^n$, is the [affine space](notes/ntpy/Definitions/Algebraic geometry/Affine space.md) of dimension $n+1$ with the origin removed an all lines through the origin identified: 
$$
\begin{gather}
(\mathbb{A}^{n+1}-\{0\})/\sim \\
(a_0,\dots,a_n)\sim (\lambda a_0,\dots,\lambda a_n),\quad \lambda\in k\setminus\{0\}
\end{gather}
$$

The equivalence class of a point $P\in\mathbb{P}^n$ is called the _set of homogeneous coordinates_ for $P$.

## Algebraic sets
Let $T\subset k[x_0,\dots,x_n]$. Define
$$
Z(T)=\{P\in\mathbb{P}^n\mid f(P)=0\text{ for all }f\in T\}.
$$

**Definition.** A subset $Y\subset\mathbb{P}^n$ is called an _algebraic set_ if there exists a set $T$

# Properties
1. If $V\subset \mathbb{P}^n$ is algebraic and $V\cap U_i$ is irreducible, then $V$ is irreducible.
