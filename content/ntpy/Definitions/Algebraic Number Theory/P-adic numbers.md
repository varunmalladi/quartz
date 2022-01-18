Define $v_p(x)$ to be the largest power of $p$ that divides $x$. Define $v_p(0)=\infty$. Clearly 
$$
v_p(xy)=v_p(x)+v_p(y),\quad v_p(x+y)\geq\min\{v_p(x),v_p(y)\}
$$

## Definition

### Analytic definition
**Definition.** The completion of $\mathbb{Q}$ with respect to $\|\cdot\|_p=s^{-v_p(x)}$, where $s\in\mathbb{R}_{> 1}$ is the field of _p-adic numbers_, denoted $\mathbb{Q}_p$.

**Definition.** Let $\mathbb{Z}_p\subset\mathbb{Q}_p$ denote the valuation ring
$$
\{x\in\mathbb{Q}_p\mid\|x\|\leq 1\}.
$$
It is called the ring of _integer p-adics_.

### Algebraic definition
For $i>1$, define the natural map $\phi:\mathbb{Z}_{p^i}\to \mathbb{Z}_{p^{i-1}}$.

**Definition.** The ring of _integer p-adics_ $\mathbb{Z}_p$ is the limit (in the category of unital rings)
$$
\lim_\leftarrow (\mathbb{Z}_{p^i},\phi_i),
$$
i.e. $\mathbb{Z}_p$ is a sequence
$$
\{{}_ix\in\mathbb{Z}_{p^i}\mid 1\leq i\leq\infty\}
$$
such that for all $i>1$ we have $\phi({}_ix)={}_{i-1}x$.

Consider the ${}_ix$ as fitting the following diagram:
$$
\cdots\longrightarrow\mathbb{Z}_{p^3}\overset{\phi_3}{\longrightarrow}\mathbb{Z}_{p^2}\overset{\phi_2}{\longrightarrow}\mathbb{Z}_p
$$

In this way we see that for $p=5$, a number 31 would be represented as a sequence $(31,\dots,31,6,1)$.

If ${}_ix$ is determined, then there are $p$ possibilities of what ${}_{i+1}x$ could be, corresponding to the $p$ residue classes a number modulo $p^i$ has modulo $p^{i+1}$. 

**Remark.** Consider the absolute value $\|x-y\|=s^{-v_p(x-y)}$ described above. Intuitively, $x$ and $y$ are close if their difference is close to $0$. Since a coordinate of $x-y$ being 0 means automatically that all lower coordinates are 0, we see that $x-y$ become closer if they share the first $n$ coordinates, where $n$ is large. But this means that $v_p(x-y)$ gets bigger and bigger. So for this intuitive closeness to be reflected in the absolute value, we want to raise $s$ to the negative power, so that a larger $v_p(x-y)$ results in a smaller distance between $x$ and $y$.

**Definition.** Let the field of $p$-adics, denoted $\mathbb{Q}_p$, be the field of fractions of $\mathbb{Z}_p$.

Let $\mathbb{Q}_p$ be the field of fractions of $\mathbb{Z}_p$. We can extend $v_p$ to $\mathbb{Q}_p\setminus\{0\}$ by $v_p(z=\frac{x}{y})=v_p(x)-v_p(y)$. Then 
- $v_p(z)$ does not depend on the choice of $x,y\in\mathbb{Z}_p$
- $v_p:\mathbb{Q}_p^\ast\to\mathbb{Z}$ is a group homomorphism.
- This extension defines a nonarchimedean absolute value on $\mathbb{Q}_p$ as it did above.

### Equivalence of definitions
TODO
### Group of units
**Definition.** Let $U=\mathbb{Z}_p^\ast$ denote the group of $p$-adic units. For every $n\geq 1$, write $U_n=1+p^n\mathbb{Z}_p$.

The group of units $U$ completely describes the multiplicative qualities of $\mathbb{Z}_p$, see for example (1) in properties of units below.

## Properties

