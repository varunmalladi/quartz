---
title: "profinite group"
---

# Definition
- A group $G$ is *profinite* if it is isomorphic to an [[inverse limit]] of finite groups.

**Remark.** We could replace the suffix "finite" with other things, like prosolvable, etc.

# Examples
**1** ([[profinite completion]])

**2** (p-adic integers, see [[P-adic numbers]])
$$\mathbb{Z}_p=\lim_\leftarrow\mathbb{Z}/(p^n),$$ which is also a procyclic group per the remark in the definition.

**3** (Galois groups)
Every Galois group is profinite. In particular, $$\begin{gather} \text{Gal}(K/F)\overset{\simeq}{\rightarrow}\lim_{\overset{\leftarrow}{\underset{L/F \text{ finite Galois}}{K/L/F}}}\text{Gal}(L/F) \\ \sigma\mapsto (\sigma|_L)\end{gather}$$
To see this, regard the adjunction of categories of subextensions of $K/F$ (take the opposite category, actually) and subgroups of $\text{Gal}(K/F)$, with right adjoint $L/F\mapsto \text{Gal}(K/L)$ and left adjoint $H\mapsto K^H$ ([[Fundamental thm of Galois Theory]]). In [[direct limit]], we have $K/F\cong\underset{\rightarrow}{\lim}L/F$ where we range over $L/F$ finite Galois. By properties of right adjoint in the opposite category, this means that $R(K/F)=1=\underset{\leftarrow}{\lim}\text{Gal}(K/L)$. For each $L/F$ there is an exact sequence $\text{Gal}(K/L)\to G\to \text{Gal}(L/F)$. By property (1) of [[inverse limit]], this means there is an exact sequence $$\underset{\leftarrow}{\lim}\text{Gal}(K/L)=1\to \underset{\leftarrow}{\lim}G=G\to \underset{\leftarrow}{\lim}\text{Gal}(L/F),$$ whence it follows that $$G/1=G=\underset{\leftarrow}{\lim}\text{Gal}(L/F).$$

# Properties
Let $G=\underset{\leftarrow}{\lim}G_i$ be a profinite group.
1. Consider each $G_i$ with the discrete topology. Then $G$ is 
	1. compact, assuming [[Tychanoff's theorem]]. 
	2. Hausdorff
	3. totally disconnected
2. $G$ is a profinite group iff $G$ is a compact, Hausdorff, totally disconnected topological group.