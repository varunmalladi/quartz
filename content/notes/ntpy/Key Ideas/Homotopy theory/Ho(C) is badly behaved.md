---
title: "Ho(C) is badly behaved"
---

The homotopy category of an $(\infty,1)$-category is not well behaved in the categorical sense. This is perhaps believable because the homotopy category truncates all higher morphisms. These failures include:

- [(co)limits do not respect homotopy equivalence](notes/ntpy/Key Ideas/Homotopy theory/(co)limits do not respect homotopy equivalence.md)
- Etc. 

In fact this is a reason for developing and working with [model categories](notes/ntpy/Definitions/Homotopy theory/model category.md): when we pass to [fibrant/cofibrant resolutions](notes/ntpy/Definitions/Homotopy theory/(co)fibrant resolution.md), limits of these special class of objects do align with homotopy limits. 

Another moral reason why the homotopy category is insufficient is because it is an ordinary localization corresponding to the [reflective subcategory](notes/ntpy/Definitions/Category theory/reflective subcategory.md) of small categories in simplicial sets. But the setting we wish to work in is that of an $(\infty,1)$-category, so we actually want to consider the $(\infty,1)$-reflective subcategory and its corresponding localization.

The abstract construction above is modelled by Bousfield localization.

# References
- https://math.stackexchange.com/questions/3795052/what-is-an-infinity-category-really (particularly shibai's answer)