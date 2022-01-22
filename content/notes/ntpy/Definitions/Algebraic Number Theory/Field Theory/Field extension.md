---
title: "Field extension"
---

# Definition
**Definition.** Let $K$ and $L$ be fields. An subfield inclusion $K\hookrightarrow L$ is called a _field extension_.

Any field homomorphism is automatically injective. A previous definition defined an extension as a field homomorphism, but typically we mean an actual inclusion, and in this view there is no data lost in the notation $K/L$. Specifically, there exist field homomorphisms which are not inclusions, consider the map $\mathbb{R}\to \mathbb{C}$ sending $1\mapsto i$.

# Types of extensions
- [Normal extensions](<notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Normal extensions.md>)
- [Separable extension](<notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Separable extension.md>)

## Morphisms
If $K_1$ and $K_2$ are field extensions over $k$, then a homomorphism of extensions $$K_1/k\to K_2/k$$ is a field homomorphism $K_1\to K_2$ that fixes $k$. We denote the set of all such morphisms $$\sum_{K_1/k}^{K_2/k}.$$

## Dimension
For any field extension $K\subset L$, notice that $L$ can be considered as an algebra over $K$; in particular $L$ is a vector space over $K$. The dimension of $L$ as a vector space over $K$ is called the dimension of the field extension. It is denoted $$[L:K].$$

We say that $K$ is _finitely generated_ if $$K=k(\alpha_1,\dots,\alpha_n).$$

## Normal extensions
Let $K$ be an algebraic extension of $k$ contained in an algebraic closure $\overline{k}$ of $k$. The following are equivalent:
1. All $\sigma\in\sum_{K/k}^{\overline{k}/k}$ have the same image
2. $K$ is the splitting field of a family of polynomials in $k[T]$.
3. Every irreducible polynomial in $k[T]$ which has a root in $K$ splits into linear factors in $K$

# Properties
Let $K_1$ and $K_2$ be field extensions over $k$, and $\sigma: K_1/k\to K_2/k$ a homomorphism of extensions. Let $P\in k[T]$. 

1. ([Zariski's lemma](<notes/ntpy/Theorems/Field Theory/Zariski's lemma.md>)) 
2. Let $\alpha\in K$ be algebraic over $k$. Let $P_\alpha$ be a monic irreducible polynomial such that $P_\alpha(\alpha)=0$. Then
	1. $P_\alpha$ exists and is unique
	2. $k_{P_\alpha}\cong k(\alpha)\cong k[\alpha]$

### Proofs
#### 2
Certainly $P_\alpha$ exists. We just need to show it is unique. By decomposing and dividing, we can assume that $P_\alpha$ is irreducible and monic. Suppose $Q$ is another monic irreducible polynomial such that $Q(\alpha)=0$. Suppose $Q\neq P_\alpha$. Then by the Euclidean algorithm  $P_\alpha G+QH=1$ for some $G,H\in k[T]$. This is impossible, since $P_\alpha(\alpha)=Q(\alpha)=0$. Hence $P=Q$. 

We first show that $k_{P_\alpha}\cong k[\alpha]$. Consider the map
$$
\begin{gather}
\phi:kT[](<>)\to K \\
\phi_k= 1_k \\
T\mapsto \alpha.
\end{gather}
$$
Clearly $\text{im}\phi=k[\alpha]$. Then 
$$
\phi(P_\alpha(T))=P_\alpha(\phi(T))=P_\alpha(\alpha)=0.
$$
So $P_\alpha\in\ker\phi$. Thus there is a surjection $$\bar{\phi}:k[T]/(P_\alpha)\to k[\alpha]$$. This is actually also injective since it is a field homomorphism: the domain is a field (see Example 1). It is the definition of $k_{P_\alpha}$. 

That these are isomorphic to $k(\alpha)$ is a matter of definition: $k(\alpha)$ is the minimal subfield of $K$ containing $k$ and $\alpha$, where $k[\alpha]$ is the minimal subring with the same property. We have just shown that $k[\alpha]$ actually a field, so the two notions coincide.

## Of morphisms
1. Algebraic elements are sent to algebraic elements.
	1. If $P(\alpha)=0$ for some $\alpha\in K_1$, then $P(\sigma(\alpha))=0$.
