---
title: "discrete G-set"
---

# Definition
- A topological group is say to *act* (continuously) on a topological space $X$ if the action map $$G\times X\to X$$ is continuous
	- Here $G\times X$ has the product topology. 
	- The actual action is part of the data (it is not canonically defined or something)
- If $X$ is a set equipped with the discrete topology, then if $G$ acts on it we call $X$ a *discrete $G$-set*.

# Examples
**Galois actions**
See: [Galois group](notes/ntpy/Galois group.md)

- Let $K/F$ be a Galois extension, $G=\text{Gal}(K/F)$. 
- There is a natural action of $G$ on $K/F$ (by definition elements of $G$ are automorphisms of $K/F$).
- We can thus naturally view $K$ as a discrete $G$-set. 
- More generally, any $G$-stable subset $X\subset K^n$ is a discrete $G$-set (including $K^n$).
	- $G$-stable just means the image of $X$ under the group action is a subset of $X$ (as opposed to a subset of $K^n$ but not $X$).

Since $G$ is compact, we can see Property 2, that all orbits are finite, directly:
- An element $x\in K^n$ is of the form $(\alpha_1,\dots,\alpha_n)$, where each $\alpha_i\in K$. 
- The orbit of $x$ are the possible places an element $g\in G$ could send $x$. But for eachh $P_i$, $g$ permutes its roots. Hence there are only finitely many places each $\alpha_i$ could be sent, hence the orbit of $x$ is finite.

In fact, for each $\alpha\in F^s$ the orbit $G\alpha$ is precisely the set of roots of the minimal polynomial for $\alpha$. A minimal polynomial is seperable, irreducible, and monic. Conversely, any polynomial satisfying those conditions is the minimal polynomial of some element in $F^s$. So there is a bijection

\begin{gather}
\{G\alpha\}_{\alpha\in F^s} \quad \leftrightarrow \quad \{\text{monic, sep, irred, polys over }F\}, \\
G_\alpha = \{\alpha_1,\dots,\alpha_n\}\mapsto \prod_{i=1}^n(x-\alpha_i) \\ \{\text{roots of }f\text{ in }F^s\}\leftarrow f
\end{gather}

where $F^s$ denotes the separable closure.

One aspect of Grothendieck's Galois theory is the weaking of the left side (i.e. the set of orbits) to the set of finite $G$-sets (i.e. the set being acted on in finite). This is a weakening because we have just said that every orbit is finite, implying it is a finite $G$-set.

# Properties
1. $X$ is a discrete $G$-set iff the orbit $G_x\subset G$ is open for all $x\in X$.
	1. Recall the orbit is $Gx=\{gx\mid g\in G\}$. 
	2. Recall the stabilizer $G_x=\{g\in G\mid gx=x\}$.
2. By the orbit-stabilizer theorem, if $G$ is compact and $X$ is a discrete $G$-set, then all orbits $G_x$ are finite.
	1. The orbit-stabilizer theorem says there is a bijection $G/Gx = G_x$.
3. Forms a category, $G_F\text{Set}$.
	1. objects are discrete $G_F$-sets.
	2. morphisms are $G_F$-equivariant maps
		1. i.e. $f:S\to T\in \text{Set}$ such that $f(\sigma s)=\sigma f(s)$ for all $\sigma\in G$.

*Proofs*

**2**
Continuous image of compact set is bounded, so that $Gx\subset X$ is bounded...