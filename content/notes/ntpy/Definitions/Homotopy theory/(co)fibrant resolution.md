---
title: "(co)fibrant resolution"
---

# Idea
As discussed in [model categories and derived functors](<notes/ntpy/Key Ideas/Homotopy theory/model categories and derived functors.md>), we can have, say, functors which are homotopical (preserve weak equivalences) only on "good" (i.e. fibrant, cofibrant) objects. Presently we discuss a method of replacing, up to weak equivalence, any object with a fibrant or cofibrant one.
# Definition
A **fibrant resolution** of $X$ is a fibrant object $\hat{X}$ equipped with a weak equivalence into it: $$X\overset{\simeq}{\longrightarrow}\hat{X}\longrightarrow\ast$$

A **cofibrant resolution** of $X$ is a cofibrant object $\tilde{X}$ equipped with a weak equivalence out of it: $$\emptyset\longrightarrow\tilde{X}\overset{\simeq}{\longrightarrow} X$$
# Examples
## Chain complexes
- [inj proj resolutions](<notes/ntpy/Definitions/Homological algebra/inj proj resolutions.md>)

# Related
- [model category](<notes/ntpy/Definitions/Homotopy theory/model category.md>)