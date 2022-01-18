# Definition
Let $A$ be a (commutative) ring.

**Definition.** An ideal $p\subset A$ is called _prime_ if the following equivalent conditions are met:
1. For every $a,b\in A$ such that $ab\in p$ either $a\in p$ or $b\in p$.
2. For every $a\not\in p$ and $b\not\in p$ then $ab\not\in p$.
3. $A/p$ is an [[Integral domain|integral domain]].

**Theorem.** The intersection of all prime ideals of $A$ is the [[Nilpotent|nilradical]] $Nil(A)$.

## Over / under
### Integral extensions
([[integral extensions]])

Let $\mathcal{O}$ be a [[dedekind domain]], $k$ its field of fractions and $K/k$ a finite separable [[Field extension|extension]]. Let $\mathcal{O}_K$ be the integral closure.

The prime ideal $\mathfrak{B}\subset\mathcal{O}_K$ lies over the prime ideal $\mathfrak{p}\subset\mathcal{O}$, denoted as $\mathfrak{B}\mid\mathfrak{p}$, iff $$\mathfrak{B}\cap\mathcal{O}=\mathfrak{p}.$$

([[extensions of p-adic absolute values]])

# Properties
1. The zero ideal is prime if and only if $A$ is an integral domain.
2. If $f:A\to B$ is a ring homomorphism, and $\mathfrak{q}$ is a prime ideal in $B$, then $f^{-1}(\mathfrak{q})$ is a prime ideal in $A$.
3. TFAE:
	1. $\mathfrak{q}$ lies over $\mathfrak{p}$
	2. $\mathfrak{p}\subset\mathfrak{q}$, by which we mean $\mathfrak{p}S\subset\mathfrak{q}$
	3. $\mathfrak{q}$ occurs in the factorization of $\mathfrak{p}S$.
#### Proofs
##### 1
For the forward direction, suppose the zero ideal is prime. Then if $xy=0$ either $x=0$ or $y=0$. This by definition makes $A$ an integral domain. Convsersely, suppose $A$ is an integral domain. Then if $xy=0$ either $x=0$ or $y=0$. This makes $(0)$ a prime ideal.
##### 2
$f^{-1}(\mathfrak{q})$ is the kernel of the quotient map $A\to B/f^{-1}(\mathfrak{q})$, hence $A/f^{-1}(\mathfrak{q})\cong B/\mathfrak{q}$. The latter is an integral domain since $\mathfrak{q}$ is prime, so the former is as well, meaning $f^{-1}(\mathfrak{q})$ is a prime ideal.
