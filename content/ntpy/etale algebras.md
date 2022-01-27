---
title: "etale algebras"
---

---
title: "etale algebras"
---

# Idea
Dual to [etale space](notes/ntpy/etale space.md)<notes/ntpy/etale space.md>) of [scheme](notes/ntpy/scheme.md)<notes/ntpy/scheme.md>)s.

Stable under [base change, ascent](notes/ntpy/Key Ideas/base change, ascent.md)<notes/ntpy/Key Ideas/base change, ascent.md>).

# Definition
Let $F$ b a field.
- An $F$-algebra $A$ is called *etale* if it is isomorphic to the direct product of finitely many finite seperable extensions of $F$: $$A\cong\prod_{i=1}^n K_i.$$
- $A$ is called *split* if $A=F\times\cdots\times F$.
# Properties
Let $A$ be an etale $F$-algebra. Fix a seperable closure $F^s/F$.

1. $A$ is unital
2. etale algebras form a category, $\text{Et}(F)$.
	1. objects are etale $F$-algebras
	2. morphisms are (unital) $F$-algebra homomorphisms.
3. $\text{Et}(F)$ is closed under base change.
	1. If $F'/F$ is any field extension, $A\otimes_F F'$ is an etale $F'$-algebra.
		1. If $A$ is split, so is $A\otimes_F F'$. (?)
	2. If $f\in F[X]$ is separable, then $F[X]/(f)$ is an etale $F$-algebra.
4. $\text{Et}(F)$ is closed under $\oplus$, $\otimes_F$.
5. If $A$ is a finite-dimensional $F$-algebra (not yet etale!), TFAE
	1. $A$ is an etale $F$-algebra.
	2. $A\otimes_F F^s$ is a split etale $F^s$-algebra.
	3. $A\otimes_F F'$ is a split etale $F'$-algebra for some $F'/F$.
6. Any $\phi\in\text{Mor}(\text{Et}_F)$ factors through a projection $K_i\to F^s$ for some $i$.
	1. $\text{Et}_F(A,F^s)=\bigsqcup_i\text{Et}_F(K_i,F^s)$.
	2. In [absolute galois group](notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/absolute galois group.md)<notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/absolute galois group.md>) we discuss that $\text{Et}_F(A,F^s)$ is acted on by the absolute galois group $G_F$. We may interpret the decomposition in (6.1) as the orbit decomposition of this action: $G_F$ can send an embedding $A\to F^s$ to product of conjugates of its $K_i$...
	3. In particular, $\text{Et}_F(A,F^s)\in G_F\text{Set}$. (cf. 8)
7. There is a functor \begin{gather}\text{Et}_F\to (G_F\text{Set})^{\text{op}}, \\ A\mapsto \text{Et}(A,F^s).\end{gather}
8. Let $S$ be a finite $G_F$-set. Consider $F^s$ as a discrete $G_F$-set. Then $G_F\text{Set}(S,F^s)$ is an etale algebra of degree (i.e. $\text{dim}_FA$) $|S|$.

*Proofs*
**3.1**
Since etale algebras are closed under (finite) products, it suffices to consider the case where $A=K$ is a finite seperable extension. In particular, if $A'=K\times K'$ and $K\otimes_F F'$, $K'\otimes_F F'\in\text{Et}_{F'}$ then $A'\otimes_F F'\cong (K\otimes_F F')\times (K'\otimes_F F')\in\text{Et}_{F'}$.

By the primitive element theorem, $K\cong F(\alpha)\cong F[X]/(f)$ where $f$ is the minimal polynomial of $\alpha$. Then

\begin{align}
K\otimes_F F'\cong& FX[](<>)/(f)\otimes_F F' \\
\cong& F'X[](<>)/(f) \\
\cong& \prod_i F'X[](<>)/(f_i) \\
\cong& \prod K_i'.
\end{align}

- the second line is [tensor product (commutative algebra)](notes/ntpy/tensor product (commutative algebra).md)<notes/ntpy/tensor product (commutative algebra).md>) in "Of algebras", properties 1 and 2
- the third line is by the [Chinese Remainder Theorem](notes/ntpy/Theorems/Ring Theory/Chinese Remainder Theorem.md)<notes/ntpy/Theorems/Ring Theory/Chinese Remainder Theorem.md>), namely letting $f=\prod_i f_i$ be the irreducible factorization over $F'$.

