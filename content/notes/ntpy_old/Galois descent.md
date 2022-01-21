---
title: "Galois descent"
---

# Idea
The oppose of ascent, see [base change, ascent](ntpy/Key Ideas/base change, ascent.md). 

For vector spaces, it asks: given a field extension $L/K$ and a nonzero $L$-vector space $V$, how can we construct a $K$-vector space $W$ such that the $K$-basis of $W$ naturally extends to a $K$-basis (e.g. if $\{e_i\}$ is the $K$-basis, an example of a natural extension would be if $\{1\otimes e_i\}$ was an $L$-basis).

# Vector spaces
Let $K/F$ be a Galois extension, $G=\text{Gal}(K/F)$. Let $V$ be an $F$-vector space.
- $V\otimes_F K$ is a $K$-vector space via $\alpha(v\otimes\beta)=v\otimes \alpha\beta$. (see [base change, ascent](ntpy/Key Ideas/base change, ascent.md)). 
- $G$ acts on $V\otimes_F K$ via $$\sigma(v\otimes\alpha)=v\otimes \sigma(\alpha).$$ 
Let $W$ be a $K$-vector space. 
- An action of $G$ on $W$ is $K/F$-semilinear, i.e. for $\alpha\in K/F$, $$\sigma(\alpha\omega)=\sigma(\alpha)\sigma(\omega).$$
	- This is because $\sigma$ is a homomorphism.
- Thus $W^G$ is an $F$-vector space.
	- $f\sigma(\omega)=\sigma(f)\sigma(\omega)=\sigma(f\omega)=f\omega\in W^G$.
## Properties
Let $K/F$ be a Galois extension, $G=\text{Gal}(K/F)$. Let $V$ be an $F$-vector space, $W$ be a $K$-vector space.

1. The map $$\begin{gather}V\to (V\otimes_F K)^G \\ v\mapsto v\otimes 1\end{gather}$$ is an $F$-linear isomorphism.
2. The map $$\begin{gather}W^G\otimes_F K\to W\\ \omega\otimes\alpha\mapsto \alpha\omega\end{gather}$$ is a $K$-linear isomorphism.
3. (Galois descent for vector spaces) Let $(K,G)$ denote a $K$-vector space withh a similinear $G$-action. Then there is a quasi-inverse pair of equivalences (=adjunction or equiv of cats?) $$\begin{gather}\text{Vect}_F\overset{\rightarrow}{\leftarrow}\text{Vect}_{(K,G)}, \\ V\mapsto V\otimes_F K \\ W^G\leftarrow W.\end{gather}$$
	1. We can replace "vector space" with "algebra" in the statement above.

*Proofs*
**1**
If $V=F$, then $V\otimes_F K=K$ and $V=F=K^G$.

In the general case we may write $V=\bigoplus_i F$.

**2**
