---
title: "lie algebra"
---

# Idea
There are two principles that make the study of Lie algebras related to the structure of Lie groups:
1. Let $G$ and $H$ be Lie groups, and $G$ is additionally connected. Then a map $\rho:G\to H$ is uniquely determined by its differential at the identity: $d\rho_e:T_eG\to T_eH$.
2. Let $G$ and $H$ be Lie groups, with $G$ connected and simply connected. Then a linear map $T_eG\to T_eH$ is the differential of a homomorphism $\rho:G\to H$ if and only if it preserves the bracket operation.

The first statement already looks strong, but a priori we do not know whether an arbitrary map between Lie algebras is the differential of a map between Lie groups. The second principle answers this question.

## Bracket
Given our two principles above, we might formulate the following question:

- How is the structure of a homomorphism of Lie groups reflected in its differential, which is a map of Lie algebras?

Given a map of Lie groups there is a canonical induced map of Lie algebras— constructing this is not the problem. The problem is seeing what structure within the Lie algebra is preserved under this induced map.

To do this, we can regard "structure" as an endomorphism. Then, we can somehow associate to the structure maps on $G$ some structure maps on $T_eG$ and see what $d\rho$ does to them.

For example, for any element $g\in G$ there is an endomorphism $m_g:G\to G$ which is just multiplication by $g$. Then, to say that a homomorphism $\rho:G\to H$ preserves a certain structure is to say that it commutes with the structure endomorphism. For instance, a homomorphism $\rho:G\to H$ is a smooth map that respects the group structure in the sense that $\rho(gh)=\rho(g)\rho(h)$, and we may equivalently formulate this property in terms of the structure map $m_g$ above:

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09G%20%26%20H%20%5C%5C%0A%09G%20%26%20H%0A%09%5Carrow%5B%22%7Bm_g%7D%22'%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22%5Crho%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%5Crho%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7Bm_%7B%5Crho(g)%7D%7D%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	G &amp; H \\
	G &amp; H
	\arrow&quot;{m_g}&quot;', from=1-1, to=2-1[](<>)
	\arrow&quot;\rho&quot;', from=2-1, to=2-2[](<>)
	\arrow&quot;\rho&quot;, from=1-1, to=1-2[](<>)
	\arrow&quot;{m_{\rho(g)}}&quot;, from=1-2, to=2-2[](<>)
\end{tikzcd}" />

(start with $h$ in the top left, and commutativity relations give the formula above). If this diagram commutes for all $g$ then we have a homomorphism, so we can think of $\rho$ as being a homomorphism iff it preserves the structure maps $\{m_g\}_{g\in G}$.

We could try to "lift" these structure maps to $T_e G$ and see if $d\rho$ preserves them, but this doesn't work well because $m_g$ does not fix $e$, so we can't expect to be able to associate a map corresponding to $m_g$ on the tangent space at $e$.

So our next goal is to build another endomorphism, $\Psi_g$, that does fix $e$ but also expresses the group structure like $\{m_g\}$ did, i.e. such that $\rho$ is a homomorphism iff it preserves the structure maps $\{\Psi_g\}_{g\in G}$. We suggest the map of conjugation: $$\Psi_g(h)=ghg^{-1}.$$
A map is a group homomorphism implies that it preserves conjugation for all elements, so $\rho$ is a homomorphism implies $\{\Psi_g\}_{g\in G}$ is preserved. It also has the added benefit that $\Psi_g(e)=e$ for all $g$, so at least $e$ is fixed so we can try to associate to $\Psi_g$ a map $T_eG\to T_eG$.  So if $\rho$ is a homomorphism, then the following diagram commutes: 

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09G%20%26%20H%20%5C%5C%0A%09G%20%26%20H%0A%09%5Carrow%5B%22%7B%5CPsi_g%7D%22'%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22%5Crho%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%5Crho%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7B%5CPsi_%7B%5Crho(g)%7D%7D%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	G &amp; H \\
	G &amp; H
	\arrow&quot;{\Psi_g}&quot;', from=1-1, to=2-1[](<>)
	\arrow&quot;\rho&quot;', from=2-1, to=2-2[](<>)
	\arrow&quot;\rho&quot;, from=1-1, to=1-2[](<>)
	\arrow&quot;{\Psi_{\rho(g)}}&quot;, from=1-2, to=2-2[](<>)
\end{tikzcd}" />

What's more, conjugation is an automorphism, so there is an associated map $$\Psi:G\to \text{Aut}(G).$$ At this point, we recall the following fact: $T_e\text{Aut}(T_eG)\cong\text{End}(T_eG)$. So we want to lift $\Psi$ to $T_eG$, but we cant just take the differential, as then we would have a map $T_eG\to T_e\text{Aut}(G)$. Our fact above suggests that we first want to lift $\text{Aut}(G)$ to $\text{Aut}(T_eG)$. We can do this just be taking the differential of the maps in $\text{Aut}(G)$, which amounts to associating a map $$\begin{gather} \text{Ad}:G\to \text{Aut}(T_eG) \\ g\mapsto (d\Psi_g)_e\end{gather}$$ which is actually a representation since $T_eG$ can be regarded as a vector space. This is called the adjoint representation of $G$.

