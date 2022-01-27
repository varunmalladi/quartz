---
title: "Associated primes"
---

---
title: "Associated primes"
---

# Definition
Let $R$ be a ring and let $M$ be an $R$-module.

**Definition.** A prime $P$ of $R$ is _associated_ to $M$ if $P$ is the [Annihilator](notes/ntpy/Definitions/Ring theory/Annihilator.md)<notes/ntpy/Definitions/Ring theory/Annihilator.md>) of an element of $M$. $$\text{Ass}(M)=\{\mathfrak{p}\in\text{Spec}(A)\mid \exists m\in M\text{ st }\text{Ann}(m)=\mathfrak{p}\}.$$

The set of all primes associated to $M$ is written $\text{Ass}_R M$ or $\text{Ass}M$. If $I$ is an ideal, then by the associated primes of $I$ we really mean the associated primes of $R/I$.

# Properties
1. Let $R$ be a [Noetherian ring](notes/ntpy/Definitions/Ring theory/Noetherian ring.md)<notes/ntpy/Definitions/Ring theory/Noetherian ring.md>) and let $M$ be a finitely generated nonzero $R$-module.
	1. $\operatorname{Ass}M$ is a finite, nonempty set of primes, each containing $\operatorname{ann}M$. The set $\operatorname{Ass}M$ includes all the primes minimal among primes containing $\operatorname{ann}M$.
	2. The union of the associated primes of $M$ consists of 0 and the set of zero divisors on $M$.
	3. The formation of $\operatorname{Ass}M$ commutes with [localization]()<notes/ntpy/Definitions/Ring theory/Localization of a ring.md>): $$ \operatorname{Ass}_{R_U}M_U=\{\mathfrak{p}\cdot R_U\mid \mathfrak{p}\in\operatorname{Ass}M\text{ and }\mathfrak{p}\cap U=\emptyset\}.$$
2. Let $R$ be a ring and let $M$ be a nonzero $R$-module. If $I$ is an ideal of $R$ maximal among all ideals of $R$ that are annihilators of elements of $M$, then $I$ is prime (and thus belongs to $\operatorname{Ass}M)$. In particular, if $R$ is Noetherian then $\operatorname{Ass}M$ is nonempty.
3. The following:
	1. If $M=M'\oplus M''$, then $\operatorname{Ass}M=(\operatorname{Ass}M')\cup(\operatorname{Ass}M'')$.
	2. More generally, given a short-exact sequence of $R$-modules $$0\to M'\to M\to M''\to 0$$ we have $$\operatorname{Ass}M'\subset\operatorname{Ass}M\subset (\operatorname{Ass}M')\cup(\operatorname{Ass}M'').$$
4. If $R$ is a Noetherian ring and $M$ is a finitely generated $R$-module, then $M$ has a filtration $$0=M_0\subset M_1\subset\cdots\subset M_n=M$$ with each $M_{i+1}/M_i\cong R/P_i$ for some prime ideal $P_i$. 

# Examples
1. $\text{Ass}(A/\mathfrak{p})=\{\mathfrak{p}\}$
2. $\text{Ass}(A/\mathfrak{p}^n)$
