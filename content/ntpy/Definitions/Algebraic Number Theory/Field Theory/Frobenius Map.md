Suppose $K$ is a field of characteristic $p$. The **absolute Frobenius map** is the map
$$
\begin{gathered}
\text{Fr}:K\to K \\
x\mapsto x^p
\end{gathered}.
$$

**Proposition.** The absolute Frobenius map is a field homomorphism.

_Pf_ We check:
1. $(xy)^p = x^py^p$.
2. $(x^{-1})^p = x^{-p} = (x^p)^{-1}$.
3. $$
\begin{align}
(x-y)^p =& \sum_{i=0}^p (-1)^{p-i} {p\choose i} x^i y^{p-i} \\
=& - {p\choose 0}x^0 y^p + {p\choose p}x^p y^0 \\
=& x^p-y^p.
\end{align}
$$
We were able to reduce the binomial expansion because all the ${p \choose i}$ are divisible by $p$ except for $i=0,p$. This is because $i!$ and $(p-1)!$ are coprime with $p$ for these values of $i$ since their factors are less than $p$. Then use the fact that the binomial coefficient is always an integer. 

The negative signs above would differ if $p=2$, but in that case addition and subtraction are the same anyways.

**Lemma.** If a field $K$ is finite, then the Frobenius map is an automorphism.

_Pf._ Every field homomorphism is injective, and an injective map between fields of the same order is necessarily surjective as well, hence an isomorphism.