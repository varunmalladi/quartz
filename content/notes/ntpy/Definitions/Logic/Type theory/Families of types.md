---
title: "Families of types"
---

# Definition
**Definition.** A *family of type* $A$ is a function $B:A\to\mathcal{U}$ whose codomain is a [universe](<notes/ntpy/Definitions/Logic/Type theory/Universes.md>).

# Example
1. Family of finite sets
	1. $\text{Fin}:\mathbb{N}\to\mathcal{U}$
2. Constant type family
	1. $(\lambda(x:A).B):A\to\mathcal{U}$
3. Nonexample: the expression $\lambda(i:\mathbb{N}).\mathbb{U}_i$ does not make sense when used to define a family (referring to the hierarchy of universes). Indeed, no universe is large enough to be the codomain (we reach a paradox).