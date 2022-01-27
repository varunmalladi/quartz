---
title: "central simple algebra"
---

# Definition
An $F$-algebra $A$ is called
- *central* if the center is equal to $F$, i.e. $$Z(A)=\{a\in A:ab=ba\ \forall b\in A\} = F\cdot 1_A.$$
	- Note that by our assumptions on $A$, we already have $F\subset Z(A)$.
- *simple* if there are no nontrivial two-sided ideals
- *division* if every nonzero element is invertible.

**Remark.** 
- If $A$ is division, then it is simple, hence $Z(A)$ is a field, hence $A$ is a central simple $Z(A)$-algebra.
- If $A$ is division, the obstruction to $A$ being a field is commutativity ([obstruction to division algebras being fields](notes/ntpy/Key Ideas/obstruction to division algebras being fields.md))
- Being simple is slightly weaker than being transitive ([simple is weaker than transitive](notes/ntpy/Key Ideas/simple is weaker than transitive.md))

Some more definitions:
- A central simple $F$-algebra $A$ is called *split* if $A\cong M_n(F)$.
- Let $A^{\text{op}}$ be the opposite algebra, which is the same set but with multiplication reversed, i.e. $a\cdot_{\text{op}}b=b\cdot a$.

# Examples
**1** (M_n(F))
The $n\times n$ matrices over $F$ form a CSA.

**2** (Quaternions)
The [quaternion algebra](notes/ntpy/quaternion algebra.md) forms a CSA.

# Properties
1. ([Artin-Wedderburn](notes/ntpy/Theorems/Artin-Wedderburn.md)) Let $A$ be a [central simple algebra](notes/ntpy/Definitions/central simple algebra.md) over $F$. Then
$$A\cong M_n(D),$$ where $D$ is a division $F$-algebra that is unique up to isomorphism.
2. Let $A,B$ be CSAs over $F$. Then $A\otimes_F B$ is a CSA
	1. $Z(A\otimes_F B)=Z(A)\otimes_F Z(B)$
3. $A\otimes_F M_n(F)\cong M_n(A)$
4. $A\otimes_F K$ is a CSA over $K$, where $K/F$ is a field extension.
5. $A$ is a CSA over $F$ iff there exists $K/F$ such that $A\otimes_F K$ is split.
	1. (harder result proved by Noether) $A$ is a CSA over $F$ iff there exists $K/F$ finite separable with $A\otimes_F K$ split (i.e. $A\otimes_F F^s$ splits?)
	2. In general, this is not $G$-equivariant. It is $G$-equivariant iff $A$ is split.
6. $A\otimes_F A^{\text{op}}\cong \text{Vect}_F(A,A)\cong M_n(F)$ 
7. $\text{dim}_FA=n^2$ for some $n\geq 1$.
	1. We call $n$ the *degree* of $A$.
8. Let $CSA_K(n)$ denote the $k$-isomorphism classes of split by $K$, degree $n$ CSAs over $k$. (i.e. $A\in CSA_K(n)$ is such that $A\otimes_k K$ is split). 
	1. This is a pointed set, with basepoint $[M_n(k)]$. 
	2. There is a basepoint preserving bijection $$CSA_K(n)\leftrightarrow H^1(G,PGL_n(K)),$$ where 

*Proofs*

**5**
To see that this is not generally $G$-equivariant, we could argue implicitly that if it where, then by [Galois descent](notes/ntpy/Galois descent.md) we'd have $A\cong (A\otimes_F K)^G\cong (M_n(K))^G\cong M_n(k)$, so that $A\cong M_n(k)$, which is generally not true. This shows that the isomorphism is $G$-equivariant iff $A$ is split.