### Of integer p-adics
1. $\mathbb{Z}_p$ carries a natural structure of a ring with identity.
	- It is an [[Integral domain]]
2. The map $\mathbb{Z}\to\mathbb{Z}_p$ is injective.
3. Multiplication by $p$ (hence also $p^n$) is an isomorphism from $\mathbb{Z}_p$ to itself.
4. Let $\epsilon_i$ be the projection $\mathbb{Z}_p\to\mathbb{Z}_{p^i}$ to the $i$th component. The following sequence is exact: $$0\longrightarrow\mathbb{Z}_p\overset{(-)\cdot p^i}{\longrightarrow}\mathbb{Z}_p\overset{\epsilon_i}{\longrightarrow}\mathbb{Z}/(p^i)\longrightarrow 0.$$ 
5. TFAE:
	- $u\in\mathbb{Z}_p$ is invertible
	- ${}_1u\neq 0$ in $\mathbb{Z}_p$
	- $p\nmid u$ in $\mathbb{Z}_p$.
6. Every nonzero element $z\in\mathbb{Z}_p$ can be uniquely represnted as an invertible element and a power of $p$; i.e. there exists a unique $u\in\mathbb{Z}_p^\ast$ and $n\in\mathbb{Z}_{\geq 0}$ such that $z=p^nu$.
	- The $n$ above is equal to $v_p(z)$.
	- We denote the group of invertible elements of $\mathbb{Z}_p$ by $U$.
