---
title: "Finite Fields of Prime Power Order"
---

Let $p$ be prime, and $f$ be a positive integer. Let $q=p^f$. Let $\Omega$ be an algebraically closed field with characteristic $p$. Then:
1. $x^q-x=0$ has $q$ different solutions in $\Omega$. The set of the solutions is a subfield, call it $\mathbb{F}_q$.
2. For all $p$, $\Omega$ does exist. For any field $K$ such that $|K|=q$, there exists an isomorphism $K\cong \mathbb{F}_q$, i.e. this is the only finite field of that order.
3. $\mathbb{F}_p\cong\mathbb{Z}_p$ (in one sense) and $\mathbb{F}_q \supset\mathbb{F}_p$.

_Pf of statement 1._ 
Since $\Omega$ is algebraically closed, the polynomial $x^q-x$ splits into $q$ linear factors. It remains only to show that these factors are distinct. To that end, consider the (formal) derivative is $qx^{q-1}-1=-1$. But if the polynomial had a repeated root, then that root would also be a root of the derivative by considering the power and product rule. Hence it cannot have a repeated root. Another way of seeing this is by observing that $F$ and $F'$ are relatively prime in that the greatest common polynomial divisor is 1. Thus they have no common roots. 

To see that the set of roots is a subfield, observe that the set can be expressed as
$$
\{ x\in|Omega \mid \text{Fr}^f(x)=x \}
$$
where
$$
\begin{gathered}
\text{Fr}:x\mapsto x^p \\
\text{Fr}^f: x\mapsto x^{pf}=x^q.
\end{gathered}
$$
Hence the roots are precisely the set of fixed points of the $\text{Fr}^f:\Omega\to \Omega$, hence a subfield of $\Omega$, as it is the image of a field homomorphism.

_Pf of statement 2._
Let $K^+$ be the additive group of $K$, and $|K|=q$. Since $q\cdot 1 = 0$ it follows that $p\cdot 1=0$ which implies the characteristic of $K$ is $p$.

By a theorem, $\Omega$ exists and for any field $K$ of $q$ elements there exists and inclusion $K\hookrightarrow \Omega$. 

Now consider $L=i(K)\subset\Omega$. By properties of homomorphism, $|L|=|K|=q$ and indeed $K\cong L$. Hence $|L^\ast|=q-1$ so for all $x\in L^\ast$ we have $x^{q-1}=1$ so $x^q=x$ and $0^q=0$, which shows that $L\cong F_q$. So $K\cong F_q$.

_Pf of statement 3._
Consider the $(p-1)$-fold sums of 1. It forms a subring in $\Omega$ isomorphic to $\mathbb{Z}_p$, hence it is a subfield of order $p$. By part 2, it is therefore isomorphic to $\mathbb{F}_p$ as defined in part 1.

$\mathbb{F}_q\supset \mathbb{F}_p$ since $x^p=x$ implies $x^{q}=x$.
