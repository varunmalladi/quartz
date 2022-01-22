---
title: "profinite topology"
---

# Definition
Let $G$ be a group. 
- The *profinite topology* on $G$ is the one with base $$\mathcal{B}=\{\text{cosets of finite index normal subgroups}\}$$
- A [topological group](<notes/ntpy/topological group.md>) $G$ is called *residually finite* if it its profinite topology is Hausdorff. 
	- Equivalently, $$\bigcap_{H\in\mathcal{B}}H=\{1_G\}$$ (Property 1).

# Examples
**1**
Galois groups are residually finite. In [direct limit](<notes/ntpy/Definitions/Category theory/direct limit.md>), we describe that a Galois extension $K/k$ is the direct limit of its finite Galois subfields $L/k$: $$K/k\cong\lim_\to L/k.$$ The basis on $G=\text{Gal}(K/k)$ is the set of $\text{Gal}(K/L)$. Suppose $\sigma\in\bigcap_{H\in\mathcal{B}}H$. Then $\sigma$ fixes every $L$, hence fixes $K$, hence $\sigma=1_G$ and by Property (1) we are done.

In fact, Galois groups are even stronger in their topology: they are [profinite group](<notes/ntpy/profinite group.md>)s.

**2** (additive $\mathbb{Z}$ and $\mathbb{R}$)
The profinite topology on $\mathbb{Z}$ is not compact: consider the open cover $$\{U_p\}\cup \{1+5\mathbb{Z}\}\cup \{1-5\mathbb{Z}\},$$ where $U_p=p\mathbb{Z}$ for $p$ prime. There is no finite subcover, as this would imply that there are only finitely many primes.



# Properties
1. $G$ is residually finite iff $\bigcap_{H\in\mathcal{B}}H=\{1_G\}$.
2. An equivalent bases is the one consisting of all left cosets of all subgroups of finite index.
	1. Hence in the profinite topology, every finite index subgroup is open. But this is not generally true for [profinite group](<notes/ntpy/profinite group.md>)s. Namely, the topologies may not agree.

*Proofs*
**2**
The proposed basis contains the one in the definition, so it suffices to consider the other inclusion. Any subgroup contains a nonempty normal subgroup ([core](<notes/ntpy/Definitions/core.md>)) $N\subset H\subset G$. The profinite topology is translation invariant, so for any $g\in H$ we can translate $N$ to an open set $gN$ containing $g$. Since we can do this for every $g\in H$, $H$ is the union of all such translated open sets, hence in the topology.
