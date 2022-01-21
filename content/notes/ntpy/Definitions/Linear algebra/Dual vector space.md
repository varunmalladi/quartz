---
title: "Dual vector space"
---

## Traditional definition
### Between vector spaces
Let $V$ be a vector space over a field $F$.

**Definition.** The _dual space_ of $V$, denoted $V^\ast$, is the vector space $\text{Hom}(V,F)$.
### Basis
#### Finite dimensional
**Proposition.** If $V$ is finite dimensional with basis $\{v_1,\dots,v_n\}$, definte $f^i\in V^\ast$ by
$$ f^i(v_j)=\delta_j^i,\quad 1\leq i,j\leq n. $$
Then the $\{f^1,\dots,f^n\}$ form a basis of $V^\ast$.
### Transpose map
The map $f:V\to W$ induces a map $f^\ast:W^\ast\to V^\ast$ via the following extension:
$$
\begin{array}
zV & \overset{f}{\rightarrow} & W \\
{}_{f^\ast\ \coloneqq\ \phi\circ f} & \searrow & \rlap{\ \ {}^\phi}{\downarrow} \\ 
& & F
\end{array}
$$

## Categorical definition
The unit object in the category $\text{Vect}_F$ is $F$ regarded as a vector space over itself. The dual object of an object $V$ in category theory is the internal hom $[V,K]$.
### Transpose map
Recall from above that a map $f:V\to W$ induces a map $f^\ast:W^\ast\to V^\ast$. This extends to a contravariant functor from $\text{Vect}_F$ to its dual. In particular, this functor is the [representable functor](notes/ntpy/Definitions/Category theory/Representable functor.md) represented by $F$:
$$
\text{Hom}(V\to W, F) \mapsto \text{Hom}(W,F)\to\text{Hom}(V,F).
$$

## Properties

- If $V$ is finite dimensional, then $(V^\ast)^\ast\cong V$.
- If $A$ is the matrix for a map in $V$, then the matrix for $A^\ast$ is $A^t$.
