---
title: "Noetherian ring"
---

# Definition
## Rings
**Definition.** A _Noetherian ring_ is associative, commutative ring with identity $A$ such that one of the following equivalent conditions hold:
1. Every ideal $I\subset A$ is finitely generated, i.e. $\exists f_1,\dots,f_n\in I$ such that for all $a\in I$, $a=\sum a_i f_i$ where $a_i\in A$.
2. (Ascending chain condition) For all infinite chains $$ I_1\subset I_2\subset\cdots\subset I_k\subset\cdots $$ there exists $N$ such that $I_N=I_{N+1}=\cdots$.

**Proposition.** The conditions above are indeed equivalent.

## Modules
Let $M$ be an $A$-module.

**Definition.** $M$ is *Noetherian* if one of the following equivalent conditions hold:
1. Every ascending chain of submodules stabilizes.
2. Any submodule of $M$ is finitely generated.

### Properties

1. If $A$ is Noetherian and $I\subset A$ is some ideal, then $A/I$ is Noetherian.
2. **[[Hilbert basis theorem|Hilber basis theorem.]].** If $A$ is a Noetherian ring, then so is $A[x]$.
3. If $A$ is a Noetherian ring then $A^n$ is a Noetherian module.
4. Lemma
	1. Submodule of a Noetherian module is Noetherian
	2. Let $\phi:M\to N$ be a surjective module homomorphism. Then if $M$ is Noetherian then $N$ is Noetherian.
	3.  Given a sequence $$0\to N\to M\to M/N\to 0$$ if $N$ and $M/N$ are Noetherian then so is $M$.
	4.  A finitely generated module $M$ of a Noetherian ring $A$ is also Noetherian.
5. If $A$ is Noetherian then $A[[x]]$ is Noetherian (formal power series).
6. Nilradical is nilpotent (since it is f.g.)

### Examples
- Any [[Principal ideal domain|PID]] 
- Any field $K$
- For a Noetherian ring $A$, $A[x]$ is a Noetherian ring

# Dimension
- dimension 0: [[Artinian ring]]
- dimension 1: includes [[dedekind domain]]