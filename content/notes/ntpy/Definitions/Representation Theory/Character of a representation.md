---
title: "Character of a representation"
---

# Idea
Eigenvalues play a very important role in understanding invariant subspaces of a representation, and thus the representations themselves. Calculating eigenvalues for every element of $G$ can be very tedious, though. The key observation is that it suffices to know the sum of eigenvalues for every element in $g$.
# Definition
Let $T$ be a representation of $G$ on $V$.

**Definition.** The _character_ of $T$ is the function \begin{gather}\chi_V:G\to\mathbb{F} \\ g\mapsto \text{Tr}(Tg).\end{gather}

# Properties
1. $\chi_{V\oplus W}=\chi_V+\chi_W$
2. $\chi_{V\otimes W}=\chi_V\cdot \chi_W$
3. $\chi_{V^\ast}=\overline{\chi}_V$
4. $\chi_{\Lambda^2V}(g)=\frac{1}{2}[\chi_V(g)^2]-\chi_V(g^2)]$
5. If $G$ is a finite group and $T$ is a complex representation, then there exists an inner product in $V$ such that $T(g)$ is [unitary for every](<notes/ntpy/Definitions/Unitary operator.md>) $g\in G$.