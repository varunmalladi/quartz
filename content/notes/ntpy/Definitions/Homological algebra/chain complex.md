---
title: "chain complex"
---

# Definition
A sequence of modules such that $d^2=0$, i.e. the image of the previous map is contained in the kernel of the next map.

- (**Projective**) A projective chain complex (augmented) over $M$ is a chain complex $$P_\ast\to M\to 0$$ such that the $P_\ast$ are projective modules (see [inj proj modules](notes/ntpy/Definitions/Homological algebra/inj proj modules.md)).
	- Note that this is more general than a projective resolution (see [inj proj resolutions](notes/ntpy/Definitions/Homological algebra/inj proj resolutions.md)), as we are not requiring that the sequence is exact.