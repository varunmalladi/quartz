---
title: "model category"
---

---
title: "model category"
---

# Idea
To study the homotopy of a category, we wish to pass to a setting which isolates the phenomenon. This is because working with the entire category has "too much" information since we only want to consider things up to homotopy. For instance, if two topological spaces are homotopy equivalent, we wish to consider them as isomorphic when passing to the new setting.

This leads us to our first idea, the homotopy category. This is obtained by taking the same objects and morphisms and adding inverses for all homotopy equivalences, thereby making them isomorphisms. Unfortunately, [Ho(C) is badly behaved](notes/ntpy/Key Ideas/Homotopy theory/Ho(C) is badly behaved.md)<notes/ntpy/Key Ideas/Homotopy theory/Ho(C) is badly behaved.md>). It does not preserve limits, for example. In short, the categorical constructions in the homotopy category don't tell us anything about categorical constructions in the original category, not even up to homotopy.

If the category in question admits the structure of a model category, however, we have an alternative. Namely, we take an object, pass to its [(co)fibrant resolution](notes/ntpy/Definitions/Homotopy theory/(co)fibrant resolution.md)<notes/ntpy/Definitions/Homotopy theory/(co)fibrant resolution.md>), and then take the limit. Taking limits of these special classes of objects does respect homotopy equivalence.

A few issues present themselves:
- We still have a lot of data that isn't stricly related to homotopy
- It might be necessary to work with different model structures to compute limits vs. colimits.
	- For example, in homological algebra, there are two model structures: projective and injective. These have cofibrant and fibrant replacements, respectively, which correspond to projective and injective resolutions (respectively). However, we discuss [here]()<notes/ntpy/Definitions/Homological algebra/inj proj resolutions.md>) that projective resolutions model homotopy limits while injective resolutions model colimits. So it is difficult to relate the two in this setting because we are working with two different model structures.

# References
- https://math.mit.edu/events/talbot/2014/Notes/00.pdf
