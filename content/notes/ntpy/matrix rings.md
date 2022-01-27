---
title: "matrix rings"
---

# Properties
1. ([Skolem-Noether theorem](<notes/ntpy/Skolem-Noether theorem.md>)) All automorphisms of $M_n(K)$ are inner, i.e. given by $M\mapsto CMC^{-1}$ for some invertible $C$.
2. $\text{Aut}(M_n(K))\cong PGL_n(K)$.

*Proofs*
**2**
Consider the homomorphism 

\begin{gather}
GL_n(K)\to\text{Aut}(M_n(K))\\
M\mapsto CMC^{-1}.
\end{gather}
 By (1), this is surjective. We now consider the kernel. Suppose $CMC^{-1}=1$. Since we can make no assumptions on $C$ as it may vary with $M$, we conclude that $M$ is in the center of $GL_n(K)$, hence a scalar matrix. These nonzero scalar matrices are the center $Z$. By definition, $PGL_n(K)=GL_n(K)/Z$, whence the statement.