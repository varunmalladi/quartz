---
title: "Field Characteristic and Squares"
---

**Theorem.** Let $p$ be prime and $f$ a positive integer. Let $K=\mathbb{F}_q$ be a field of characteristic $p$. Then 
1. If $p=2$, then every element in $K^\ast$ is a square.
2. If $p\neq 2$, then the subset of squares form a subgroup of $K^\ast$ of index 2. This subgroup coincides with the kernal of the map

\begin{gather}
K^\ast\to\{\pm 1\} \\
x\mapsto x^{(q-1)/2}.
\end{gather}


_Pf of statement 1._ In this case, the Frobenius map, which is an automorphism ([lemma.](notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Frobenius Map.md)), coincides with the operation of squaring.

_Pf of statement 2._ Consider $K$ as a subfield of an algebraically closed field $\Omega$ of characteristic $p$. If $a\in K$ then $x^2 = a$ has a solution in $\Omega$ since $\Omega$ is algebraically closed. Then $(x^{q-1})^2 = (x^2)^{q-1}=a^{q-1}=1$  since $a\in K$. But there are only two roots of $1$, namely $1$ and $-1$. If $x^{q-1}=1$ then $x\in K$ by definition, so $a$ is a square. Otherwise, if $x^{q-1}=-1$, then $x\not\in K$ since $x$ does not have order $q-1$. Thus $a$ is not a square. $x^{q-1}=1$ is equivalently $a^{(p-1)/2}$. This shows that the squares coincide with the kernel of the map $K^\ast\to\{\pm 1\}$ above.

It remains to show that the subgroup of squares has index to in $K^\ast$. It suffices to show that the map $K^\ast\to\{\pm 1\}$ above is surjective. This is because surjectivity would imply that $K^\ast$ modulo the kernel has order 2, i.e. that the subgroup of squares has index 2. To that end, we just need to find a single element that maps to $-1$, and the generator of $K$ suffices: it has order $q-1$, so certainly its $\frac{q-1}{2}$ power is not 1.
