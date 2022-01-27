---
title: "Maximal ideal"
---

---
title: "Maximal ideal"
---

Let $A$ be a commutative ring with unit.

**Definition.** A proper ideal $M\subset A$ is called _maximial_ if any of the following equivalent conditions hold:
- $A/M$ is a field
- $M$ is not contained in any larger proper ideal.

**Corollary.** The set of invertible elements is contained in the complement of the union of all maximal ideals.

### Local rings
A ring with exactly one maximal ideal (e.g. a field) is called a [local ring]()<notes/ntpy/Definitions/Ring theory/Local ring.md>).

### Existence
**Theorem.** Every nonzero (commutative, with identity) ring has at least one maximal idea.

_Pf._ [Zorn's lemma](notes/ntpy/Theorems/Zorn's lemma.md)<notes/ntpy/Theorems/Zorn's lemma.md>)

**Corollary.** If an ideal $I\subset A$ is nontrivial (i.e. not $(1)$), then there exists a maximal ideal containing $I$.

**Corollary.** Suppose there exists $a\in A$ such that $a$ is not invertible. Then there exists a maximal ideal $M\subset A$ such that $a\in M$.

### Properties
1. Every maximal ideal is [prime]()<notes/ntpy/Definitions/Ring theory/Prime ideal.md>).
2. If $f:A\to B$ is a ring homomorphism and $\mathfrak{b}$ is a maximial ideal in $B$, then $f^{-1}(\mathfrak{b})$ is a prime ideal. (Not necessarily maximal.)
#### Proofs
##### 1
Let $I$ be the maximal ideal. By definition $A/I$ is a field, hence in particular an integral domain, hence $I$ is a prime ideal.
##### 2
In the [Prime ideal](notes/ntpy/Definitions/Ring theory/Prime ideal.md)<notes/ntpy/Definitions/Ring theory/Prime ideal.md>) we prove the result for prime ideals, and we have just showed every maximal ideal is a prime ideal. To give an example of where $f^{-1}(\mathfrak{b})$ is not maximal, consider the natural map $\mathbb{Z}\to\mathbb{Q}$. Take $\mathfrak{b}=(0)$. This is maximal because $\mathbb{Q}\setminus\{0\}$ is a field. But $\mathbb{Z}\setminus\{0\}$ is not a field.
