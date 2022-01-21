---
title: "five lemma"
---

# Statement

In an [abelian category](), given a commutative diagram 

<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09A%20%26%20B%20%26%20C%20%26%20D%20%26%20E%20%5C%5C%0A%09%7BA'%7D%20%26%20%7BB'%7D%20%26%20%7BC'%7D%20%26%20%7BD'%7D%20%26%20%7BE'%7D%0A%09%5Carrow%5B%22f%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22g%22%2C%20from%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22h%22%2C%20from%3D1-3%2C%20to%3D1-4%5D%0A%09%5Carrow%5B%22r%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22s%22'%2C%20from%3D2-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22l%22%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22m%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22n%22%2C%20from%3D1-3%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22j%22%2C%20from%3D1-4%2C%20to%3D1-5%5D%0A%09%5Carrow%5B%22t%22'%2C%20from%3D2-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22u%22'%2C%20from%3D2-4%2C%20to%3D2-5%5D%0A%09%5Carrow%5B%22p%22%2C%20from%3D1-4%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22q%22%2C%20from%3D1-5%2C%20to%3D2-5%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	A &amp; B &amp; C &amp; D &amp; E \\
	{A'} &amp; {B'} &amp; {C'} &amp; {D'} &amp; {E'}
	\arrow&quot;f&quot;, from=1-1, to=1-2[]()
	\arrow&quot;g&quot;, from=1-2, to=1-3[]()
	\arrow&quot;h&quot;, from=1-3, to=1-4[]()
	\arrow&quot;r&quot;', from=2-1, to=2-2[]()
	\arrow&quot;s&quot;', from=2-2, to=2-3[]()
	\arrow&quot;l&quot;, from=1-1, to=2-1[]()
	\arrow&quot;m&quot;, from=1-2, to=2-2[]()
	\arrow&quot;n&quot;, from=1-3, to=2-3[]()
	\arrow&quot;j&quot;, from=1-4, to=1-5[]()
	\arrow&quot;t&quot;', from=2-3, to=2-4[]()
	\arrow&quot;u&quot;', from=2-4, to=2-5[]()
	\arrow&quot;p&quot;, from=1-4, to=2-4[]()
	\arrow&quot;q&quot;, from=1-5, to=2-5[]()
\end{tikzcd}" />

then if the rows are exact, $m$ and $p$ are isomorphisms, $l$ is epi, $q$ is mono, then $n$ is is an isomorphism. Sometimes the "five lemma" refers to a weaker statement: if all vertical arrows except the middle are isomorphisms then so is the middle.

We state the "four-lemmas" which in turn immediately imply the five-lemma:
1. Given the commutative diagram 
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09B%20%26%20C%20%26%20D%20%26%20E%20%5C%5C%0A%09%7BB'%7D%20%26%20%7BC'%7D%20%26%20%7BD'%7D%20%26%20%7BE'%7D%0A%09%5Carrow%5B%22g%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22h%22%2C%20from%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22s%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22m%22%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22n%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22j%22%2C%20from%3D1-3%2C%20to%3D1-4%5D%0A%09%5Carrow%5B%22t%22'%2C%20from%3D2-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22u%22'%2C%20from%3D2-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22p%22%2C%20from%3D1-3%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22q%22%2C%20from%3D1-4%2C%20to%3D2-4%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	B &amp; C &amp; D &amp; E \\
	{B'} &amp; {C'} &amp; {D'} &amp; {E'}
	\arrow&quot;g&quot;, from=1-1, to=1-2[]()
	\arrow&quot;h&quot;, from=1-2, to=1-3[]()
	\arrow&quot;s&quot;', from=2-1, to=2-2[]()
	\arrow&quot;m&quot;, from=1-1, to=2-1[]()
	\arrow&quot;n&quot;, from=1-2, to=2-2[]()
	\arrow&quot;j&quot;, from=1-3, to=1-4[]()
	\arrow&quot;t&quot;', from=2-2, to=2-3[]()
	\arrow&quot;u&quot;', from=2-3, to=2-4[]()
	\arrow&quot;p&quot;, from=1-3, to=2-3[]()
	\arrow&quot;q&quot;, from=1-4, to=2-4[]()
\end{tikzcd}" />
if the rows are exact, $m$ and $p$ are epi, and $q$ is mono, then $n$ is epi.
2. Given the commutative diagram
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09A%20%26%20B%20%26%20C%20%26%20D%20%5C%5C%0A%09%7BA'%7D%20%26%20%7BB'%7D%20%26%20%7BC'%7D%20%26%20%7BD'%7D%0A%09%5Carrow%5B%22g%22%2C%20from%3D1-2%2C%20to%3D1-3%5D%0A%09%5Carrow%5B%22h%22%2C%20from%3D1-3%2C%20to%3D1-4%5D%0A%09%5Carrow%5B%22s%22'%2C%20from%3D2-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22m%22%2C%20from%3D1-2%2C%20to%3D2-2%5D%0A%09%5Carrow%5B%22n%22%2C%20from%3D1-3%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22t%22'%2C%20from%3D2-3%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22p%22%2C%20from%3D1-4%2C%20to%3D2-4%5D%0A%09%5Carrow%5B%22f%22%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22l%22%2C%20from%3D1-1%2C%20to%3D2-1%5D%0A%09%5Carrow%5B%22r%22'%2C%20from%3D2-1%2C%20to%3D2-2%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	A &amp; B &amp; C &amp; D \\
	{A'} &amp; {B'} &amp; {C'} &amp; {D'}
	\arrow&quot;g&quot;, from=1-2, to=1-3[]()
	\arrow&quot;h&quot;, from=1-3, to=1-4[]()
	\arrow&quot;s&quot;', from=2-2, to=2-3[]()
	\arrow&quot;m&quot;, from=1-2, to=2-2[]()
	\arrow&quot;n&quot;, from=1-3, to=2-3[]()
	\arrow&quot;t&quot;', from=2-3, to=2-4[]()
	\arrow&quot;p&quot;, from=1-4, to=2-4[]()
	\arrow&quot;f&quot;, from=1-1, to=1-2[]()
	\arrow&quot;l&quot;, from=1-1, to=2-1[]()
	\arrow&quot;r&quot;', from=2-1, to=2-2[]()
\end{tikzcd}" />
if the rows are exact, $m$ and $p$ are mono, $l$ is epi, then $n$ is mono.


# Proof

*Four-lemma 1*
Let $c'\in C'$. We need to show that there exists $c\in C$ such that $n(c)=c'$. Since $p$ is surjective, there exists $d\in D$ such that $p(d)=t(c')$. By exactness on the bottom row, $u(t(c'))=0$. Equivalently, $u(t(c'))=u(p(d))=q(j(d))=0$. By assumption, $q$ is injective, so $j(d)=0\in D$. Hence $d\in\text{ker }j$, so by exactness of the top row $d\in\text{im }h$. Thus there exists $c\in C$ such that $h(c)=d$. Then $t(n(c))=p(h(c))=p(d)=t(c')$. Thus $t(c'-n(c))=0$. So $c'-n(c)\in\text{ker }t$ so by exactness $c'-n(c)\in\text{im }s$. This means there exists $b'\in B'$ such that $s(b')=c-n(c)$. By assumption $m$ is surjective, so there exists $b\in B$ such that $m(b)=b'$. Then $n(g(b))=s(m(b))=c'-n(c)$, so that $n(g(b)+c)=n(g(b))+n(c)=c'-n(c)+n(c)=c'$. Hence $n$ is surjective.

*Four-lemma 2*
Let $c\in \text{ker }n$. We need to show that $c=0$. First observe that $t(n(c))=p(h(c))=0$. By assumption, $p$ is injective, so $h(c)=0$. By exactness on the top row, there exists $b\in B$ such that $g(b)=c$. Then $n(g(b))=s(m(b))=n(c)=0$. So $m(b)\in\text{ker }s$ so by exactness of the bottom row there exists $a'\in A$ such that $r(a')=m(b)$. By assumption $l$ is surjective so there exists $a\in A$ such that $l(a)=a'$. Then $m(f(a))=r(l(a))=r(a')=m(b)$. By assumption $m$ is injective, so $m(f(a))=m(b)$ implies $f(a)=b$. So then $g(f(a))=g(b)=c$. By exactness, $g\circ f=0$ so $g(f(a))=c=0$.

*Five-lemma*
Applying the four-lemmas to the left and right of the diagram, we get that $n$ is injective and surjective, hence is an isomorphism.
