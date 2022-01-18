---
title: "ext functor as extension"
---

# Definitions
Recall that an extension of $C$ by $A$ is an exact sequence of the form $$0\to A\to B\to C\to 0.$$ We say that two extensions are equivalent if there is a commuting diagram of the form 
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%090%20%26%20A%20%26%20B%20%26%20C%20%26%200%20%5C%5C%0A%090%20%26%20A%20%26%20%7B%5Ctilde%7BB%7D%7D%20%26%20C%20%26%200%0A%09%5Carrow%5B%22%7B%5Ctilde%7Bf%7D%7D%22%2C%20from%3D1-3%2C%20to%3D2-3%5D%0A%09%5Carrow%5BRightarrow%2C%20no%20head%2C%20from%3D1-4%2C%20to%3D2-4%5D%0A%09%5Carrow%5BRightarrow%2C%20no%20head%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5Bfrom%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5Bfrom%3D1-3%2C%20to%3D1-4%5D%0A%09%5Carrow%5Bfrom%3D1-4%2C%20to%3D1-5%5D%0A%09%5Carrow%5Bfrom%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5Bfrom%3D2-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5Bfrom%3D2-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5Bfrom%3D2-4%2C%20to%3D2-5%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	0 &amp; A &amp; B &amp; C &amp; 0 \\
	0 &amp; A &amp; {\tilde{B}} &amp; C &amp; 0
	\arrow[&quot;{\tilde{f}}&quot;, from=1-3, to=2-3]
	\arrow[Rightarrow, no head, from=1-4, to=2-4]
	\arrow[Rightarrow, no head, from=1-2, to=2-2]
	\arrow[from=1-1, to=1-2]
	\arrow[from=1-2, to=1-3]
	\arrow[from=1-3, to=1-4]
	\arrow[from=1-4, to=1-5]
	\arrow[from=2-1, to=2-2]
	\arrow[from=2-2, to=2-3]
	\arrow[from=2-3, to=2-4]
	\arrow[from=2-4, to=2-5]
\end{tikzcd}" />

There is 1-1 correspondence $$\{\text{equivalence classes of extensions of }A \text{ by } B\}\leftrightarrow\text{Ext}^1(C,A).$$

By the notion of the [[pullback and pushforward of ES]], given some extension $E$ and a map $g:C_1\to C$, we may define the pullback extension to just be the SES corresponding to the pullback $E\circ g$. Likewise, we may define the pushforward of an extension $f\circ E$. As noted there, this is not associative in general.

We can generalize the construction above by identifying $\text{Ext}^i(C,A)$ with $i$-fold extensions $$A\to X_1\to\cdots\to X_i\to C\to 0$$ under an *some* equivalence relation. It's not obvious what this should be. However, it seems natural that there should be a map $$\text{Ext}^i(B,A)\times\text{Ext}^j(C,B)\to \text{Ext}^{i+j}(C,A)$$ defined by the concatenation of extensions, e.g. given extensions $$\begin{gather}0\to A\to X_1\to\cdots\to X_i\to B\to 0\\ 0\to B\to Y_1\to\dots\to Y_j\to C\to 0,\end{gather}$$ we may identify the $B$ terms to create a long exact sequence $$A\to X_1\to\cdots\to X_i\to Y_1\to\cdots\to Y_j\to C\to 0.$$ We need to choose our  equivalence relation such that the equivalence class of the result is independent of the choice of representatives of its factors. We would also like there to be "associativity" of pullback and pushout, particularly since we can decompose a LES into the composition of SESs.

In conclusion, we may define an equivelence relation on $\text{Ext}^i$ as follows: given an $i$-fold extension $E$, we may consider its decomposition into short exact sequences $$E=E_1\circ\cdots\circ E_n.$$ Then the equivalence class of $E$ is invariant under the following actions:
1. Changing an $E_i$ for a congruent $\tilde{E_i}$
2. Exchanging two terms $(E_i\pi)\circ E_{i+1}=E_i\circ(\pi E_{i+1})$

# Group Laws
On $\text{Ext}^1$ there is a group law determined by the "exterior sum", e..g given extensions
$$
\begin{gather}
0\to A_1\to B_1\to C_1\to 0\in\text{Ext}^1(C_1,A_1) \\
0\to A_2\to B_2\to C_2\to 0\in\text{Ext}^1(C_2,A_2), 
\end{gather}
$$ 
the exterior sum is 
$$
0\to A_1\oplus A_2\to B_1\oplus B_2\to C_1\oplus C_2\to 0\in\text{Ext}^1(C_1\oplus C_2, A_1\oplus A_2).
$$

In the special case where $A=A_1=A_2$ and $C=C_1=C_2$, then we can actually regard the sum as an element of $\text{Ext}^1(C,A)$ via the [[(co)diagonal map]]s 
$$
\begin{gather}
\Delta_A:A\to A\oplus A \\
a\mapsto (a,a), \\
\nabla_A:A\oplus A\to A \\
(a,a')\mapsto a+a'
\end{gather}
$$
in the following way: first pullback along the diagonal map to obtain $(E_1+E_2)\circ \Delta_C$, then pushout along the codiagonal to obtain $\nabla_A\circ (E_1+E_2)\circ\Delta_C$. This apparently makes $\text{Ext}^1(C,A)$ a monoid.

# Proof of equivalence of definitions

# Related
- [[ext functor]]