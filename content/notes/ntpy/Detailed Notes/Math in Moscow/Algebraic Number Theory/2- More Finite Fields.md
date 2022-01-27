---
title: "2- More Finite Fields"
---

# Lecture Notes
**[Theorem 1.7.](notes/ntpy/Theorems/Field Theory/Finite Fields of Prime Power Order.md)** Let $p$ be prime, and $f$ be a positive integer. Let $q=p^f$. Let $\Omega$ be an algebraically closed field with characteristic $p$. Then:
1. $x^q-x=0$ has $q$ different solutions in $\Omega$. The set of the solutions is a subfield, call it $\mathbb{F}_q$.
2. For all $p$, $\Omega$ does exist. For any field $K$ such that $|K|=q$, there exists an isomorphism $K\cong \mathbb{F}_q$, i.e. this is the only finite field of that order.
3. $\mathbb{F}_p\cong\mathbb{Z}_p$ (in one sense) and $\mathbb{F}_q \supset\mathbb{F}_p$.

We now wish to study the squares in a finite field.

**[Theorem.](notes/ntpy/Theorems/Field Theory/Field Characteristic and Squares.md)** Let $p$ be prime and $f$ a positive integer. Let $K=\mathbb{F}_q$ be a field of characteristic $p$. Then 
1. If $p=2$, then every element in $K^\ast$ is a square.
2. If $p\neq 2$, then the subset of squares form a subgroup of $K^\ast$ of index 2. This subgroup coincides with the kernal of the map

\begin{gather}
K^\ast\to\{\pm 1\} \\
x\mapsto x^{(q-1)/2}.
\end{gather}


In what follows, assume the characteristic of the field is not 2 unless otherwise stated.

**[Definition](notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Legendre Symbol.md).** Let $a$ be any residue modulo $p$. The Legendre symbol is 
$$
\left(\frac{a}{p}\right)\coloneqq a^{(p-1)/2} 
$$

Recall that if $a\neq 0$ then $\left(\frac{a}{p}\right)=\pm 1$.

Define $\left(\frac{0}{p}\right)=0$.

**Theorem (Quadratic Reciprocity).** Let $p$ and $l$ be two distinct primes. Then 
$$
\left(\frac{p}{l}\right)\left(\frac{l}{p}\right) = (-1)^{\frac{p-1}{2}\frac{l-1}{2}}.
$$

