---
title: "integral extensions"
---

# Idea
We wish to generalize the methods of field and Galois theory to (commutative) rings. A central notion in the aforementioned theory is that of [algebraic extensions](ntpy/Definitions/Algebraic Number Theory/Field Theory/Algebraic extensions.md): an extension $F\subset G$ is algebraic if every element in $G$ is the root of a polynomial with coefficients in $F$. 

An integral extension of a commutative ring $A$, say $A\subset B$, is such that every every element of $B$ is the root of a *monic* polynomial with coefficients in $A$. Algebraic extensions are integral extensions, because in a field we can just divide by the leading coefficient to obtain a monic polynomial. But why should we make this distinction when dealing with commutative rings?

The integral closure of a subring $A\subset B$ is the collection (which actually forms a ring) of integral elements of $A$ in $B$, i.e. roots of monic polynomials with coefficients in $A$ that are in $B$. The ring of integers refers to the specific case where $A=\mathbb{Z}$ and $B$ is a finite extension of $\mathbb{Q}$. We write this as $\mathcal{O}_B$. The ring of integers generalize the standard integers, in particular their relationship to $\mathbb{Q}$: $\mathcal{O}_\mathbb{Q}=\mathbb{Z}$. But what properties in particular are we capturing, and how does this tie back in with monic polynomials?

The necessity of the monic polynomial definition is seen as follows: given $a,b\in\mathbb{Z}^\ast$, the polynomial $aX+b$ has an integer solution iff $a=1$.

# Definitions
An **integrally closed domain** $A$ is an integral domain whose integral closure in its field of fractions is itself.

# Properties
1. For a finite extension $\mathbb{Q}\subset K$, it is not sufficient to define the ring of integers as the subring such that its field of fractions is $K$ (as is the case with $\mathbb{Z}$ and $\mathbb{Q}$). There may be several rings with this property.
2. $\mathcal{O}_K$ is a [Noetherian](ntpy/Definitions/Ring theory/Noetherian ring.md) integrally closed domain.
