---
title: "Absolute value"
---

Let $K$ be a field.

**Definition.** A map $\|\cdot\|\to\mathbb{R}_{\geq 0}$ is called an _absolute value_ when 
1. $\|x\|=0 \iff x=0$
2. $\|\cdot\|$ restricted to $K^\ast$ is a homomorphism $K^\ast\to\mathbb{R}^\ast_{\geq 0}$.
3. (Triangle inequality) $\|x+y\|\leq\|x\|+\|y\|$

**Definition.** An absolute value is called _nonarchimedean_ if 
$$
\|x+y\|\leq\max(\|x\|,\|y\|).
$$
Otherwise, it is called _archimediean_.

### Equivalence
**Definition.** The absolute values $\|\cdot\|_1$ and $\|\cdot\|_2$ are called _equivalent_ if either of the following holds:
1. $\|\cdot\|_2=\|\cdot\|_1^t$ for some $t>0$
2. They define the same topology on $K$.


## Properties
1. If $\|\cdot\|$ is nonarchimedean and $x\in K$ can be expressed as a finite sum of distinct $x_i$, then $\|x\|=\max_{i}\|x_i\|$.
2. Consider the standard ring homomorphism $i:\mathbb{Z}\to K$. (i(\mathbb{Z}) is either $\mathbb{Z}$ or $\mathbb{F}_p$ depending on the characteristic of $K$.) Then $\|\cdot\|$ is nonarchimedian if and only if for all $x\in i(\mathbb{Z})$ we have $\|x\|\leq 1$.
	1. If $\text{char}(K)\neq 0$ then any absolute value on $K$ is nonarchimedean.
- Let $k=K(x)$, the rational polynomials in $K$. Suppose $\|\cdot\|$ is a nontrivial absolute value whose restriction to $K$ is trivial. Then it is nonarchimedean and either \begin{gathered}\|x\|=s^{-v_P(x)}\quad s\in\mathbb{R},s>1,P\in K[T]\text{ irreducible }, \text{deg}(P)\geq 1\text{, or} \\ \|x\|=s^{\text{deg}(\text{numerator}(x))-\text{deg}(\text{denominator}(x))}\quad s\in\mathbb{R},s>1. \end{gathered}
	- These two are in fact the same, differing only by an automorphism of $K$.

_Proof of (2)._ For the forward direction, each $x\in i(\mathbb{Z})$ can be written as a sum of $1$s. Since $\|1\|=1$, the non-archimedean property ensures $\|x\|\leq 1$.

_Proof of (2.1)_ Every $x$ is such that $x^p=1$, so $\|x^p\|=1$ and since 1 is the only root of unity in $\mathbb{R}_{\geq 0}$ it follows $\|x\|=1$.

### Over a field
1. Let $K$ be a field and $\|\cdot\|$ be an absolute value on it. Then 
	1. Addition, subtraction, and multiplication, and absolute value are continuous functions.
	2. The absolute value may be extended to the completion of $K$, which is also a fieldd. It becomes an absolute value on the completion. If the original absolute value was nonarchimedean, so is the extended one.
	3. If the absolute value is nonarchimedean, then the set of absolute values of $K$ is the same as the set of absolute values of the completion of $K$.
2. Let $\|\cdot\|$ be a nonarchimedean absolute value on $K$. Suppose $K$ is complete with respect to this absolute value. Then 
$$
\sum_{i=1}^\infty x_i,\quad x_i\in K
$$
converges if and only if $\lim_{i\to\infty}x_i=0$.
3. Let $K/k$ be a finite [field extension](<notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Field extension.md>), with  absolute value $\|\cdot\|$ whose restriction to $k$ gives $k$ the structure of a complete metric space. Then the topology of the metric space $K$ coincides with the topology of $k^n$, i.e. the absolute value is entirely defined by its restriction to $k$.

### Examples
- The trivial absolute value has $\|0\|=0$ and $\|x\|=1$ otherwise.
