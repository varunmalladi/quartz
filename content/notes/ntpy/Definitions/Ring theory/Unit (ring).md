---
title: "Unit (ring)"
---

Let $A$ be a commutative ring with identity. 

**Definition.** A _unit_ is an element $x\in A$ such that $xy=1$ for some $y\in A$.

### Properties
1. The element $y$ is uniquely determined by $x$, justifying the notation $x^{-1}$.
2. The units in $A$ for a multiplicative abelian group.
3. $x$ is a unit if and only if $(x)=A=(1)$.
	1. [Ideal](notes/ntpy/Definitions/Ring theory/Ideal.md) for definition of principal ideal

#### Proofs
##### 1
Suppose $xy_1=xy_2=1$.  Multiplying all sides by $y_1$ (on the left) gives that $(y_1x)y_1=(y_1x)y_2=y_1$ and so $y_1=y_2=y_1$. 
##### 2
Clearly if $u_1$ and $u_2$ are units then $u_1u_2$ is a unit, since $u_1u_2u_1^{-1}u_2^{-1}=1$. The element 1 is certainly a unit.
##### 3
For the forward direction, suppose $x$ is a unit. Then it contains $xx^{-1}=1$ and the result follows. Conversely, suppose $(x)=A$. Then in particular $1\in (x)$ so there is some $a\in A$ such that $ax=1$. 