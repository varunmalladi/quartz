---
title: "Representation of a group"
---

# Definition
## Traditional definition

**Definition.** Let $G$ be a group and $\mathbb{F}$ a field. Let $V$ be a vector space over $\mathbb{F}$. Then a homomorphism
$$
T:G\longrightarrow GL(V)
$$
is called a _representation_ of $G$. The _dimension_ of $T$ is the dimension of the vector space $V$.

The image forms a vector space under composition.

**Definition.** A representation is said to be *faithful* if its kernel is trivial.

### Morphisms

**Definition.** A morphism of representations $T:G\to GL(V)$ and $S:G\to GL(U)$ is a map $A\in [V,U]$ such that $$ AT(g)=S(g)A$$$$ for all $$\in $G$.

**Definition.** The representations $T:G\to GL(V)$ and $S:G\to GL(U)$ are isomorphic if there is a morphism between them that is bijective with respect to their vector spaces.

### Irreducible representations
**Definition.** Assume $T:G\to GL(V)$ is a representation. A subspace $U\subset V$ is called _invariant_ with respect to $T$ if 
$$
T(g)u\in U,\quad \forall g\in G,\ u\in U.
$$
We can construct the representation $S\to GL(U)$ setting $S(g)$ to be the restriction of the automorphism $T(g)$ to the subspace $U$. $S$ is called a _subrepresentation_ of the representation $T$.

**Definition.** Assume $T:G\to GL(V)$ is a representatioin. $T$ is called _irreducible_ if it has no non-trivial invariant subspaces.

**Definition.** Assume $T:G\to GL(V)$ is a representation. $T$ is called completely reducible if for any invariant subspace $U$ there exists another invariant subspace $W$ such that $V=U\oplus W$.

It is an [open question](notes/ntpy/Questions/Is every gp representation completely reducible?.md) whether every representation is completely reducible, but the situation has been proven in the affirmative in the [finite dimensional](notes/ntpy/Key Ideas/Representation theory/Reducibility of finite dimensional representations.md) case.

**Proposition.** Let $A\in\text{Mor}(T,S)$ be a morphism between irreducible representations.

## Categorical definition

Every group $G$ can be regarded as a category with a single object whose morphisms are precisely the elements of the group.

**Definition.** A _linear representation of $G$ over $F$_ is a functor $G\to\text{Vect}_F$. The functor category is called the _category of linear representations of $G$ over $F$_.

- At first it may not be clear how this lines up with the traditional definition, in which a representation is a map from $G$ to the automorphism group of $V$ (as opposed to just $V$). A functor between categories covariantly induces a group homomorphism between the automorphism groups (see [Automorphisms of a category](notes/ntpy/Definitions/Category theory/Automorphisms of a category.md)). So a functor contains exactly the information of the traditional definition.
- Morphisms of representations are natural transformations in the corresponding category of linear representations. By definition, if $S$ and $T$ are representations, then a morphism $\phi:S\to T$ is a commuting diagram of the form $$\begin{array} sG & \overset{S}{\rightarrow} & \text{Vect}_F \\ \downarrow & & \downarrow \\ G & \overset{T}{\rightarrow} & \text{Vect}_F \end{array}.$$ The map on the left is the identity. Also, every representation defined as a functor is in bijection with a group homomorphism from $G$ to the automorphism group of the vector space $V$ it is acting on, which are (invertible) maps $V\overset{g}{\to}V$. So diagrams of the form above are in bijection with commuting diagrams of the form $$\begin{array} sV & \overset{\phi}{\rightarrow} & W \\ \llap{g}{\downarrow} & & \llap{g}{\downarrow} \\ V & \overset{\phi}{\rightarrow} & W \end{array}$$ for all $g\in G$, which matches the traditional definition.

**Definition.** A *faithful representation* is a [faithful functor](notes/ntpy/Definitions/Category theory/Full, faithful functors.md) in the category of representations.

- We should check that this matches with the notion of a faithful representation in the traditional definition. Let $T$ be a representation, in the sense that it is a functor. In particular $T$ can be regarded as a morphism of groups by our remarks above. Suppose the kernel of $T$ (regarded as a morphism of groups) is just the identity on $G$. Now suppose $T(g)=T(h)$. Then $T(g)T(g^{-1})=T(h)T(g^{-1})$ so $T(hg^{-1})=1$ so $h=g$. Conversely, suppose $T$ is a faithful functor. If $T(g)=1$, then by definition of a faithful functor $g$ must be the identity morphism on $G$, which is precisely the identity group element.

### Irreducible representations
We claim that the traditional definition of irreducible representations coincides with that of [simple objects](notes/ntpy/Definitions/Category theory/Simple objects.md) in the category of representations.

One direction is clear. If a representation $T$ is reducible, then there is an [epimorphism](notes/ntpy/Definitions/Category theory/Mono, epimorphisms.md) from it to one of its nontrivial subrepresentations. It remains to show that a simple object is an irreducible representation. Let $S$ be a simple object, say acting on a vector space $V$. Then its only [quotient objects](notes/ntpy/Definitions/Category theory/Subobjects, quotient objects.md) are itself and 0. This means that there are no nontrivial subspaces $U\subset V$ such that $S'=S\mid_U$ is a representation, for then $S\to S'$ would be an epimorphism. Hence $S$ is irreducible.

### Dual
The [dual object](notes/ntpy/Definitions/Category theory/Dual object.md) in the category is the internal hom from the object to the [unit object](notes/ntpy/Definitions/Category theory/Unit object.md). We claim that the traditional definition of the dual representation is equivalent to taking the dual object of a representation when viewed as an object in the category of representations. 

