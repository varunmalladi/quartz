---
title: "inverse limit"
---

# Idea
Inverse limits are dual to [direct limit](notes/ntpy/Definitions/Category theory/direct limit.md)s and are special kinds of categorical limits.

# Definition
Let $(I,\leq)$ be a directed set (one can actually weaken this upper bound condition).
- An *inverse system* of (groups) $(G_i,\phi_{ij})_{i,j\in I}$ is 
	- a group $G_i$ for each $i\in I$.
	- a hom $\phi_{ij}:G_j\to G_i$ whenver $i\leq j$.
	- $\phi_{ii}=\text{id}_{G_i}$
	- $\phi_{ik}=\phi_{ij}\circ\phi_{jk}$ 
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%7BG_k%7D%20%26%20%7BG_j%7D%20%26%20%7BG_i%7D%0A%09%5Carrow%5B%22%7B%5Cphi_%7Bjk%7D%7D%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7B%5Cphi_%7Bji%7D%7D%22%2C%20from%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22%7B%5Cphi_%7Bik%7D%7D%22'%2C%20curve%3D%7Bheight%3D18pt%7D%2C%20from%3D1-1%2C%20to%3D1-3%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	{G_k} &amp; {G_j} &amp; {G_i}
	\arrow&quot;{\phi_{jk}}&quot;, from=1-1, to=1-2[]()
	\arrow&quot;{\phi_{ji}}&quot;, from=1-2, to=1-3[]()
	\arrow&quot;{\phi_{ik}}&quot;', curve={height=18pt}, from=1-1, to=1-3[]()
\end{tikzcd}" />
- An *inverse limit* of an inverse system $(G_i,\phi_{ij})_{i,j\in I}$ is the group $G=\underset{\leftarrow}{\lim}G_i$ that is universal with respect to thhe diagrams <img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%26%20G%20%5C%5C%0A%09%7BG_j%7D%20%26%26%20%7BG_i%7D%0A%09%5Carrow%5B%22%7B%5Cphi_%7Bij%7D%7D%22%2C%20from%3D2-1%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22%7B%5Cpi_j%7D%22'%2C%20from%3D1-2%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22%7B%5Cpi_i%7D%22%2C%20from%3D1-2%2C%20to%3D2-3%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	&amp; G \\
	{G_j} &amp;&amp; {G_i}
	\arrow&quot;{\phi_{ij}}&quot;, from=2-1, to=2-3[]()
	\arrow&quot;{\pi_j}&quot;', from=1-2, to=2-1[]()
	\arrow&quot;{\pi_i}&quot;, from=1-2, to=2-3[]()
\end{tikzcd}" />

We can explicitly construct it in $\text{Grp}$:
$$
\lim_\leftarrow G_i=\{(g_i)\in\prod_{i\in I}G_i\mid g_i=\phi_{ij}(g_j)\ \forall i\leq j\}
$$
**Remark.** The equivalence relation here is saying "identify elements that map (backwards) to the same element. Just like the equivalence relation in the explicit construction of direct limits, it is identifying things that are "eventually equal", but the directions are reversed.

# Examples
**1** ([profinite completion](notes/ntpy/profinite completion.md))
 **2** (power series)
 Let $F$ be a field. We may regard
 $$ F[X]/(X^n)=\{a_0+a_1X+\cdots+a_{n-1}X^{n-1}\mid a_i\in F\} $$ 
 as a "truncated power series". For $n\leq m$, there is a natural quotient $$\pi_{nm}:F[X]/(X^m)\to F[X]/(X^n).$$ Then $(F[X]/(X^n),\pi_{nm})_{n,m\in\mathbb{N}}$ determines an inverse system, and
 $$ \lim_\leftarrow F[X]/(X^n)\cong F[[X]], $$ the power series ring. Explicitly, elements of the inverse limit look like $$ (a_0, a_0+a_1X,a_0+a_1X+a_2X^2,\cdots).$$

**3** ([p-adic integers](notes/ntpy/Definitions/Algebraic Number Theory/P-adic numbers.md))
 This draws an analogy between p-adic integers and power series.
 
 **4**
 For $n\mid m$, there is a quotient map $$\pi_{nm}:\mathbb{Z}/m\mathbb{Z}\to\mathbb{Z}/n\mathbb{Z}.$$ Thhen $(\mathbb{Z}/n\mathbb{Z},\pi_{nm})$ is an inverse system indexed by the divisibility poset $(\mathbb{Z}_{\geq 0},\cdot\mid\cdot)$, which is isomorphic to the finite index subgroups poset $\{n\mathbb{Z}\subset\mathbb{Z}\mid n\geq 1\}$ under reverse inclusion. Hence 
 $$\lim_\leftarrow \mathbb{Z}/n\mathbb{Z}=\widehat{\mathbb{Z}}\cong\prod_{p}\mathbb{Z}_p,$$
 where the middle object is the profinite compleetion and the isomorphism is due to the [Chinese Remainder Theorem](notes/ntpy/Theorems/Ring Theory/Chinese Remainder Theorem.md).
 
 # Properties
 1. A sequence $(K_i)\to (L_i)\to (M_i)$ is exact iff each $K_i\to L_i\to N_i$ is exact.
	 1. (?) We require the maps to be compatible, in the sense that the diagram appearing in beginning of the proof commutes.

