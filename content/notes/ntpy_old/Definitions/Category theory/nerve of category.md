---
title: "nerve of category"
---

# Idea

# Relation to homotopy
Let $\partial\Delta[n]$ be the boundary or sphere of a simplex. In the nerve, in the case of $\partial\Delta[2]\to C$, this means a triangle
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%26%20b%20%5C%5C%0A%09a%20%26%26%20c%0A%09%5Carrow%5B%22f%22%2C%20from%3D2-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22g%22%2C%20from%3D1-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22h%22'%2C%20from%3D2-1%2C%20to%3D2-3%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	&amp; b \\
	a &amp;&amp; c
	\arrow&quot;f&quot;, from=2-1, to=1-2[]()
	\arrow&quot;g&quot;, from=1-2, to=2-3[]()
	\arrow&quot;h&quot;', from=2-1, to=2-3[]()
\end{tikzcd}" />
It is apparent that there is a 2-cell $fg\Rightarrow h$ iff $h=fg$. Of course, this need not be the case, which is to say that every 2-sphere need not be fillable or extendable to a 2-simplex.

Now consider a 3-sphere. This is a 3-simplex with the 3-cell removed. It turns out that this does extend to a simplex, due to the existence of the 2-cells on its faces. Explicitly, given a 3-sphere, we wish to show that the composite $a\to b\to c\to d$ equals $a\to d$. But using the 2-cells, we see that $a\to b\to c\to d = a\to b\to d=a\to d$. Intuitively, it makes sense that the 2-cells, which witness composition, are enough to fill in higher spheres in the nerve, because higher simplices in the nerve correspond to chains of compositions.

Informally, the above describes the nerve of a category as 2-coskeletal. In [simplicial skeleton](ntpy/Definitions/Category theory/simplicial skeleton.md), we discuss homotopical properties of this. But we will here discuss intuitively why the homotopy category functor is left adjoint to the nerve construction $\text{Cat}\to\text{sSet}$. Essentially, to move back to $\text{Cat}$ from the nerve we need to preserve the property that a 2-sphere is filled iff its exhibits the composite (described above). This means that given a diagram of the form 
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%26%20b%20%5C%5C%0A%09a%20%26%26%20c%0A%09%5Carrow%5B%22f%22%2C%20from%3D2-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22g%22%2C%20from%3D1-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22%22%7Bname%3D0%2C%20anchor%3Dcenter%2C%20inner%20sep%3D0%7D%2C%20%22h%22'%2C%20from%3D2-1%2C%20to%3D2-3%5D%0A%09%5Carrow%5Bshorten%20%3E%3D3pt%2C%20Rightarrow%2C%20from%3D1-2%2C%20to%3D0%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	&amp; b \\
	a &amp;&amp; c
	\arrow&quot;f&quot;, from=2-1, to=1-2[]()
	\arrow&quot;g&quot;, from=1-2, to=2-3[]()
	\arrow&quot;&quot;{name=0, anchor=center, inner sep=0}, &quot;h&quot;', from=2-1, to=2-3[]()
	\arrowshorten &gt;=3pt, Rightarrow, from=1-2, to=0[]()
\end{tikzcd}" />
we require that $h=fg$. In particular this implies that given a homotopy
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%26%20b%20%5C%5C%0A%09a%20%26%26%20b%0A%09%5Carrow%5B%22f%22%2C%20from%3D2-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5Bno%20head%2C%20from%3D1-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22%22%7Bname%3D0%2C%20anchor%3Dcenter%2C%20inner%20sep%3D0%7D%2C%20%22h%22'%2C%20from%3D2-1%2C%20to%3D2-3%5D%0A%09%5Carrow%5Bshift%20left%3D1%2C%20no%20head%2C%20from%3D1-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5Bshorten%20%3C%3D3pt%2C%20shorten%20%3E%3D6pt%2C%20Rightarrow%2C%20from%3D1-2%2C%20to%3D0%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	&amp; b \\
	a &amp;&amp; b
	\arrow&quot;f&quot;, from=2-1, to=1-2[]()
	\arrowno head, from=1-2, to=2-3[]()
	\arrow&quot;&quot;{name=0, anchor=center, inner sep=0}, &quot;h&quot;', from=2-1, to=2-3[]()
	\arrowshift left=1, no head, from=1-2, to=2-3[]()
	\arrowshorten &lt;=3pt, shorten &gt;=6pt, Rightarrow, from=1-2, to=0[]()
\end{tikzcd}" />
then $f\cong h$, i.e. homotopy equivalences become isomorphisms.

