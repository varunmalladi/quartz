---
title: "Artinian ring"
---

# Definition
## Rings
Let $A$ be a commutative ring.

**Definition.** $A$ is called *Artinian* if every ascending chain of ideals stabilizes, i.e. for every chain is of the form
$$
J_1\supseteq J_2\supseteq\dots\supseteq J_i\supseteq\cdots
$$
where $J_i=J_{i+1}=\dots$.

## Modules
Let $M$ be an $A$-module.

**Definition.** $M$ is *Artinian* if every ascending chain of submodules stabilizes.

# Properties
1. Every Artinian ring is Noetherian. (The converse may fail.)
2. Artinian rings are [Noetherian rings](ntpy/Definitions/Ring theory/Noetherian ring.md) of [dimension](ntpy/Definitions/Ring theory/Dimension of ring.md) 0. 
	1. This is equivalent to saying every prime ideal is maximal.
3. Lemma
	1. Submodule of a Artinian module is Artinian
	2. Let $\phi:M\to N$ be a surjective module homomorphism. Then if $M$ is Artinian then $N$ is Artinian.
	3.  Given a sequence $$0\to N\to M\to M/N\to 0$$ if $N$ and $M/N$ are Artinian then so is $M$.
4. The [Jacobson radical](ntpy/Definitions/Ring theory/Radical.md) is [nilpotent](ntpy/Definitions/Ring theory/Nilpotent.md).
5. There are finitely many maximal ideals

# Examples
1. Fields
2. $k[X]/(f_1^{n_1}\cdots f_k^{n_k})$
	1. $k[X]/(X^n)$
3. $\mathbb{Z}/n\mathbb{Z}$