By the definition of a dual object that we have just given, we need to check $[T,I]$ where $T$ is an arbitrary representation and $I$ is the unit (below we spell out that this is the trivial representation on the base field $K$). By the above discussion, the set of morphisms $[T,I]$ is in bijection with squares of the form 
$$
\begin{array}
zV & \rightarrow & K \\
\llap{{}^g}{\downarrow} & & \llap{{}^{1_K}}{\downarrow} \\
V & \rightarrow & K
\end{array}
$$
for all $g\in G$. These are equivalent to $\text{Hom}(V\overset{g}{\to}V,K)$. By contravariance this is equivalently a map $\text{Hom}(V,K)\to\text{Hom}(V,K)$ defined by sending $f\mapsto g^{-1}f$. (The map defined by $g$ lives in the opposite category of $G$ hence we need to invert it). 

So we can see that for $T^\ast(g)$ it must be the case that $f(gv)=f(g^{-1}(v))$. We can then write this as in the traditional definition: $T^\ast(g)=(T(g^{-1}))^\ast$.

### Properties
- Monoidal category
	- The tensor product of linear representations makes the category of linear representations a monoidal category.
	- The unit is the trivial representation on the base field (see below)
	- Generally, this is true if the target category is monoidal, for example $\text{Vect}_F$ is monoidal.

# Reducibility and Decomposability
A representation is *decomposable* if it can be written as the direct sum of nontrivial subrepresentations. This might seem like the same thing as a reducable representation, but it is not.

While every irreducible representation is indecomposable, not every indecomposable representation is irreducible. This is the intuition that a representation may only have a single non-trivial representation. 

However, if $G$ is finite and $\text{char}(k)\nmid |G|$, then the two notions coincide. In particular, every indecomposable representation is irreducible. (Property 5)

If you notice, this is a condition under which [Maschke's Theorem](notes/ntpy/Theorems/Representation theory/Maschke's Theorem.md) is stated. It is because it is a direct corollary of (Property 5): just use induction. If the representation is infinite dimensional, you need the [Axiom of Choice](notes/ntpy/Theorems/Axiom of Choice.md) to say anything.

# Operations
- Direct sum (of representations is a representation)
	- $(T\oplus S)(g)(v,u)\coloneqq (T(g)v,S(g)u),\quad\forall g\in G,\ v\in V,\ u\in U$
- Tensor product
	- If $S:G\to V$ and $T:G\to W$ are representations, then $S\otimes T$ is a representation defined by \begin{gather} T\otimes S: G\longrightarrow \text{GL}(V\otimes W) \\ g(v\otimes w)=gv\otimes gw. \end{gather}
	- That this a representation follows from property 2 [here](notes/ntpy/Definitions/Linear algebra/Tensor product of vector spaces.md).
	- The unit object is the trivial representation sending each $g\in G$ to the identity automorphism on the base field $K$. To see this, consider that in $T\otimes 1$, we have $g(v\otimes k)=gv\otimes gk=gv\otimes k$. Thus there is a natural isomorphism $T\otimes 1\to T$ given by the projection $p_V$ onto the $V$ factor: $$ \begin{array} zV\otimes K & \rightarrow & V \\ \llap{{}^{g\otimes 1}}{\downarrow} & & \rlap{\ \ {}^{g}}{\downarrow} \\ V\otimes K & \rightarrow & V \end{array}.$$ This is well defined since every element in $V\otimes W$ is a linear combinations of elementary tensors (these have the form $v\otimes w$) so the projection map will send an element to the sum of the $V$ factors in its expression as a linear combination of elementary tensors.
- Dual 
	- Define $T^\ast:G\to\text{GL}(V^\ast)$ by $$ T^\ast(g)=(T(g^{-1}))^\ast. $$
	- $T^\ast$ is a representation over $V^\ast$.
	- $(T(g))^\ast = (T(-n))^t$
- Symmetric / antisymmetric ([definition](notes/ntpy/Definitions/Linear algebra/Tensor product of vector spaces.md))
	- $(S^2 T)(g)\coloneqq S^2(T(g))\coloneqq T(g)\mid_{S^2(V)}$
	- $(\Lambda^2 T)(g)\coloneqq\Lambda^2(T(g))\coloneqq T(g)\mid_{\Lambda^2(V)}$
- Equivalent representations: multiplying by an invertible matrix
	- Given a representation $\rho$ and an invertible matrix $T$, you can define a representation $\sigma(g) = T^{-1}\rho(g)T$. 
	- If the degree of a representation $\rho$ is 1, or the representation is trivial, then the only equivalent representation to $\rho$ is $\rho$ itself.

# Properties

- Given a morphism between representations, the kernel and image are invariant subspaces (wrt to the source and target representations)
- A morphism between irreducible representations is either trivial or an isomorphism.
- The image of a faithful representation is isomorphic to the group
- [Schur's Lemma](notes/ntpy/Theorems/Representation theory/Schur's Lemma.md) All endomorphisms of irreducible complex representations are one-dimensional
5. If $G$ is finite and $\text{char}(k)\nmid |G|$, then every indecomposable representation is irreducible.
	1. If $U$ is a nontrivial invariant subrepresentation of $T$, then there exists a complementary invariant subresentation $V$ such that $T=U\oplus V$. 
- [Maschke's Theorem](notes/ntpy/Theorems/Representation theory/Maschke's Theorem.md) The representation of a finite group whose order is not divisible by the characteristic of the field is completely reducible.