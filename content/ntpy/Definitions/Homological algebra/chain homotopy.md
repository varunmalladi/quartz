---
title: "chain homotopy"
---

---
title: "chain homotopy"
---

# Definition
Let $f,g:C_\bullet\to D_\bullet$ be maps between [chain complex](notes/ntpy/Definitions/Homological algebra/chain complex.md)<notes/ntpy/Definitions/Homological algebra/chain complex.md>)es. 

$f$ and $g$ are homotopic, denoted $f\simeq g$, if there exist maps $h_\bullet$ such that

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%26%26%20%7BC_n%7D%20%26%26%20%7BC_%7Bn-1%7D%7D%20%5C%5C%0A%09%7BD_%7Bn%2B1%7D%7D%20%26%26%20%7BD_n%7D%0A%09%5Carrow%5B%22%7Bf_n-g_n%7D%22%7Bpos%3D0.3%7D%2C%20from%3D1-3%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22%7Bh_%7Bn-1%7D%7D%22%2C%20from%3D1-5%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22%7Bd_n%7D%22%2C%20from%3D1-3%2C%20to%3D1-5%5D%0A%09%5Carrow%5B%22%7Bd_%7Bn%2B1%7D%7D%22'%2C%20from%3D2-1%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22%7Bh_n%7D%22'%2C%20from%3D1-3%2C%20to%3D2-1%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	&amp;&amp; {C_n} &amp;&amp; {C_{n-1}} \\
	{D_{n+1}} &amp;&amp; {D_n}
	\arrow&quot;{f_n-g_n}&quot;{pos=0.3}, from=1-3, to=2-3[](<>)
	\arrow&quot;{h_{n-1}}&quot;, from=1-5, to=2-3[](<>)
	\arrow&quot;{d_n}&quot;, from=1-3, to=1-5[](<>)
	\arrow&quot;{d_{n+1}}&quot;', from=2-1, to=2-3[](<>)
	\arrow&quot;{h_n}&quot;', from=1-3, to=2-1[](<>)
\end{tikzcd}" />

The idea is that $f$ and $g$ induce the same map on homology. $f_n$ and $g_n$ differ only by a boundary: given a cycle $z\in C_n$, $(f_n-g_n)(z)\in\text{Im }d_{n+1}$.
