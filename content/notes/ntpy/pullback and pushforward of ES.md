---
title: "pullback and pushforward of ES"
---

# Pullback

Given a short exact sequence $$0\to A\to B\to C\to 0$$ and a map $g:C_1\to C$, we may construct the pullback along this map such that the following diagram commutes:
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%090%20%26%20A%20%26%20%7BB_1%7D%20%26%20%7BC_1%7D%20%26%200%20%5C%5C%0A%090%20%26%20A%20%26%20B%20%26%20C%20%26%200%0A%09%5Carrow%5Bfrom%3D1-3%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22g%22%2C%20from%3D1-4%2C%20to%3D2-4%5D%0A%09%5Carrow%5BRightarrow%2C%20no%20head%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5Bfrom%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5Bfrom%3D1-3%2C%20to%3D1-4%5D%0A%09%5Carrow%5Bfrom%3D1-4%2C%20to%3D1-5%5D%0A%09%5Carrow%5Bfrom%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D2-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5Bfrom%3D2-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5Bfrom%3D2-4%2C%20to%3D2-5%5D%0A%09%5Carrow%5B%22%5Clrcorner%22%7Banchor%3Dcenter%2C%20pos%3D0.125%7D%2C%20draw%3Dnone%2C%20from%3D1-3%2C%20to%3D2-4%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	0 &amp; A &amp; {B_1} &amp; {C_1} &amp; 0 \\
	0 &amp; A &amp; B &amp; C &amp; 0
	\arrowfrom=1-3, to=2-3[]()
	\arrow&quot;g&quot;, from=1-4, to=2-4[]()
	\arrowRightarrow, no head, from=1-2, to=2-2[]()
	\arrowfrom=1-1, to=1-2[]()
	\arrowfrom=1-2, to=1-3[]()
	\arrowfrom=1-3, to=1-4[]()
	\arrowfrom=1-4, to=1-5[]()
	\arrowfrom=2-1, to=2-2[]()
	\arrowfrom=2-2, to=2-3[]()
	\arrowfrom=2-3, to=2-4[]()
	\arrowfrom=2-4, to=2-5[]()
	\arrow&quot;\lrcorner&quot;{anchor=center, pos=0.125}, draw=none, from=1-3, to=2-4[]()
\end{tikzcd}" />
Regarding the SES as an extension $E$, we write $E\circ g$ for the pullback.

# Pushout
Given a SES $$0\to A\to B\to C\to 0$$ and a map $f:A\to A_1$, we may construct the pushout along this map such that the following diagram commutes:
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%090%20%26%20A%20%26%20B%20%26%20C%20%26%200%20%5C%5C%0A%090%20%26%20%7BA_1%7D%20%26%20%7BB_1%7D%20%26%20C%20%26%200%0A%09%5Carrow%5Bfrom%3D1-3%2C%20to%3D2-3%5D%0A%09%5Carrow%5BRightarrow%2C%20no%20head%2C%20from%3D1-4%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22f%22'%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5Bfrom%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5Bfrom%3D1-3%2C%20to%3D1-4%5D%0A%09%5Carrow%5Bfrom%3D1-4%2C%20to%3D1-5%5D%0A%09%5Carrow%5Bfrom%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D2-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5Bfrom%3D2-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5Bfrom%3D2-4%2C%20to%3D2-5%5D%0A%09%5Carrow%5B%22%5Clrcorner%22%7Banchor%3Dcenter%2C%20pos%3D0.125%2C%20rotate%3D180%7D%2C%20draw%3Dnone%2C%20from%3D2-3%2C%20to%3D1-2%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	0 &amp; A &amp; B &amp; C &amp; 0 \\
	0 &amp; {A_1} &amp; {B_1} &amp; C &amp; 0
	\arrowfrom=1-3, to=2-3[]()
	\arrowRightarrow, no head, from=1-4, to=2-4[]()
	\arrow&quot;f&quot;', from=1-2, to=2-2[]()
	\arrowfrom=1-1, to=1-2[]()
	\arrowfrom=1-2, to=1-3[]()
	\arrowfrom=1-3, to=1-4[]()
	\arrowfrom=1-4, to=1-5[]()
	\arrowfrom=2-1, to=2-2[]()
	\arrowfrom=2-2, to=2-3[]()
	\arrowfrom=2-3, to=2-4[]()
	\arrowfrom=2-4, to=2-5[]()
	\arrow&quot;\lrcorner&quot;{anchor=center, pos=0.125, rotate=180}, draw=none, from=2-3, to=1-2[]()
\end{tikzcd}" />
We write $f\circ E$ for the pushout.

# Generalization to LES
Write the LES as a sequence of SESs $$E=E_1\circ\cdots\circ E_k$$ and define 
$$
\begin{gather}
\pi E\coloneqq (\pi E_1)\circ E_2\circ\cdots\circ E_k, \\
E\pi\coloneqq E_1\circ\cdots\circ E_{k-1}\circ (E_k\pi).
\end{gather}
$$

# Properties
These operations are not commutative in general, for example given extensions 
$$
\begin{gather}
E_1=0\to A\to X_1\oplus T\to K\oplus T\to 0, \\
E_2=0\to K\to X_2\to C\to 0
\end{gather}
$$ 
and the natural map $\pi:K\oplus T\to K$, we have that $$\pi E_1= 0\to A\to X_1\to K\to 0$$ and $$E_2\pi=0\to K\oplus T\to X_2\oplus T\to C\to 0,$$ and it is clear that $(E_2\pi)\circ E_1\neq E_2\circ (\pi E_1)$.

In certain situations, we formally declare associativity, such as in equivalence relation on $Ext^i$, see [ext functor as extension](notes/ntpy/ext functor as extension.md).
