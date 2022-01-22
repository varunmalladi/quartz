---
title: "topological group"
---

# Idea
A group with a topology that interacts nicely with the group operations.

# Definition
- A *topological group* is a group with a topology such that the operations of "multiplication" 
$$
\begin{gather}
G\times G\to G \\ 
(g,h)\mapsto gh
\end{gather}
$$
and "inversion" 
$$
\begin{gather}
G\to G \\
g\mapsto g^{-1}
\end{gather}
$$
are continuous.
- They are precisely the [group objects](<notes/ntpy/Definitions/Category theory/group objects.md>) in the category $\text{Top}$.

# Examples
1. (Hilbert's fifth problem) If $G$ is a topological group and a manifold, then it is also a Lie group.
2. Every group under the discrete topology
3. Every group under the [profinite topology](<notes/ntpy/profinite topology.md>)
4. Products and subgroups of topological groups
5. [lie group](<>)

# Properties
1. Every topological group's topology is translation invariant, i.e. left or right multipilication is a homeomorphism.
	1. Conjugation is also a homeomorphism.
2. Every open subgroup is also closed.
3. For $H\triangleleft G$, the quotient map $q:G\to G/H$ is open.
4. $G/H$ with the quotient topology is a topological group.
5. The closure $\overline{H}$ of any subgroup $H$ of $G$ is a subgroup.
6. The closure of any normal subgroup is normal.
7. The trivial subgroup $\{1_G\}$ is closed iff $G$ is Hausdorff. Thus $G/\overline{1_G}$ is a Hausdorff topological group.

*Proofs*
**1**
Multiplication is already required to be continuous, and the continuous inverse is multiplication on the same side by the inverse element. The two sets are in bijection as well.

**2**
Let $g\in G\setminus H$. Then $gh\not\in H$ since $h^{-1}\in H$ and this would imply $ghh^{-1}=g\in H$. In particular, $g\in gH$. So $$G\setminus H=\bigcup_{g\in  G\setminus H}gH.$$ By Property (1), each $gH$ is open, as it is just a translation of an open set ($H$). Thus $G\setminus H$ is open, so $H$ is closed.

For the subparts, what is left is the case where $H$ is neither open nor closed.

**3**
By definition, open sets in the quotient topology are those whose preimage is open, whence $q$ is tautologically continuous. Suppose $U\subset G$ is open. We need to show that $q(U)$ is open. This true iff $q^{-1}(q(U))$ is open, as $q$ is continuous. Observe that $$q^{-1}(q(U))=\bigcup_{h\in H}hU.$$ $U$ is open and $hU$ is a translation, so by Property 1 $hU$ is open, and so $q^{-1}(q(U))$ is open.

**4**
ISTS that multiplication and inversion are continuous. 

Regarding multipilication: for $[xy]\in G/H$, an open neighborhood $S'$ has preimage (under quotient) an open set $S$ in $G$ containing $xy$. Since multipilication map in $G$ is continuous, there exist neighborhoods $x\in U$, $y\in V$ such that $UV\subset S$. Under quotient, these correspond to open sets $[x]\in U'$, $[y]\in V'$. It remains to show that $U'V'\subset S'$, but this is immediate.

Regarding inversion: let $[x^{-1}]\in V'$ be a neighborhood. We need to show that there exists a neighborhood $[x]\in U'$ such that $(U')^{-1}\subset V'$. The quotient is continuous, so there exists a neighborhood $x^{-1}\in V$ such that $[V]\subset V'$. Inversion is continuous in $G$, so there exists a neighborhood $x\in U$ such that $U^{-1}\subset V$. The image of this under quotient is an open set $U'$, and this is the desired set.

**5**
Property (2) is not enough, as it could be the case that $H$ is neither open nor closed.

Let $a,b\in \overline{H}$. Let $ab\in S$ be a neighborhood. Then there exist neighborhoods $a\in U$, $b\in V$ such that $UV\subset S$.
