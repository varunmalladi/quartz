---
title: "Finite fields"
---

# Definition

# Properties
1. $\mathbb{F}_{p^m}\subset\mathbb{F}_{p^n}$ iff $m\mid n$.

#### Proofs
##### 1
Every $\sigma\in\sum_{K/k}^{K/k}$ fixes $k$ by definition. Letting $k=\mathbb{F}_p$ and $K=\mathbb{F}_{p^n}$, this means $\sigma$ is a map such that $\alpha^p=\alpha$ for all $\alpha\in\mathbb{F}_p$. Thus $\sum_{K/k}^{K/k}$ is generated by the Frobenius map $\alpha\mapsto\alpha^p$. We can see that $n$ unique maps are generated. By ([Field extension](<notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Field extension.md>), Property ??) every $\sigma$ is an automorphism.

Recall that $|\mathbb{F}_{p^n}|=p^n$, and its elements precisely satisfy the polynomial $X^{p^n}-X=0$. This implies that $\mathbb{F}_{p^n}/\mathbb{F}_p$ is [Galois](<notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Galois extension.md>). By our discussion above, $\text{Gal}(\mathbb{F}_{p^n}/\mathbb{F}_p)=C_n$, the cyclic group of order $n$. It is a basic fact that $A$ is a subgroup of $C_n$ if and only if $|A|\mid n$ (and moreover this subgroup is the unique one of its order). By the [Fundamental thm of Galois Theory](<notes/ntpy/Theorems/Field Theory/Fundamental thm of Galois Theory.md>), the subfield of $\mathbb{F}_{p^n}$ corresponding to $A$ is the one which is fixed under $A$. Suppose $|A|=m$. Then the elements of $A$ correspond to applying the Frobenius map up to $m$ times. The unique field (hence the subfield in question) that is fixed under such maps is $\mathbb{F}_{p^m}$. Due to the Galois correspondence, this shows the claim.