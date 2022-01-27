---
title: "Finite Mult. Subgroup of Field is Cyclic"
---

---
title: "Finite Mult. Subgroup of Field is Cyclic"
---

# Statement
Let $K$ be a field and $K^\ast$ be its multiplicative group. Suppose $G\subset K^\ast$ is a finite subgroup. Then $G$ is cyclic.

# Proof
**Lemma 1.** For all $d$, the number of elements of order just $d$ in $G$ is either 0 or $\phi(d)$.

_Proof._ Suppose there exists $a\in G$ of order $d$. Consider the elements $1, a,\dots, a^{d-1}$. They are all different, and all are such that $x^d=1$.

In $K^\ast$, we can rewrite the identity $x^d=1$ as $x^d-1=0$, since it is a subgroup of a field. This has no more than $d$ solutions by Bezout's theorem. Then they must be exactly the ones listed above, of which there are $d$. 

So if an $a_i$ above itself has _order_ $d$, it has $d$ distinct powers that are also solutions to $x^d-1=0$. But these must be the same as the $d$ distinct $a_k$. In other words, this $a_i$ must generate $\langle a\rangle$, which suggests $\phi(i,d)=1$. Q.E.D.

**Remark.** We did not use the finiteness of the theorem's assumptions in the proof of the lemma.

**Lemma 2.** 
$$
\sum_{d\mid w}\phi(d)=w.
$$

_Proof of theorem._ Suppose $G$ has order $w$. The order of any element in $G$ must divide $w$. Thus
$$
\sum_{d\mid w}(\# \text{elts of order } d)=w
$$
Lemma 2 states that
$$
\sum_{d\mid w}\phi(d)=w.
$$
Using Lemma 1, we conclude that for all $d\mid w$, the number of elements of order $d$ in $G$ is $\phi(d)$, so in particular the number of elements of order $w$ in $d$ is $\phi(w)\neq 0$. But this implies the group is cyclic. QED. 
