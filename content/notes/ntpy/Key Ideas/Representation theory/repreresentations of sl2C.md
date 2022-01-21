---
title: "repreresentations of sl2C"
---

# Idea
A general approach to determining the representations of a group, particularly a (semisimple) Lie algebra, is
1. Decompose the vector space into a direct sum of eigenspaces
2. Determine how the images of the group in $GL(V)$ act on these eigenspaces

The reason this method is effective is because eigenspaces are a clear way to see invariant subspaces.  Suppose we have a decomposition $$V=\bigoplus V_\alpha$$ where $\alpha$ is an eigenvalue for some $H\in GL(V)$. Now suppose for every element $g\in G$, the representation of $g$, which we will just call $g$, it was the case that for $v\in V_\alpha$, $gv\in V_\alpha$. In other words, suppose $v\in V_\alpha$ is an eigenvector of $g$ with eigenvalue $\alpha$. If this was true for all $g$, then every $V_\alpha$ would be an invariant subspace, so the representation would obviously be reducible.

Now suppose we had a decomposition $$V=V_{-2}\oplus V_0\oplus V_2.$$ Suppose it was the case that every $g\in G$ was such that for $g\in V_\alpha$, $gv\in V_{\alpha-2}$ and elements in $V_{-2}$ are annihilated. Then there are no nontrivial invariant subspaces, as any $g$ will either move us to a different eigenspace or be annihilated.

We'll also mention that it is not necessary to check what every single element does— it suffices to consider what the generators of the group do.

Hopefully it is clear that we can glean a lot of information from a decomposition of a vector space into eigenspaces. This is the approach we take here.

# General discussion
## A basis
The following is a basis for $\mathfrak{sl}_2(\mathbb{C})$: $$H=\begin{pmatrix}1 & 0 \\ 0 & -1\end{pmatrix},\quad X=\begin{pmatrix}0 & 1\\ 0 & 0\end{pmatrix},\quad Y=\begin{pmatrix}0& 0\\1 &0\end{pmatrix}$$
It satisfies the following properties: $$[H,X]=2X,\quad [H,Y]=-2Y,\quad [X,Y]=H.$$

As mentioned before, the choice of $H$ as a basis is sensible enough in our aim to decompose the vector space into eigenspaces. We will address why $X$ and $Y$ are sensible choices in retrospect.

## A decomposition
Let $V$ be an irreducible finite-dimensional [representation](notes/ntpy/Key Ideas/Representation theory/repreresentations of sl2C.md). We will use the following fact: $\mathfrak{sl}_2(\mathbb{C})$ is a semisimple [lie algebra](notes/ntpy/Definitions/Representation Theory/lie algebra.md). In [jordan decomposition](notes/ntpy/jordan decomposition.md), we discuss that the Jordan decomposition is preserved under a representation in this case, in our case implying that
- The action of $H$ on $V$ is diagonalizable

(This is because $H$ is diagonalizable, and we have just referenced the fact that this is a property preserved under a representation)

This allows us to decompose $V$ into the direct sum of eigenspaces: $$V=\bigoplus V_\alpha.$$ Specifically, for $v\in V_\alpha$, $$H(v)=\alpha\cdot v.$$ In other words, $v\in V_\alpha$ means $v$ is an eigenvector with eigenvalue $\alpha$. (Diagonalizable implies that the sum of the dimensions of the eigenspaces is the dimension of the whole space, so that we may regard $V$ as a direct sum of eigenspaces of $H$).

This is similar to how we decomposed the abelian [representations of s3](notes/ntpy/Key Ideas/Representation theory/representations of s3.md). In that case, the nonabelian part of $S_3$ simply permutated the summands above in which vectors were in. To do something analagous here, we need to ask how $X$ and $Y$ act on the summands. It turns out that they also just carry each summand to another, i.e. permutes the summands.

## Actions of other basis elements on decomposition
Let us consider how $X$ acts on $V_\alpha$. To do this, let us consider how $X$ acts on some $v\in V_\alpha$. This means we want to analyze $X(v)$ with respect to the decomposition above: $$\begin{gather} HX(v)-XH(v)=[H,X](v), \\ HX(v)=X(\alpha\cdot v)+2X(v) = (\alpha+2)\cdot X(v).\end{gather}$$
Thus:
- If $v$ is an eigenvector for $H$ with eigenvalue $\alpha$, then $X(v)$ is an eigenvector for $H$ with eigenvalue $\alpha+2$.

This tells us that not only does $X$ simply permute the summands, it does so specifically: $$X:V_\alpha\to V_{\alpha+2}.$$

Likewise, $$Y:V_\alpha\to V_{\alpha-2}.$$

