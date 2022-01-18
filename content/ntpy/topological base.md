# Idea
Topological bases allow us, in some cases, to more easily describe a topology. It "generates" the topology, in a sense. In fact, every topology has a basis: itself. But there are also nontrivial bases. For instance, the set of open intervals is a basis for the Euclidean topology on the real numbers.

In the other direction, if we have a topology we might search for a tractable basis for it.

# Definition
Let $X\in\text{Set}$, $\mathcal{B}\subset \mathcal{P}(X)$.  
- (Version 2) We call $\mathcal{B}$ a *basis* if 
	- $\mathcal{B}$ covers $X$.
	- Any finite intersection is a union of elements of $\mathcal{B}$.

The set $\tau$ of unions of elements of $\mathcal{B}$ is a topology on $X$, and $\mathcal{B}$ is called a basis of $X$.

- Let $x\in X$, $\mathcal{B}_x\subset \{S\in \mathcal{P}(X)\mid x\in S\}$.
- We call $\mathcal{B}_x$ a *local basis* if
	- Any finite intersection in $\mathcal{B}_x$ is a union of elements of $\mathcal{B}_x$.

# Properties
2. (local to global basis) The set $$\{B_x\mid x\in X\}$$ is a basis for $X$.
3. Every basis has a set of local bases

*Proofs*
**1**
ISTS that any finite intersection in $\mathcal{B}$ is a union of elements in $\mathcal{B}$. Write the finite intersection as $$I=I_1\cap\cdots I_k.$$ For each $x_i\in I_i$, there exist $B_{x_i}^i\in B_{x_i}$ such that $B_{x_i}^i\subset I_i$. It follows that $$I_i=\bigcup_{x_i\in I_i}B_{x_i}^i.$$ Then $I$ is the intersection over 

Each $I_i$ is a union of subsets of $B_x$ for some collection of $x$. In particular, if $x\in I$, then there exist $B_{xi}\in B_x$ such that $B_{xi}\in I_i$ for all $1\leq i \leq k$. We claim that $$I=\bigcup_{1\leq i\leq k} \left(\bigcap_{x\in X}B_{xi}\right).$$