*Proofs*
**1**
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%5Ccdots%20%26%20%7BM_3%7D%20%26%20%7BM_2%7D%20%26%20%7BM_1%7D%20%5C%5C%0A%09%5Ccdots%20%26%20%7BL_3%7D%20%26%20%7BL_2%7D%20%26%20%7BL_1%7D%20%5C%5C%0A%09%5Ccdots%20%26%20%7BK_3%7D%20%26%20%7BK_2%7D%20%26%20%7BK_1%7D%0A%09%5Carrow%5B%22%7Bk_%7B34%7D%7D%22'%2C%20from%3D3-1%2C%20to%3D3-2%5D%0A%09%5Carrow%5Bfrom%3D3-2%2C%20to%3D3-3%5D%0A%09%5Carrow%5Bfrom%3D3-3%2C%20to%3D3-4%5D%0A%09%5Carrow%5B%22%7Bl_%7B34%7D%7D%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D2-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5Bfrom%3D2-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22%7Bm_%7B34%7D%7D%22'%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5Bfrom%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5Bfrom%3D1-3%2C%20to%3D1-4%5D%0A%09%5Carrow%5B%22%7B%5Ctext%7Blm%7D_3%7D%22'%2C%20from%3D2-2%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%7B%5Ctext%7Bkl%7D_3%7D%22'%2C%20from%3D3-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D3-3%2C%20to%3D2-3%5D%0A%09%5Carrow%5Bfrom%3D2-3%2C%20to%3D1-3%5D%0A%09%5Carrow%5Bfrom%3D2-4%2C%20to%3D1-4%5D%0A%09%5Carrow%5Bfrom%3D3-4%2C%20to%3D2-4%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	\cdots &amp; {M_3} &amp; {M_2} &amp; {M_1} \\
	\cdots &amp; {L_3} &amp; {L_2} &amp; {L_1} \\
	\cdots &amp; {K_3} &amp; {K_2} &amp; {K_1}
	\arrow&quot;{k_{34}}&quot;', from=3-1, to=3-2[]()
	\arrowfrom=3-2, to=3-3[]()
	\arrowfrom=3-3, to=3-4[]()
	\arrow&quot;{l_{34}}&quot;', from=2-1, to=2-2[]()
	\arrowfrom=2-2, to=2-3[]()
	\arrowfrom=2-3, to=2-4[]()
	\arrow&quot;{m_{34}}&quot;', from=1-1, to=1-2[]()
	\arrowfrom=1-2, to=1-3[]()
	\arrowfrom=1-3, to=1-4[]()
	\arrow&quot;{\text{lm}_3}&quot;', from=2-2, to=1-2[]()
	\arrow&quot;{\text{kl}_3}&quot;', from=3-2, to=2-2[]()
	\arrowfrom=3-3, to=2-3[]()
	\arrowfrom=2-3, to=1-3[]()
	\arrowfrom=2-4, to=1-4[]()
	\arrowfrom=3-4, to=2-4[]()
\end{tikzcd}" />

Since each element of the inverse limits can be expressed as an element of the direct product per the explicit definition above, the maps $K\to L\to M$ are defined componentwise by the ones given in the diagram above.

Suppose $\alpha\in\text{ker}(L\to M)$. Writing $\alpha=(\dots,l_3,l_2,l_1)$, it must be the case that $\text{lm}_i(l_i)=0$ for all $i$. Hence each $l_i\in\text{ker}(\text{lm}_i)$, so that by assumption there exists $k_i\in K_i$ such that $\text{kl}_i(k_i)=l_i$. These determine an element $(\dots,k_3,k_2,k_1)\in\prod K_i$. Now we will construct an element such that for all $j$, it is the case that $k_{ij}(k_j)=k_i$ for all $i\leq j$. For any $j$, $$\text{kl}_i(k_{ij}(k_j))=l_{ij}(\text{kl}_j(k_j))=l_i,$$ so that we may set $k_i=k_{ij}(k_j)$ while still having image $\alpha$. Since we can do this for any $j$, we can construct an element in $K$ with image $\alpha$. Hence $\text{ker}(L\to M)\subset\text{im}(K\to L)$.

Conversely, suppose $\beta\in\text{im}(K\to L)$. Then each component $l_i$ of $\beta$ is the image of some $k_i$. Then by assumption each $l_i\in\text{ker}(\text{lm}_i)$. But then the image of $\beta$ in $M$ is given on components by $(\text{lm}_i(l_i)=0)$, hence $\beta\in\text{ker}(L\to M)$ and $\text{im}(K\to L)\subset\text{ker}(L\to M)$.



