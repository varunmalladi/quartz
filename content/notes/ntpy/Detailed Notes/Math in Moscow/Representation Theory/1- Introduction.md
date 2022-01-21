---
title: "1- Introduction"
---

**Definition.** Let $G$ be a group and $\mathbb{F}$ a field. Let $V$ be a vector space over $\mathbb{F}$. Then a homomorphism
$$
T:G\longrightarrow GL(V)
$$
is called a _representation_ of $G$. The _dimension_ of $T$ is the dimension of the vector space $V$.

The image forms a vector space under composition.

### Direct sum
Assume $T:G\to GL(V)$ and $S:G\to GL(V)$ are representations over $\mathbb{F}$. Then define $T\oplus S:G\to GL(V\oplus U)$ via
$$
(T\oplus S)(g)(v,u)\coloneqq (T(g)v,S(g)u),\quad\forall g\in G,\ v\in V,\ u\in U.
$$

### Irreducible representations
**Definition.** Assume $T:G\to GL(V)$ is a representation. A subspace $U\subset V$ is called _invariant_ with respect to $T$ if 
$$
T(g)u\in U,\quad \forall g\in G,\ u\in U.
$$
We can construct the representation $S\to GL(U)$ setting $S(g)$ to be the restriction of the automorphism $T(g)$ to the subspace $U$. $S$ is called a _subrepresentation_ of the representation $T$.

**Definition.** Assume $T:G\to GL(V)$ is a representatioin. $T$ is called _irreducible_ if it has no non-trivial invariant subspaces.

**Definition.** Assume $T:G\to GL(V)$ is a representation. $T$ is called completely reducible if for any invariant subspace $U$ there exists another invariant subspace $W$ such that $V=U\oplus W$.

It is an [open question](notes/ntpy/Questions/Is every gp representation completely reducible?.md) whether every representation is completely reducible, but the situation has been proven in the affirmative in the [finite dimensional](notes/ntpy/Key Ideas/Representation theory/Reducibility of finite dimensional representations.md) case.
