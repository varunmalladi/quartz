---
title: "group cohomology"
---

# Definition
## H1
### Idea
Let $G$ be a group, and $A$ another group equipped with a left $G$-action. We wish to study maps $G\to A$ that respect the $G$-action on $A$. The point is, it is not enough to just study group homomorphisms. Consider a group homomorphism $f:G\to A$. Then $f(gh)=f(g)f(h)$. 


- A *1-cocycle* of $G$ with values in $A$ is a map $$\phi:\sigma\mapsto a_\sigma$$ such that $$\phi(\sigma\tau)=\phi(\sigma)\cdot\sigma\cdot\phi(\tau)=a_\sigma\cdot\sigma(a_\tau).$$
- Two 1-cocycles $\phi,\psi$ are *equivalent* or *cohomologous* if there exists $c\in A$ such that $$\phi(\sigma)=c^{-1}\psi(\sigma)\sigma c.$$ 
