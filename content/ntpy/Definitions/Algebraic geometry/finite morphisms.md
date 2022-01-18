# Algebraic sets
[[Algebraic subset]]

Let $X,Y$ be affine sets. Then a regular map $f:X\to Y$ is finite if $K[X]$ is finitely generated as a $f^\ast(K[Y])$-module.

## Properties
1. If $f:X\to Y$ is finite, then $|f^{-1}(y)|<\infty$ for all $y\in Y$.
2. Let $\phi:X\to Y$ be finite between affine sets.
	1. If $Z\subset X$ is closed, then $\phi(Z)$ is closed and the restriction $\phi|_Z:Z\to \phi(Z)$ is finite.
	2. If $X$ is irreducible and $Z\subsetneq X$ is closed, then $\phi(Z)\subsetneq Y$.
3. The composition of finite morphisms is finite.

**Proofs**
*1*
We provide an example to show that this condition is not sufficient. Consider the map $\mathbb{A}^1\setminus\{1\}\to\mathbb{A}^1$ defined by $z\mapsto z^2$. Then every point in the image has finite fiber: the points $0,1$ have fibers of cardinality 1 and every other point has a fiber of cardinality 2. 

We calculate the coordinate ring for $\mathbb{A}^1\setminus \{1\}$. This is isomorphic to $\{(x,y)\in\mathbb{A}^2\mid xy-y=1\}\subset\mathbb{A}^2$ by the maps $x\mapsto (x,\frac{1}{x-1})$ and $(x,y)\mapsto x$. Thus the coordinate ring can be seen to be isomorphic to $k[x,y]/(xy-y-1)$. 

The coordinate ring of $\mathbb{A}^1$ is $k[x]$, so the induced map on coordinate rings is $k[x]\hookrightarrow k[x,y]/(xy-y-1)$. But $k[x,y](xy-y-1)$ is not finitely generated as a $k[x]$-algebra, which can be seen by observing that the elements $y,y^2,y^3,\dots$ remain linearly independent. 

*3*
Let $f:X\to Y$ and $g:Y\to Z$ be finite morphisms. To show that $g\circ f$ (notation $gf$) is finite, we need to show that $K[X]$ is finitely generated as a $(gf)^\ast(K[Z])$-module. By assumption, $K[X]$ is finitely generated as an $f^\ast(K[Y])$-module and $K[Y]$ is finitely generated as a $g^\ast(K[Z])$-module.

Let $y\in K[Y]$. Then it can be written as a finite linear combination $y=g^\ast(z_1)y_1+\cdots+g^\ast(z_n)y_n$ with coefficients in $g^\ast(K[Z])\subset K[Y]$. Since every element in $K[X]$ can be expressed as a finite linear combination with coefficients in $f^\ast(K[Y])$, it suffices to show that $f^\ast(y)$ can be expressed as a finite linear combination with coefficients in $(gf)^\ast(K[Z])$. 

To that end, observe that $f^\ast$ is an algebra homomorphism, hence $f^\ast(y)=f^\ast(g^\ast(z_1)y_1+\cdots g^\ast(z_n)y_n)=(gf)^\ast(z_1)f^\ast(y_1)+\cdots+(gf)^\ast(z_n)f^\ast(y_n)$.This expresses $f^\ast(y)$ as a finite linear combination as desired. Now, it might be the case that some of the terms become equal upon applying $f^\ast$, but the combination still remains finite.



# Quasi-projective
[[Projective variety]]

Let $X,Y$ be quasi-projective sets.

A regular map $f:X\to Y$ is called finite if for all $y\in Y$ there exists an open affine set $U\ni y$ such that $V\coloneqq f^{-1}(U)\subset X$ is affine and $f|_V:V\to U$ is a finite map of affine sets.

So in some sense, this is the "global" definition.