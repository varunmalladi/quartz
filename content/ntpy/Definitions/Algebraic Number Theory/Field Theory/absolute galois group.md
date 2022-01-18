---
title: "absolute galois group"
---

# Idea
The absolute Galois group of $F$ can be thought of as the Galois group of the maximal Galois extension of $F$, namely the [[separable closure]] $F^\text{sep}/F$.

It is unique up to conjugation, i.e. multipilication by a conjugate $ghg^{-1}$. This is sometimes called an inner automorphism. Because of this, there is an analogy with the [[funamental groupoid]]: 
- For a topological space, assign to each point the fundamental group at that point. Morphisms are paths between points (which are invertible)
- For a field, assign to each separable closure its absolute Galois group. Morphisms are multipilication by a conjugate, between objects that become equal after the application of the map.

# Properties
1. Let $K/F$ be a finite separable extension in $F^s/F$. Then $G_F$ acts on $\text{Et}(K,F^s)$ (see [[etale algebras]]) by $$\begin{gather} \sigma i\mapsto \sigma \circ i \\ (K\overset{i}{\rightarrow} F)\mapsto (K\overset{i}{\rightarrow}F^s\overset{\sigma}{\rightarrow}F^s,\end{gather}$$ and the kernel of this action is $\text{Gal}(F^s/N)$, where $N$ is the compositum of all conjugates of $K$, i.e. all images of the embeddings $i$.
2. The action in (1) extends to a transitive action of $\text{Gal}(N/F)$ on $\text{Et}(K,F^s)$. 
	1. This process of reduction is like reducing the entire absolute galois group to the galois group of $K/F$, for example:
	2. Consider $\mathbb{Q}(\sqrt[3]{2},\omega)/\mathbb{Q})$. The kernel of the action of $G_\mathbb{Q}$ are those elements that fix the three cube roots of $2$, which is definitionally $\text{Gal}(\overline{\mathbb{Q}}/\mathbb{Q}(\sqrt[3]{2},\omega))$. So the action of $G_\mathbb{Q}$ reduces to an action of $G_\mathbb{Q}/\text{Gal}(\overline{\mathbb{Q}}/\mathbb{Q}(\sqrt[3]{2},\omega))=\text{Gal}(\mathbb{Q}(\sqrt[3]{2},\omega)/\mathbb{Q})$. 

*Proofs*
**1**
We first make a remark on the last part of the property's statement, to verify that the image of $K$ under any $i$ is a conjugate of $K$. Any embedding permutes the roots of the minimal polynomial of $K$, and this is what we mean by a "conjugate" of $K$.

We now wish to verify the kernel of the action is $\text{Gal}(F^s/N)$. Let $\sigma\in\text{Gal}(F^s/N)$. By construction $N$ contains all conjugates of $K$, hence $\sigma$ fixes all embeddings of $K$ in $F^s$. So $\sigma$ is in the kernel. Any element in the kernel likewise fixes any conjugate of $K$, hence is an element of $\text{Gal}(F^s/N)$.

**2**
The action extends in such a way as to remove the kernel: by $(G_F=\text{Gal}(F^s/F))/\text{Gal}(F^s/N)=\text{Gal}(N/F)$. Why is $N$ normal? $F^s$ has all roots of the minimal polynomial of $K/F$ (since it is a separable polynomial so all its roots are separable hence in $F^s$), hence $N$ is the splitting field of that polynomial.

It is transitive because $\text{Gal}(N/F)$ is Galois and $\text{Et}(K,F^s)$ corresponds to different permutations of the roots of the minimal polynomial, on which $\text{Gal}(N/F)$ acts transitively.

To see this another way, let $i_0:K\to F^s$ be an embedding. The stabilizer of $i_0$, under the action of $\text{Gal}(N/F)$ described above, is $\text{Gal}(N/K)\subset\text{Gal}(N/F)$, as the elements that fix (an embedding of) $K\subset F^s$ are definitionally those of $\text{Gal}(N/i_0K)\cong\text{Gal}(N/K)$. By the [[orbit-stabilizer theorem]], the orbit of $i_0$ has size $$|\text{Gal}(N/F)|/|\text{Gal}(N/K)|=[N:F]/[N:K]=[K:F],$$ which implies the action is transitive as the only way the orbit could have that many elements is if it had every conjugate in it.