It follows from the fact that $T_e(-)$ is a functor that the following diagram commutes (we're saying that taking differentials of all the maps in a commuting diagram yields another commuting diagram):

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%7BT_eG%7D%20%26%20%7BT_eH%7D%20%5C%5C%0A%09%7BT_eG%7D%20%26%20%7BT_eH%7D%0A%09%5Carrow%5B%22%7B%5Ctext%7BAd%7D(g)%7D%22'%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22%7B(d%5Crho)_e%7D%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7B(d%5Crho)_e%7D%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7B%5Ctext%7BAd%7D(%5Crho(g))%7D%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	{T_eG} &amp; {T_eH} \\
	{T_eG} &amp; {T_eH}
	\arrow&quot;{\text{Ad}(g)}&quot;', from=1-1, to=2-1[](<>)
	\arrow&quot;{(d\rho)_e}&quot;', from=2-1, to=2-2[](<>)
	\arrow&quot;{(d\rho)_e}&quot;, from=1-1, to=1-2[](<>)
	\arrow&quot;{\text{Ad}(\rho(g))}&quot;, from=1-2, to=2-2[](<>)
\end{tikzcd}" />

By our fact above, we can now easily cast $\text{Ad}:G\to \text{Aut}(T_eG)$ as a structure map purely in terms of the $T_eG$ by taking the differential: $$\text{ad}:T_eG\to \text{End}(T_eG).$$ By the tensor hom adjunction, $\text{ad}$ is equivalent to a linear map $T_eG\otimes T_eG\to T_eG$, which is nothing but a bilinear map $$T_eG\times T_eG\to T_eG.$$ Again, because $\rho$ preserved $\text{Ad}$ it must also preserve its differential $\text{ad}$, hence it preserves the bilinear map above. For $X,Y\in T_eG$, we write $$[X,Y]\coloneqq\text{ad}(X)(Y)$$ and this is the Lie bracket. Thus the following square commutes:

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%7BT_eG%7D%20%26%20%7BT_eH%7D%20%5C%5C%0A%09%7BT_eG%7D%20%26%20%7BT_eH%7D%0A%09%5Carrow%5B%22%7B%5Ctext%7Bad%7D(v)%7D%22'%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22%7B(d%5Crho)_e%7D%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7B(d%5Crho)_e%7D%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7B%5Ctext%7Bad%7D(d%5Crho(v))%7D%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	{T_eG} &amp; {T_eH} \\
	{T_eG} &amp; {T_eH}
	\arrow&quot;{\text{ad}(v)}&quot;', from=1-1, to=2-1[](<>)
	\arrow&quot;{(d\rho)_e}&quot;', from=2-1, to=2-2[](<>)
	\arrow&quot;{(d\rho)_e}&quot;, from=1-1, to=1-2[](<>)
	\arrow&quot;{\text{ad}(d\rho(v))}&quot;, from=1-2, to=2-2[](<>)
\end{tikzcd}" />

The point:
- the differential of a homomorphism of Lie groups (at $e$) preserves the Lie bracket.

There is also a nice formula in the flavor of the group homomorphism one: $$d\rho_e[X,Y]=[d\rho_e(X),d\rho_e(X)].$$

This is a necessary condition, but, remarkably, under mild additional assumptions this turns out to be a sufficient condition, meaning if a map $T_eG\to T_eG$ preserves the lie bracket, it is the differential of some map of Lie groups, i.e. is equal to $d\rho_e$ for some homomorphism $\rho$.

Ultimately, our journey of lifting structure maps has been the following:


<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%7B%5Ctext%7BEnd%7D(T_eG)%7D%20%5C%5C%0A%09%7B%5Ctext%7BAut%7D(T_eG)%7D%20%26%20%7BT_eG%7D%20%5C%5C%0A%09%7B%5Ctext%7BAut%7D(G)%7D%20%26%20G%0A%09%5Carrow%5B%22%5CPsi%22%2C%20from%3D3-2%2C%20to%3D3-1%5D%0A%09%5Carrow%5Bfrom%3D3-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22%7B%5Ctext%7BAd%7D%7D%22'%2C%20dashed%2C%20from%3D3-2%2C%20to%3D2-1%5D%0A%09%5Carrow%5Bfrom%3D3-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D2-1%2C%20to%3D1-1%5D%0A%09%5Carrow%5B%22%7B%5Ctext%7Bad%7D%7D%22'%2C%20dotted%2C%20from%3D2-2%2C%20to%3D1-1%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	{\text{End}(T_eG)} \\
	{\text{Aut}(T_eG)} &amp; {T_eG} \\
	{\text{Aut}(G)} &amp; G
	\arrow&quot;\Psi&quot;, from=3-2, to=3-1[](<>)
	\arrowfrom=3-1, to=2-1[](<>)
	\arrow&quot;{\text{Ad}}&quot;', dashed, from=3-2, to=2-1[](<>)
	\arrowfrom=3-2, to=2-2[](<>)
	\arrowfrom=2-1, to=1-1[](<>)
	\arrow&quot;{\text{ad}}&quot;', dotted, from=2-2, to=1-1[](<>)
\end{tikzcd}" />

# Definition

# Representations
A representation of a Lie algebra is a morphism $$\mathfrak{g}\to\mathfrak{gl}(V)$$ that preserves the structure, i.e. a linear map that preserves the bracket: for $X,Y\in\mathfrak{g}$ and $v\in V$, $$[X,Y](v)=X(Y(v))-Y(X(v)).$$

There are the following properties:
1. (tensor product) $X(v\otimes w)=X(v)\otimes w+v\otimes X(w)$
2. (dual) $(\rho(X))^\ast=-{}^t\rho(X)$
