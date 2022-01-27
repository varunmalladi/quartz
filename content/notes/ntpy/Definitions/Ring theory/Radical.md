---
title: "Radical"
---

Let $A$ be a commutative ring.

# Definition
## Radical

**Definition.** The _radical_ of an ideal $I\subset A$, denoted $Rad(I)$, is the set
$$
Rad(I)=\{ a\in A \mid a^N\in I \text{ for some } n\in\mathbb{N} \}.
$$

Intuitively, this is like the set of all roots of elements in $I$. 

## Nilradical
**Proposition.** The set $\mathfrak{N}$ of all [nilpotent](notes/ntpy/Definitions/Ring theory/Nilpotent.md) elements in $A$ form an ideal called the _nilradical_, and $A/\mathfrak{N}$ has no nilpotent elements $\neq 0$.

Equivalently, it is the intersection of all prime ideals (Of nilradical, Property 1).

_Proof._ For any $x\in\mathfrak{N}$, there exists $N$ such that $x^N=0$. Then clearly $(ax)^N=0$ for any $a\in A$. It remains to show that $\mathfrak{N}$ is an additive subgroup. Let $x,y\in\mathfrak{N}$. Let $x^m=y^n=0$. By the binomial theorem, $(x+y)^{m+n-1}$ has each term is a product of $x^ry^s$ where $r+s=m+n-1$. But then either $r\geq m$ or $s\geq n$, so it vanishes. Hence $x+y\in\mathfrak{N}$. Hence $\mathfrak{N}$ is an ideal.

If $\bar{X}\in A/\mathfrak{N}$ is such that $\bar{X}^n=0$, then its preimage $x$ is such that $x^n\in\mathfrak{N}$ (it is either 0 or vanishes under the quotient). But then $x\in\mathfrak{N}$, so $\bar{x}=0$. $\square$

### Jacobson radical
**Definition.** The intersection of all maximal ideals of $A$ forms an ideal called the _Jacobson radical_.

# Properties
- $I\subset Rad(I)$.
- It is the preimage of the ideal of [nilpotent](notes/ntpy/Definitions/Ring theory/Nilpotent.md) elements under the natural quotient map $R\to R/I$.
3. $\text{rad}(IJ) = \text{rad}(I\cap J) = \text{rad}(I)\cap\text{rad}(J)$.

### Proofs
#### 3
First we will show that $\text{rad}(IJ)\subseteq\text{rad}(I\cap J)$. Let $\alpha^r\in IJ$. Then $\alpha^r$ can be written as a finite sum where each summand is the product of an element in $i$ and an element in $j$. But then each term is in $I\cap J$, so $\alpha^r\in I\cap J$, so $\alpha\in\text{rad}(I\cap J)$.

Now we will show that $\text{rad}(IJ)\supseteq\text{rad}(I\cap J)$. Let $\alpha^r\in I\cap J$. Then $\alpha^r\alpha^r=\alpha^{2r}\in IJ$, so $\alpha\in\text{rad}(IJ)$.

Next we will show that $\text{rad}(I\cap J)\subseteq\text{rad}(I)\cap\text{rad}(J)$. Let $\alpha^r\in I\cap J$. Then $\alpha^r\in I$ and $\alpha^r\in J$ so $\alpha\in\text{rad}(I)\cap\text{rad}(J)$. 

Finally, we will show that $\text{rad}(I\cap J)\supseteq\text{rad}(I)\cap\text{rad}(J)$. Let $\alpha^r\in I$ and $\alpha^s\in J$. Then $\alpha^{r+s}\in I\cap J$, so $\alpha\in\text{rad}(I\cap J)$. 

## Of nilradical
1. The nilradical is equivalently the intersection of all prime ideals in $A$.

## Of Jacobson radical
1. The Jacobson radical can be equivalently defined as $$ \text{Jac}(A)=\{x\in A\mid 1-xy\text{ is invertible }\forall y\in A\} $$