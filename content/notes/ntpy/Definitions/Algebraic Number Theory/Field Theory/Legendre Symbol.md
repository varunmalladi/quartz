---
title: "Legendre Symbol"
---

**Definition.** Let $a$ be any residue modulo $p$. The Legendre symbol is 
$$
\left(\frac{a}{p}\right)\coloneqq a^{(p-1)/2} 
$$

Recall that if $a\neq 0$ then $\left(\frac{a}{p}\right)=\pm 1$.

Define $\left(\frac{0}{p}\right)=0$.

By this [thm.](<notes/ntpy/Theorems/Field Theory/Field Characteristic and Squares.md>), we see that the Legendre symbol is tracking the data for squares modulo $p$.

## Results

**Theorem.** 
1. The symbol is multiplicative: $(\frac{a}{p})(\frac{b}{p})=(\frac{ab}{p})$.
2. $(\frac{1}{p})=1$
3. $(\frac{-1}{p})=(-1)^{(p-1)/2}$.
4. $(\frac{2}{p})=(-1)^{(p^2-1)/8}$.

_Pf of statements 1-3._ Immediate from the definition.

_Pf of statement 4._ Consider $\mathbb{F}_p$ as a subgroup of $\Omega$, an algebraically closed fieldd with characteristic $p$. We first will calculate $\sqrt{2}$ in $\Omega$ (which exists since it is algebraically closed). Then we will check under which conditions that element is in $\mathbb{F}_p$. 

Let $\zeta$ be a solution to $\zeta^4+1=0$. These correspond to the "primitive 8th roots of unity," where "primitive" refers to those roots not on an axis. Define $\tau\coloneqq\zeta+\zeta^{-1}$. Then
$$
\begin{align}
\tau^2 =& (\zeta+\zeta^{-1})^2 \\
=& \zeta^2 + 2\zeta\zeta^{-1} + \zeta^{-2} \\
=& (\zeta^2 + \zeta^{2}\zeta^{-4}) + 2 \\
=& (\zeta^2 - \zeta^{2}) + 2 = 2
\end{align}
$$
where we used the fact that $\zeta^4=-1$ implies $\zeta^{-4}=-1$. Hence $\tau=\sqrt{2}$. 

It remains to check under which conditions $\tau\in\mathbb{F}_p$. This happens if and only if $\tau^{p-1}=1$ or equivalently $\tau^p = \tau$. We calculate that
$$
\begin{align}
\tau^p =& (\zeta+\zeta^{-1})^p = \text{Fr}(\zeta+\zeta^{-1}) \\
=& \text{Fr}(\zeta) + Fr(\zeta^{-1}) = \zeta^p + \zeta^{-p}.
\end{align}
$$
So we need to check under which conditions $\zeta^p+\zeta^{-p}=\zeta+\zeta^{-1}$. We claim this happens precisely when $p=1$ or $p\equiv 7\mod 8$.

Let us prove the reverse direction first. Clearly if $p=1$ the statement is true, so suppose $p\equiv 7\mod 8$. Since $\zeta^4+1=0$ by assumption, it follows that $\zeta^4=-1$ and so $\zeta^8=1$. This means $\zeta^7=\zeta^{-1}$ and $\zeta^{-7}=\zeta$. So $\zeta^p+\zeta^{-p}=\zeta^{-1}+\zeta$ as desired.

Now let us prove the forward direction, so suppose $\zeta^p+\zeta^{-p}=\zeta+\zeta^{-1}$. Clearly it is possible that $p=1$. It remains to show that the only other possibility is $p\equiv 7\mod 8$. We will prove by contradiction: suppose there exists $p\equiv b\mod 8$ satisfying the above equation where $0<b<8$ is an integer, $p\neq 1$, and $b\neq 7$.
