# Idea
It is natural to want to study functions on mathematical objects of interest. In our case, functions are polynomials and the objects are algebraic sets. It is not useful to consider the polynomials which vanish on the set. The affine coordinate ring is the result of removing such polynomials from the overall [[Polynomial ring|polynomial ring]].

# Definition
**Definition.** If $Y\subseteq\mathbb{A}^n$ is an [[Algebraic subset|affine algebraic set]], then the *affine coordinate ring* of $Y$ is $$A(Y)=A/I(Y)$$, where $I(Y)$ is the ideal of functions in $A=k[x_1,\dots,x_n]$ that vanish on $Y$.

In particular, $A(-)$ is a contravariant functor.

# Properties
1. If $Y$ is an [[Affine variety|affine variety]], then $A(Y)$ is an integral domain and a finitely generated $k$-algebra.
	1. Any finitely generated $k$-algebra which is a domain is the affine coordinate ring of some variety.
2. $A(-)$ is a contravariant functor