## 1st characterization of eigenvectors
The following is a corollary:
- All (complex) eigenvalues $\alpha$ are congruent mod 2.

For we have assumed that $V$ is irreducible, and by our discussion above, the subspace $V_{\alpha+2k}$ is invariant under $H,X,Y$ hence under all of $\mathfrak{sl}_2(\mathbb{C})$. Thus it must be $V$ itself.
- For every eigenvalue $\beta$, there is an unbroken string of eigenvalues $\beta, \beta+2,\dots,\beta+2j$.

We will denote the last element in the above string by $n$. That the string terminantes is because we are dealing with finite dimensional representations, hence the decomposition into eigenspaces is finite. We have the following picture now:

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%5Ccdots%20%5Carrow%5Br%2C%20%22X%22%2C%20bend%20left%3D49%5D%20%5Carrow%5B%22H%22'%2C%20loop%2C%20distance%3D2em%2C%20in%3D305%2C%20out%3D235%5D%20%26%20V_%7Bn-4%7D%20%5Carrow%5B%22H%22'%2C%20loop%2C%20distance%3D2em%2C%20in%3D305%2C%20out%3D235%5D%20%5Carrow%5Bl%2C%20%22Y%22%5D%20%5Carrow%5Br%2C%20%22X%22%2C%20bend%20left%3D49%5D%20%26%20V_%7Bn-2%7D%20%5Carrow%5B%22H%22'%2C%20loop%2C%20distance%3D2em%2C%20in%3D305%2C%20out%3D235%5D%20%5Carrow%5Bl%2C%20%22Y%22%5D%20%5Carrow%5Br%2C%20%22X%22%2C%20bend%20left%3D49%5D%20%26%20V_n%20%5Carrow%5B%22H%22'%2C%20loop%2C%20distance%3D2em%2C%20in%3D305%2C%20out%3D235%5D%20%5Carrow%5Bl%2C%20%22Y%22%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
\cdots \arrowr, &quot;X&quot;, bend left=49[]() \arrow&quot;H&quot;', loop, distance=2em, in=305, out=235[]() &amp; V_{n-4} \arrow&quot;H&quot;', loop, distance=2em, in=305, out=235[]() \arrowl, &quot;Y&quot;[]() \arrowr, &quot;X&quot;, bend left=49[]() &amp; V_{n-2} \arrow&quot;H&quot;', loop, distance=2em, in=305, out=235[]() \arrowl, &quot;Y&quot;[]() \arrowr, &quot;X&quot;, bend left=49[]() &amp; V_n \arrow&quot;H&quot;', loop, distance=2em, in=305, out=235[]() \arrowl, &quot;Y&quot;[]()
\end{tikzcd}" />
$$ $$ $$ $$ $$ $$
## 2nd characterization: a basis for $V$
We will show the following:
- For $v\in V_n$, the set $\{v, Y(v), Y^2(v),\dots\}$ spans $V$

This is believable, but the difficulty is in the fact that we do not know right now that each $V_\alpha$ is generated by a single vector, i.e. is one-dimensional. By exhibiting the set above as a basis(?) for $V$, we will have as a corollary that each $V_\alpha$ is one-dimensional.

**Proof**
Let $W=\text{span}\{v, Y(v), Y^2(V),\dots\}$. ISTS $W$ is invariant, for by assumption $V$ is irreducible hence $W=V$. ISTS that $W$ is invariant under each basis element $H$, $X$, $Y$. It is invariant under $Y$ by definition. Each $Y^m(v)$ lives in the eigenspace $V_{n-2m}$, and these are invariant under $H$ by construction. So it remains to show that $W$ is invariant under $X$.

We will check each vector in turn, inductively. For $v$, we have $X(v)=0\in V$. For $Y(v)$, observe that
$$
\begin{align}
X(Y(v))=&X,Y[]()(v)+Y(X(v)) \\
=& H(v)+Y(0)\\
=& nv.
\end{align}
$$
 Now we will check $Y^2(V)$:
 $$
 \begin{align}
X(Y^2(v))=& X,Y[]()(Y(v))+Y(X(Y(v)))\\
=& H(Y(v))+Y(nv) \\
=& (n-2)\cdot Y(V)+n\cdot Y(v).
 \end{align}
 $$
 As can be verified by induction, the general case is
 $$
\begin{align}
X(Y^m(v))=& (n+(n-2)+\cdots+(n-2(m-1)))\cdot Y^{m-1}(v) \\
=& m(n-m+1)\cdot Y^{m-1}(v).
\end{align}
$$
So indeed $X(Y^m(v))\in W$.