7. $\mathbb{Z}$ is dense in $\mathbb{Z}_p$.
7. [[Hensel's lemma]] a (simple!) root modulo $p$ can be lifted to a root modulo any higher power of $p$. By taking the limit, it follows that the root modulo $p$ can be lifted to a root over the $p$-adic integers.
8. Suppose $\alpha\in\mathbb{Z}_p$ and $\alpha\equiv 1\mod p$. The function $$ \begin{gather} \exp_\alpha:\mathbb{Z}_p\to\mathbb{Z}_p \\ z=\alpha^z=\{{}_iz\in\mathbb{Z}/(p^i)\}\mapsto \lim_{i\to\infty}\{\alpha^{\tilde{{}_iz}}\} \end{gather}$$ where $\tilde{{}_iz}\in\mathbb{Z}_{\geq 0}$ is equivalent to ${}_iz\mod p^i$ defines a group homomorphism from the additive group of $\mathbb{Z}_p$ to the subgroup $U_1$ of its group of units $U$.

#### Proofs
##### 1
Suppose $x,y\in\mathbb{Z}_p$ are both nonzero. By part (5), we can write $xy=p^mu_1p^nu_2$. Suppose $xy=0$. Since the $u_i$ are invertible, this would mean $p^{m+n}=0$, which is impossible.
##### 3
Suppose $px=0$. We need to show that $x=0$. To that end, consider that $px=0$ implies $px_{n+1}\equiv 0\mod p^{n+1}$ for all $n$. Then $px_{n+1}=p^{n+1}y_{n+1}$ for some $y_{n+1}\in \mathbb{Z}/(p^{n+1})$. Dividing both sides by $p$, we can write $x=p^ny_{n+1}$. Under the natural homomorphism $\phi_{n+1}:\mathbb{Z}/(p^{n+1})\to\mathbb{Z}/(p^n)$, clearly $\phi(x)=0$ since it has $p^n$ as a factor. Thus $x_n$ is zero (for all $n$).

The corresponding claim for multiplication by $p^n$ follows because it is the $n$-fold composition of maps that are multiplication by $p$, which are injective.
##### 4
By (3), multiplication by $p^i$ is an isomorphism. Clearly $\epsilon_i$ is surjective. So it suffices to show that $\ker\epsilon_i=p^n\mathbb{Z}_p$.

Clearly $p^i\mathbb{Z}_p\subset\text{ker}\epsilon_i$ since the $i$th coordinate is multiplied by $p^i$ so it vanishes. Conversely, let $x\in\ker\epsilon_i$. Since the $i$th coordinate vanishes, all lower order coordinates vanish as well. So just define $y\in\mathbb{Z}_p$ to be the renumbering of the coordinates of $x$ starting with $x_{i+1}=y_1$. Then clearly $x=p^i\cdot y$.
##### 5
The only nontrivial thing is to show that 3 implies 1. Suppose $p\nmid x$.  To show that $x$ is invertible, it suffices to show that each component is invertible. Consider $x_m$. Its image in $\mathbb{Z}/(p)$ is invertible hence there exists $y,z\in\mathbb{Z}/(p^m)$ such that $xy+pz=1$. We claim then that $x_m$ is invertible in $\mathbb{Z}/(p^m)$:
$$
\begin{align}
x(y+ypz+\cdots+yp^{n-1}z^{n-1}) =& xy(1+pz+\cdots+p^{n-1}z^{n-1}) \\
=& (1-pz)(1+pz+\cdots+p^{n-1}z^{n-1}) \\
=& 1.
\end{align}
$$
##### 6
Similar to our discussion in (4). If $x\in\mathbb{Z}_p$ is nonzero, then there exists a largest integer $n$ such that $x_n=0$. Take $u$ to be the renumbering of $x$ starting with $u_1=x_{n+1}$. All its components are nonzero hence $u$ is invertible.
##### 7
We need to show that every $x\in\mathbb{Z}_p$ is the limit of a sequence $(y_n)$ where $y_n\in\mathbb{Z}$. Just take $y_n\equiv x_n\mod p^n$.

### Of p-adics

### Of units
1. $\epsilon_n\mid_U:U\to(\mathbb{Z}/(p^n))^\ast$ is a surjective group homomorphism with kernel $U_n$.
	1. $U/U_1\cong\mathbb{F}_p^\ast$, hence is cyclic of order $p-1$.
2.  By property (5) of integer p-adics, $\mathbb{Q}_p^\ast=p^\mathbb{Z}\times U$ where $U$ is the set of units. 
	1. Let $U_n=1+p^n\mathbb{Z}_p\subset U$. Then $U_n$ is a subgroup and $$\epsilon_n\mid_U:U\to(\mathbb{Z}/(p^n))^\ast$$ from property (3) of integer p-adics is a surjective group homomorphism, and its kernel is $U_n$.
3. (Teichmuller decomposition) $U=T\times U_1$, where $T=\{x\in U\mid x^{p-1}=1\}$ is a cyclic group of $p-1$ elements.
#### Proofs
##### 1
The unrestricted $\epsilon_n$ is already shown to be a surjective ring homomorphism by (4) of integer p-adics. So in particular it sends invertible elements in $\mathbb{Z}_p$ (and therefore invertible elements in $U$) to invertible elements in $(\mathbb{Z}/(p^n))^\ast$. It remains to show the other direction, that if $\epsilon_n(x)$ for $x\in\mathbb{Z}_p$ then $x$ is invertible, hence $x\in U$. An element in $(\mathbb{Z}/(p^n))^\ast$ is invertible if and only if it is relatively prime to $p^n$. So $x$ is invertible if and only if $p\nmid\epsilon_n(x)$. By part (5) of integer p-adics, this shows that $x$ is invertible.

$U_1$ is the kernel of $\epsilon_1:U\to(\mathbb{Z}/p\mathbb{Z})^\ast$. Since $\epsilon_1$ is clearly surjective, $U/U_1\cong(\mathbb{Z}/p\mathbb{Z})^\ast\cong\mathbb{F}_p^\ast$.

### Product formula
**Theorem.** Consider the special set of absolute values on $\mathbb{Q}$
- $\|\cdot\|_\infty=|\cdot|$
- $\|\cdot\|_p=p^{-v_p(\cdot)}$.
Suppose $x\in\mathbb{Q}$. Then
$$
\|x\|_\infty\prod_p\|x\|_p=1.
$$


# Related
[[Absolute value]]