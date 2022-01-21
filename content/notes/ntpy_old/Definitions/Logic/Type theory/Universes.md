---
title: "Universes"
---

# Definition
**Definition.** A *universe* is a type whose elements are types.

**Definition.** The types in a particular universe are called *small types*.

# Typical ambiguity
We may wish to regard a universe as containing itself. This quickly leads to paradoxes when taken literally. One way around this is to introduce a hierarchy of universes $$\mathcal{U}_0:\mathcal{U}_1:\mathcal{U}_2:\cdots$$ and broadly refer to this hierarchy as a "universe" $\mathcal{U}$. Then we can say $A:\mathcal{U}$ to mean $A$ inhabits some universe $\mathcal{U}_i$. We can also write $\mathcal{U}:\mathcal{U}$ to mean $\mathcal{U}_i:\mathcal{U}_{i+1}$. 
