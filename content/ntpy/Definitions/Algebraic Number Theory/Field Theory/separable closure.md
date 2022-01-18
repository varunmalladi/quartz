# Idea
The separable closure of $F$, denoted $F^\text{sep}$, is the "biggest Galois extension of $F$". This is the result of two facts:
1. $F^\text{sep}$ is the maximal separable extension of $F$
2. $F^\text{sep}$ is a normal extension

# Definition
- A [[Field extension]] $K/F$ is called *separably closed* if every (nonconstant) seperable polynomial in $F$ has a root in $K$.
- $K/F$ is a *separable closure* if it is separably closed and separable.

Equivalently, let us define an element to be separable over $F$ if its minimal polynomial is separable. Then
- $F^\text{sep}$ is the collection of all separable elements over $F$.

**Remark.** The requirement of being separable (in addition to being separably closed) is not redundant: take the separable closure and add a transcendental element. The result is separable closed but not separable. We have implied the following:
1. $F^\text{sep}$ is the maximal separable extension of $F$.

# Properties
1. $F^\text{sep}$ is the maximal separable extension of $F$.
2. $F^\text{sep}$ is normal.
3. $F^\text{sep}/F$ is Galois, and also the maximal Galois extension of $F$.

*Proofs*
**2**
It suffices to show that if an irreducible polynomial in $F$ has a root in $F^\text{sep}$, then all roots are contained there. Let $P$ be an irreucible polynomial in $F$. If it has a root in $F^\text{sep}$, then that root must be separable, meaning its minimal polynomial is separable. The minimal polynomial is unique, so it must be $P$. But then all other roots of $P$ are seperable, hence they all belong to $F^\text{sep}$.




