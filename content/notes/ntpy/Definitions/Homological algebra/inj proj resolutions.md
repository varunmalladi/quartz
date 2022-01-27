---
title: "inj proj resolutions"
---

# Definition
Given a module $M$, a projective resolution is an exact sequence 
$$ \dots\to P_{-1}\to P_0\to M\to 0$$ such that the $P_i$ are projective modules ([inj proj modules](<notes/ntpy/Definitions/Homological algebra/inj proj modules.md>)). 

Dually, an injective resolution is an exact sequence $$0\to M\to I_0\to I_1\to \dots$$ such that the $I_i$ are injective modules.

# Existence
1. For all $M$, there exists a projective module $P_0\to M\to 0$.
2. For all $M$, there exists an injective module 

# Relation to model structures
There are two model structures on the category of chain complexes that we would like to discuss here: the projective model structure and the injective model structure.

- Projective resolutions are cofibrant resolutions in the projective model structure
- Injective resolutions are fibrant resolutions in the model structure

Implicit is that projective complexes are cofibrant and injective complexes are fibrant in their respective model structures. For details on these model structures see [chain complex](<notes/ntpy/Definitions/Homological algebra/chain complex.md>).
