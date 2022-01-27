---
title: "group objects"
---

---
title: "group objects"
---

# Idea
A sense in which an object in some category behaves as though it has a group structure. The prototypical example is that of [topological group](notes/ntpy/topological group.md)<notes/ntpy/topological group.md>)s, which are topological spaces with a "compatible" group structure.

# Definition
Let $C$ be a category and $G\in \text{Obj}(C)$.
1. $G$ is a *group object* if there is a well-defined functor $$\text{Hom}(-,G):G^\text{op}\to\text{Grp}.$$ In other words, homs "into $G$" are enriched in $\text{Grp}$.

# Examples
**1** ([topological group](<notes/ntpy/topological group.md>))
There, we mention that a topological group is a group with a topology such that the group operation and inversion maps are continuous. We verify that this is equivalent to such a group being a group object in $\text{Top}$.

We first show that inversion is continuous. $1_
$