---
title: "inj proj modules"
---

---
title: "inj proj modules"
---

# Definition
All modules will be assumed to be $A$-modules where $A$ is a commutative ring with identity.

Given any surjective map $$M\overset{\pi}{\longrightarrow} N\to 0$$ we say that the module $P$ is projective if for any map $\phi$ there exists a map $\psi$ that extends it:

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%26%20P%20%5C%5C%0A%09M%20%26%20N%20%26%200%0A%09%5Carrow%5B%22%5Cphi%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%5Cpi%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D2-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22%5Cpsi%22'%2C%20dashed%2C%20from%3D1-2%2C%20to%3D2-1%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	&amp; P \\
	M &amp; N &amp; 0
	\arrow&quot;\phi&quot;, from=1-2, to=2-2[](<>)
	\arrow&quot;\pi&quot;', from=2-1, to=2-2[](<>)
	\arrowfrom=2-2, to=2-3[](<>)
	\arrow&quot;\psi&quot;', dashed, from=1-2, to=2-1[](<>)
\end{tikzcd}" />

Dually, given any injective map $$0\to L\overset{i}{\longrightarrow}M$$
we say that the module $I$ is injective if for all there always exists an extension

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%090%20%26%20L%20%26%20M%20%5C%5C%0A%09%26%20I%0A%09%5Carrow%5Bfrom%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22i%22%2C%20from%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22j%22'%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7B%5Ctilde%7Bj%7D%7D%22'%2C%20dashed%2C%20from%3D2-2%2C%20to%3D1-3%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	0 &amp; L &amp; M \\
	&amp; I
	\arrowfrom=1-1, to=1-2[](<>)
	\arrow&quot;i&quot;, from=1-2, to=1-3[](<>)
	\arrow&quot;j&quot;', from=1-2, to=2-2[](<>)
	\arrow&quot;{\tilde{j}}&quot;', dashed, from=2-2, to=1-3[](<>)
\end{tikzcd}" />

# Properties
1. $P$ is a projective module iff $P$ is a direct summand of free module, i.e. there exists $n$ such that $$A^n=P\oplus Q.$$
2. Any finitely generated projective module over a local ring is free.

**Injective modules**
1. (Existence of injective modules) For all $M$ there exists an injective module $I$ such that $M\hookrightarrow I$.
2. (Criterion for injectivity) Assume that for any ideal $I$, we have that the inclusion $I\hookrightarrow A$ and any homomorphism $j:I\to Q$ extends to a map $\tilde{j}:A\to Q$. Then $Q$ is an injective module.
3. An abelian group $Q$ (which is a $\mathbb{Z}$-module) is injective iff $Q$ is divisible by elements of $\mathbb{Z}$, i.e. For all $q\in Q$ and all $N\in \mathbb{Z}$ there exists $\tilde{q}\in Q$ such that $\tilde{q}N=q$.
	1. Any $\mathbb{Z}$-module is embedded in an injective module, i.e. any abelian group is embedded in a divisible group.
4. Let $\phi:A\to B$ be a homomorphism of rings, and $Q$ an injective $A$-module. Then $\tilde{Q}=\text{Hom}_A(B,Q)$ is an injective $B$-module, where $$\text{Hom}_A(B,Q)=\{\psi:B\to Q\mid \psi(ab)=a\cdot\psi(b)\}$$
5. Any $A$ module can be put in some injective module.
	1. Let $M$ be an $A$-module and $\bar{M}$ be the abelian group obtained by forgetting the module structure on $M$. We claim that $\bar{M}$ is injective, which by example two it suffices to show that it is divisible. 
	2. Then $\text{Hom}_\mathbb{Z}(A,\bar{M})$ is an injective module by property 4

# Examples
1. (Proj) The free module $P=A^n$ is projective: it suffices to consider where to send the basis of $P$.
2. (inj) divisible group $\mathbb{Z}/(n)$