2. Let $K=k_P$. Then a homomorphism $\sigma:K/k\to L/k$ uniquely extends to a ring homomorphism $\tilde{\sigma}:k[T]\to L$ that fixes $k$ and $P(\tilde(T))=0$. 
	1. In this case the set $\sum_{K/k}^{L/k}$ coincides with the set of different roots of $P(T)$ in $L$.
	2. Conversely, a root of $P(T)$ in $L$ determines a homomorphism of field extensions.
3. Suppose $k\subset M\subset K$ where $K=M(\alpha)$ with $\alpha$ algebraic over $M$. Let $L/k$ be algebraically closed. Then any element $\sigma\in\sum_{M/k}^{L/k}$ could be extended to an element of $\sum_{K/k}^{L/k}$: $$ \begin{array} zM/k & \rightarrow & L/k \\ \downarrow & \rlap{{}^\exists}{\nearrow} & \\ K/k & & \end{array} $$
4. Suppose $K/k$ is algebraic (not necessarily finite), $L/k$ algebraically closed. Then $\sum_{K/k}^{L/k}$ is nonempty. If both $K/k$ and $L/k$ are algebraic and algebraically closed then any $\sigma\in\sum_{K/k}^{L/k}$ is an isomorphism.
	1. Compare with (Of algebraic field extensions, Property 5).

### Proofs
#### 1
We have 
$$
P(\alpha)=a_0+a_1\alpha+\cdots+a_n\alpha^n = 0.
$$
Since $\sigma$ fixes $k$, we use the properties of field homomorphisms to obtain
$$
\begin{align}
P(\sigma(\alpha)) =& a_0+a_1\sigma(\alpha)+\cdots+a_n\sigma(\alpha)^n \\
=& \sigma(a_0 + a_1\alpha+\cdots a_n\alpha^n) \\
=& \sigma(0)=0.
\end{align}
$$

#### 2
$k_P=k[T]/(P)$ so that an extension exists is obvious, and that it fixes $k$ follows by the definition of a field homomorphism. Then in particular $\tilde{\sigma}(P(T))=0=P(\tilde{\sigma}(T))$. We can move the $P$ to the outside since the ring homomorphism fixes $k$. 

The second point is the observation that since a homomorphism of field extensions has a unique extension $\tilde{\sigma}$ such that $P(\tilde{\sigma}(T))=0$, it must be the case that the homomorphism of field extensions sends $T$ to a root of $P(T)$ in $L$.

#### 3
By definition, $\sigma$ determines a field extension $L/M$. By (General, Property 2), $K=M(\alpha)=M_{P_\alpha}$. This is an extension over $M$. We want a homomorphism $M_{P_\alpha}/M\to L/M$. But $L$ is algebraically closed, so it has nontrivial roots of $P_\alpha$. Then by (Property 2.2) above, there exists such a field extension homomorphism, i.e. $\sum_{M(\alpha)/M}^{L/k}$ is nonempty. This clearly descends to an element in $\sum_{K/k}^{L/k}$. 

## Of dimensions
1. Suppose $K/k$ and $L/K$ are finite extensions. Then $$[L:K][K:k]=[L:k].$$

## Of algebraic closures
1. Algebraic closures always exist, and they are unique up to isomorphism
	1. For all fields $k$ there exists a field extension $\bar{k}/k$ such that $\bar{k}$ is algebraic over $k$ and $\bar{k}$ is algebraically closed.

### Proofs
#### 1
_Step 1_

We will construct an algebraic extension $K_1/k$ such that any nonconstant polynomial with coefficients in $k$ has a root in $K_1$.

_Step 2_




# Examples
1. [Definitions/Algebraic Number Theory/Field Theory/Minimal polynomial](<>)


## $k(\alpha)$
Suppose $K/k$ is an extension and $\alpha\in K$. The define $k(\alpha)$ to be the minimal subfield containing both $k$ and $\alpha$. 

To see what this means explicitly, observe that $k(\alpha)$ needs to be closed under addition and multiplication, as well as have inverses. These properties already hold for $k$, so it suffices to impose them for $\alpha$. Closure under addition and multiplication is equivalently saying for any $P\in k[T]$, we have $P(\alpha)\in k(\alpha)$. To also have multiplicative inverses, we need to also be able to divide by polynomials which are not zero on $\alpha$. Thus every element $a\in k(\alpha)$ can be represented as $a=\frac{P(\alpha)}{Q(\alpha)}$, where $Q(\alpha)\neq 0$. 

## $k(\alpha_1,\dots,\alpha_n)$
Similar to the above, this is the minimal subfield of $K$ containing $k$ and the $\{a_i\}$. Explicitly, this means that any element 
