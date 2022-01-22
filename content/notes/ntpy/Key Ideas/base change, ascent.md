---
title: "base change, ascent"
---

# Vector spaces
Consider a field extension $L/K$. Given a $K$-vector space $W$, how may we extend this to an $L$-vector space? In what way can we do this "canonically"?

It turns out that $L\otimes_K W$ is an $L$-vector space, and there is a canonical embedding $W\to L\otimes_K W$ where on basis elements $e_i\mapsto 1\otimes e_i$. 
- We might see this as extending a $K$-basis for $W$ to an $L$-basis for "$W$".

Going "up" base fields like this is called ascent. Going "down" basefields is descent, see [Galois descent](<notes/ntpy/Galois descent.md>).

# Fields
Suppose we have two field extensions $K/F$ and $F'/F$. We wish to complete the analogy: $K/F$ is to $?/F'$.

At the very minimum, we want $\text{dim}_F(K)=\text{dim}_{F'}(?)$. But ideally we would actually want $?$ to be a field extension of $F'$, not just a $F'$-vector space.

As $F$-vector spaces, $K$ has dimension $[K:F]$ and $F'$ has dimension $[F':F]$. So if we want $?$ to have $F'$-dimensionn $[K:F]$, we need $?$ to have $F$-dimension $[K:F][F':F]$. 

By properties of tensor products, $K\otimes_F F'$ is a natural choice of such a space. Indeed, $\text{dim}_{F'}(K\otimes_F F')=[K:F]$. Unfortunately, $K\otimes_F F'$ is not generally a field extension of $F'$. That is,
- field extensions are not closed under base change.

This is one of the motivations for working with [etale algebras](<notes/ntpy/etale algebras.md>)s instead of field extensions.
