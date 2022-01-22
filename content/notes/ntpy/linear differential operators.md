---
title: "linear differential operators"
---

# Definition
Let $A$ be a commutative $\mathbb{C}$-algebra with unit. Let $H(A)$ be the set of $\mathbb{C}$-linear endomorphisms of $A$. 
1. $H(A)$ is generally non-commutative. Think matrices.
	1. If $A=\mathbb{C}$ it is commutative.
	2. Is this a necessary condition for $H(A)$ to be commutative?

Every $a\in A$ defines an element $i(A)\in H(A)$ that sends $x\mapsto ax$. This extends to a $\mathbb{C}$-algebra homomorphism $i:A\to H(A)$ whose kernel is $1_A$, hence $i$ is injective.

Define inductively
- $D(0)=i(A)$
- $D(m)=\{P\in H(A)\mid [P,D(0)]\subset D(m-1)\}$ for $m\geq 1$.

Then 
- The $\mathbb{C}$-algebra of *$\mathbb{C}$-linear differential operators on $A$* is given by $$D(A)=\bigcup_m D(m).$$ 
# Examples
**1** ([ring of differential operators on convergent power series](<notes/ntpy/ring of differential operators on convergent power series.md>))

# Properties
1. $D(m)D(k)\subset D(m+k)$ and $D(m)\subset D(m+1)$.
2. $D(A)$ is a positively filtered ring. The filtration $\{D(m)\}$ gives the associated graded ring $$GD(A)=\bigoplus_{m\geq 0}D(m)/D(m-1),$$where $D(-1)=0$ so that $G_0D(A)=D(0)$. 
3. $GD(A)$ is a commutative $\mathbb{C}$-algebra.

*Proofs*
**1**
