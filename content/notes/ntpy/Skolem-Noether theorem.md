---
title: "Skolem-Noether theorem"
---

# Statement
Let $B$ be a [central simple algebra](<notes/ntpy/Definitions/central simple algebra.md>) of finite dimension over $k$. Let $A$ be a (central simple?) $k$-algebra. Let $f,g:A\to B$ be $k$-algebra homomorphisms. Then
- there exists a unit $b\in B$ such that $$g(a)=b\cdot f(a)\cdot b^{-1}$$ for all $a\in A$.

# Corollaries
- Letting $A=B$ and $f=1_B$, we get that every automorphism of $B$ is an inner automorphism.
	- Over a field $K$, all automorphisms of $M_n(K)$ are inner, i.e. given by $M\mapsto CMC^{-1}$ for some invertible matrix $C$.

# Proof
First consider the case where $B=M_n(k)=\text{End}_k(k^n)$. So we may see $f,g$ as defining actions of $A$ on $k^n$. Let $V_f$, $V_g$ be the $A$-modules associated to these actions. Since $A$ is simple and $f$ is nonzero, $f$ must be injective. Thus $A$ is finite dimensional. 