---
title: "reduced norm, trace"
---

# Idea
Let $A$ be a [central simple algebra](<notes/ntpy/Definitions/central simple algebra.md>) over $k$, $K/k$ a finite Galois splitting field with [Galois group](<notes/ntpy/Galois group.md>) $G$. By properties 4 and 5 there, there is an isomorphism $$\phi:M_n(K)\overset{\sim}{\to}A\otimes_k K.$$ $G$ acts on $M_n(K)$ by acting on each of a matrices entries. Furthermore $G$ acts on $A\otimes_k K$ by acting on the tensor components from $K$, see [Galois descent](<notes/ntpy/Galois descent.md>).  

It is not generally true that $\phi$ is compatible with this action, i.e. $\phi$ is not $G$-equivariant, see property 5 at [central simple algebra](<notes/ntpy/Definitions/central simple algebra.md>). We wish to resolve this by "twisting" the $G$-action $\sigma_A$ on $A\otimes_k K$ to a $G$-action $a_\sigma$ on $M_n(K)$ so that $\phi$ is $G$-equivariant, i.e. construct $a_\sigma$ such that the following diagram commutes: 
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%7BM_n(K)%7D%20%26%20%7BA%5Cotimes_k%20K%7D%20%5C%5C%0A%09%7BM_n(K)%7D%20%26%20%7BA%5Cotimes_k%20K%7D%0A%09%5Carrow%5B%22%7Ba_%5Csigma%7D%22'%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22%5Cphi%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22%5Cphi%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7B%5Csigma_A%7D%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	{M_n(K)} &amp; {A\otimes_k K} \\
	{M_n(K)} &amp; {A\otimes_k K}
	\arrow&quot;{a_\sigma}&quot;', from=1-1, to=2-1]
	\arrow&quot;\phi&quot;, from=1-1, to=1-2]
	\arrow&quot;\phi&quot;', from=2-1, to=2-2]
	\arrow&quot;{\sigma_A}&quot;, from=1-2, to=2-2]
\end{tikzcd}" />
So we need $\phi a_\sigma = \sigma_A\phi$. Hence we define $a_\sigma=\phi^{-1}\sigma_A\phi$. We call this pattern of applying a map, doing something else, then applying the inverse, [twisting](<notes/ntpy/Key Ideas/twisting.md>). If we denote by $_aM_n(K)$ the algebra $M_n(K)$ equipped with the $a_\sigma$ $G$-action, then $$\phi:_aM_n(K)\overset{\sim}{\to}A\otimes_k K$$ is a $G$-equivariant isomorphism. While this is tautologically $G$-equivariant, we should verify that $a_\sigma$ is a $K$-automorphism of $M_n(K)$. But this is because $\phi$, $\sigma_A$, and $\phi^{-1}$ are all $K$-isomorphisms.

By [Galois descent](<notes/ntpy/Galois descent.md>), $$({}_aM_n(K))^G\cong A.$$ Being a matrix algebra, there is the determinant map $\text{det}$ on $M_n(K)$. **We wish to use the determinant to induce a map $A\to k$.**  We can do this by "descending" the domain of $\text{det}$ (i.e. $M_n(K)$) to $A$, but we can only do this if $\text{det}$ is $G$-equivariant. 

More specifically, we need to check $\text{det}$ is $G$-equivariant with respect to ${}_a M_n(K)$, as it is actually already $G$-equivariant wrt $M_n(K)$ (equipped with the usual entry-wise $G$-action): indeed, the determinant is given as the sum of products of elements in $K$, and actions of $G$ are in particular $K$-homomorphisms. So we need to check $\text{det}$ is $G$-equivariant with respect to ${}_aM_n(K)$. 

For all $\sigma\in G$, $a_\sigma$ is a $K$-automorphism of $M_n(K)$ hence is determined by an invertible matrix $C_\sigma\in GL_n(K)$. Then 

\begin{align}
\text{det}(a_\sigma(M))=& \text{det}(C_\sigma\sigma(M)C_\sigma^{-1})\\
=& \text{det}(C_\sigma)\text{det}(\sigma(M))\text{det}(C_\sigma^{-1}) \\
=& \text{det}(\sigma(M)) \\
=& M.
\end{align}

So indeed $$\text{det}:{}_aM_n(K)\to K$$ is $G$-equivariant. So we can use Galois descent (take $G$-invariants) to induce a map $({}_aM_n(K))^G\to K^G$, i.e. a map $$\text{Nrd}:A\to k,$$ called the *reduced norm*. 

Performing the above with the trace instead of determinant yields a map $$\text{Trd}:A\to k$$ called the *reduced trace*.

# Relation to norm, trace
The usual norm is defined as follows: given $a\in A$, the norm of $A$, denoted $N(a)$, the the determinant of the linear map determined by multiplication by $x$, e.g. there is a $k$-linear map $L_a:A\to A$ which is multiplication on the left, say. This is $k$-invariant because $k$ is the center of $A$, hence $L_a(kx)=akx=kax=kL_k(x)$. Then $N(a)=\text{det}(L_a)$. 

However this is a bit clunky, for reasons we will now discuss. Remember that we can embed $A\hookrightarrow M_n(K)$. Thus $a$ can be regarded as an $(n\times n)$-matrix. So the map $L_a$ is represented by an $(n^2\times n^2)$-matrix, in particular by the block diagonal matrix $\text{diag}(M_a,\dots,M_a)$ where $M_a$ is the matrix associated to $a$. The determinant of each of these blocks is $\text{Nrd}(a)$, the the determinant of $L_a$ is $(\text{Nrd}(a))^n$.

# Properties
1. $\text{Nrd}$ does not depend on choice of $\phi$ or $K$.

*Proofs*
**1**
Changing $\phi$ amounts to replacing $a_\sigma$ with a different automorphism, i.e. a different invertible matrix $C_\sigma$, which vanishes in the calculation regardless. 

Suppose $L/k$ is another finite Galois splitting field extension such that $A\otimes_k L\cong M_n(L)$. 

