---
title: "Galois extension"
---

# Definition
**Definition.** An [algebraic extension](ntpy/Definitions/Algebraic Number Theory/Field Theory/Algebraic extensions.md) $K/k$ is called *Galois* iff it is [separable](ntpy/Definitions/Algebraic Number Theory/Field Theory/Separable extension.md) and [normal](ntpy/Definitions/Algebraic Number Theory/Field Theory/Normal extensions.md). 

**Definition.** The group $\text{Aut}(K/k)$ of a Galois extension is called the *Galois group*. It is written as $\text{Gal}(K/k)$.

# Properties
1. If $k\subset K\subset\overline{k}$, then $\text{Gal}(K/k)\cong\sum_{K/k}^{\overline{k}/k}$.
2. If $K/k$ is a finite Galois extension, then $\#\text{Gal}(K/k)=[K:k]$.
3. If $H\subset\text{Gal}(K/k)$ is a subgroup, then $$K^H\coloneqq\{x\in K\mid\forall h\in H,\ h(x)=x\}$$ is fixed and a field.
4. [Fundamental thm of Galois Theory](ntpy/Theorems/Field Theory/Fundamental thm of Galois Theory.md)

# Related
- [Field extension](ntpy/Definitions/Algebraic Number Theory/Field Theory/Field extension.md)
