---
title: "profinite completion"
---

# Idea
This construction takes any group and gives us an associated [profinite group](ntpy/profinite group.md).

The part "completion" in the name perhaps refers to the fact that a group is dense in its profinite completion.

# Definition
Let $G$ be an abstract group. Define the inverse system $(G/H, \phi_{HH'})$ as follows:
- $I=\{\text{finite index }H\triangleleft G\}$ where $H\leq H'$ iff $H\supseteq H'$
- $\phi_{HH'}:G/H'\to G/H$ is the canonical projection map

The* profinite completion* is the inverse limit of this system:
$$ \widehat{G}=\lim_\leftarrow G/H. $$

# Properties
1. $\widehat{G}$ is a profinite group.
2. $G$ is dense in $\widehat{G}$.
3. The natural map $\gamma:G\to\widehat{G}$ is injective iff $G$ is residually finite (see [profinite topology](ntpy/profinite topology.md)).

# References
- https://www.quora.com/What-is-an-intuitive-explanation-of-profinite-completion-of-a-group
