---
title: "Tensor product of vector spaces"
---

## Finite dimensional case
Let $V,U$ be finite dimensonal vector spaces over $K$. 

Let $Free(V,U)$ be the set of finite linear combinations $$\sum_{i=1}^na_i(x_i,y_i)$$ where $n\in\mathbb{Z}+$, $x_i\in V$, $y_i\in U$, and $a_i\in K$.

**Definition.** The _tensor product_ of $V$ and $U$, denoted $V\otimes U$, is the quotient $Free(V,U)/\sim$, where $\sim$ is the bilinear equivalence relation:
$$
(ax+bz,y)=a(x,y)+b(z,y),\quad (x,ay+bt)=a(x,y)+b(x,t).
$$

### Basis
**Proposition.** If $\{v_1,\dots,v_n\}$ is a basis of $V$ and $\{u_1,\dots,u_m\}$ is a basis of $U$, then $$ \{v_i\otimes u_j\mid 1\leq i\leq n, \ 1\leq j\leq m\} $$ forms a basis of $V\otimes U$.

### Symmetric and antisymmetric tensors
**Definition.** The subspace of _symmetric tensors_ $S^2(V)\subset V\otimes V$ is defined as
$$
\text{span}\{x\otimes y + y\otimes x\mid x,y\in V\}.
$$

**Definition.** The subspace of _antisymmetric tensors_ $\Lambda^2(V)\subset V\otimes V$ is defined as
$$
\text{span}\{x\otimes y-y\otimes x\mid x,y\in V\}.
$$

On elementary tensors, it is obvious we these are named the way they are.

## Properties
1. If $V$ is finite-dimensional, then $V\otimes V^\ast\cong\text{End}(V)$.
2. Given $A\in\text{End}(V)$ and $B\in\text{End}(U)$, we can construct a well defined element $A\otimes B\in\text{End}(V\otimes U)$ by the formula $$ A\otimes B(v\otimes u)=(Av)\otimes (Bu) $$. 
3. If $V$ is finite dimensional, then $S^2(V)\oplus\Lambda^2(V)=V\otimes V$.