Now since $f$ is separable over $F$, $f$ remains separable over $F'\supset F$, and so each $f_i$ is separable over $F'$ so each $K_i'$ is finite separable. 

**4**
We will show closure under $\otimes_F$. 

**5**
(1=>2) By remarks under 3.1, it suffices to consider a seperable finite field extension $A=K=F(\alpha)=F[x]/(f)$. The argument is virtually identical, but in the last step we observe that since $F^s$ is separable, $F^s[x]/(f_i)=F^s[x]/(x-\alpha_i)=F^s$. 

(2=>3) Take $F'=F^s$.

(3=>1) Suppose there exists $F'$ such that $A\otimes_F F'$ is split etale. Then it is reduced (i.e. has no nilpotents) as it it the $n$-fold product of a fields, which has no nilpotents. Thus $A\subset A\otimes _F F'$ is also reduced.

- Lemma 1: If $A$ is a finite reduced $F$-algebra, then it has at most $[A:F]$ maximal ideals.
- Lemma 2: If $A$ is a finite reduced $F$-algebra, then $A$ is the product of fields.
- Proof: Let $\mathfrak{m}_1,\dots,\mathfrak{m}_n$ be maximal ideals of $A$. By [Chinese Remainder Theorem](notes/ntpy/Theorems/Ring Theory/Chinese Remainder Theorem.md)<notes/ntpy/Theorems/Ring Theory/Chinese Remainder Theorem.md>), $$0\to \bigcap_i\mathfrak{m}_i\to A\to\prod_i A/\mathfrak{m}_i\to 0$$ is exact. By lemma 1, we may assume the $\mathfrak{m}_i$ are all the maximal ideals. Then $\bigcap_i\mathfrak{m}_i=Nil(A)=0$ (the nilradical is 0 as there are no nilpotents). Thus $A$ is the product of fields.

So we may write $A\cong\prod_i K_i$, where $K_i=A/\mathfrak{m}_i$ are fields. $K_i$ is a finite extension of $F$ (the quotient must contain $F$ as $F\subset A$ and it is not contained in any maximal ideal). It remains to show that $K_i$ is separable.

Suppose $K=K_i$ is inseparable. Then $\text{char}(F)=p$ and there exists $\alpha\in K$ with minimal polynomial $g(x^p)$ for some $g(x)=x^n+a_{n-1}x^{n-1}+\cdots+a_0\in F[x]$ (this is just evidencing the fact that $[K:F]$ divides $p$). Now let $L=F(a_0^{1/p},\dots,a_{n-1}^{1/p})$. Then $g(x^p)=h^p$ for some $h\in L[x]$, namely $$g(x^p)=x^{pn}+a_{n-1}x^{p(n-1)}+\cdots+a_0 = (x^n+a_{n-1}^{1/p}x^{n-1}+\cdots+a_0^{1/p})^p=h^p.$$
So $$F(\alpha)\otimes_F L\cong F[x]/(g(x^p))\otimes_F L\cong L[x]/(g(x^p))\cong L[x]/(h^p).$$
This shows that $F(\alpha)\otimes_F L$ has nilpotent elements. But then so would $$F(\alpha)\otimes_F L\subset K\otimes_F L\subset A\otimes_F L\subset A\otimes_F L'$$ for any $L'$ containing both $L$ and $F'$ (certainly one exists, e.g. $LF'$). But $A\otimes_F F'$ is split etale over $F'$ by assumption, hence $A\otimes_F L'$ is split etale over $L'$ (Property 3.1). But $A\otimes_F L'$ cannot have nilpotents, being the product of fields. This is a contradiction.

**6**
The idea is that $K_i\subset F^s$. The only reason this isn't true for all $K_i$ is that the value of the hom might be 0 on some $K_i$, but it cannot be 0 on all $K_i$. 

**7**
Let $\phi:A\to B\in\text{Et}_F(A,B)$. Then for $B\overset{i}{\rightarrow}F^s\in\text{Et}_F(B,F^s)$, there is an induced map $(A\overset{\phi}{\rightarrow}B\overset{i}{\rightarrow}F^s)\in\text{Et}_F(A,F^s)$. So $\text{Et}_F(A\overset{\phi}{\to}B,F^s)$ induces a map $\text{Et}_F(B,F^s)\to\text{Et}_F(A,F^s)$.

**8**
The proof is broken into steps.
1. 
