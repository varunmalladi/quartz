---
title: "snake lemma"
---

# Statement

In an [[abelian category]], consider a commutative diagram 

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%26%20A%20%26%20B%20%26%20C%20%26%200%20%5C%5C%0A%090%20%26%20%7BA'%7D%20%26%20%7BB'%7D%20%26%20%7BC'%7D%0A%09%5Carrow%5B%22f%22%2C%20from%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22g%22%2C%20from%3D1-3%2C%20to%3D1-4%5D%0A%09%5Carrow%5Bfrom%3D1-4%2C%20to%3D1-5%5D%0A%09%5Carrow%5Bfrom%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22%7Bf'%7D%22%2C%20from%3D2-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22%7Bg'%7D%22%2C%20from%3D2-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22a%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22b%22%2C%20from%3D1-3%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22c%22%2C%20from%3D1-4%2C%20to%3D2-4%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	&amp; A &amp; B &amp; C &amp; 0 \\
	0 &amp; {A'} &amp; {B'} &amp; {C'}
	\arrow[&quot;f&quot;, from=1-2, to=1-3]
	\arrow[&quot;g&quot;, from=1-3, to=1-4]
	\arrow[from=1-4, to=1-5]
	\arrow[from=2-1, to=2-2]
	\arrow[&quot;{f'}&quot;, from=2-2, to=2-3]
	\arrow[&quot;{g'}&quot;, from=2-3, to=2-4]
	\arrow[&quot;a&quot;, from=1-2, to=2-2]
	\arrow[&quot;b&quot;, from=1-3, to=2-3]
	\arrow[&quot;c&quot;, from=1-4, to=2-4]
\end{tikzcd}" />

where the rows are exact sequences and 0 is the [[Zero object]].

Then there is an exact sequence $$\text{ker }a\to\text{ker }b\to\text{ker }c\overset{d}{\longrightarrow}\text{coker }a\to\text{coker }b\to\text{coker }c.$$ The map $d$ is a homomorphism called the connecting homomorphism.

# Corollaries
1. If the two sequences are short exact (not just right/left exact) then the induced sequence is too, i.e. the sequence $$0\to\text{ker }a\to\text{ker }b\to\text{ker }c\overset{d}{\longrightarrow}\text{coker }a\to\text{coker }b\to\text{coker }c\to 0$$ is exact.

**Proofs**
*1*
It suffices to show that $\text{ker }a\to\text{ker }b$ is injective and $\text{coker }b\to\text{coker }c$ is surjective. First we will show that $\text{ker }a\to\text{ker b}$ is injective. By assumption, $f$ is injective, so its kernel is trivial, hence $\text{ker }a\to\text{ker }b$ is injective.

Now we will show that $\text{coker }b\to\text{coker }c$ is surjective. By assumption $g'$ is surjective. To show that the induced map $B'/\text{im }b\to C'/\text{im }c$ is surjective, it suffices to show that $g'(\text{im }b)\subset\text{im }c$. Let $y\in\text{im }b$. Then there is $x\in B$ such that $b(x)=y$. Then also $c(g(x))=g'(b(x))=g'(y)$, hence the preimage of $g'(y)$ by $c$ is $g(x)\in C$. So $g'(y)\in\text{im }c$, and since our choice of $y\in\text{im }b$ was arbitrary this shows that $g'(\text{im }b)\subset\text{im }c$.