---
title: "model categories and derived functors"
---

# Idea
Consider two model categories, so that there are notions of fibrant and cofibrant objects. It is sometimes the case that such a functor *almost* behaves homotopically, by which we mean (almost) preserves weak equivalences. To be precise, when we say "almost" we mean that it preserves weak equivalences in the subcategory of fibrant or cofibrant objects.

The model structure comes with a notion of (co)fibrant replacement. We define a new functor on the entire model category to 1) take the (co)fibrant replacement of an object 2) apply the original functor. This new functor preserves weak equivalences in the whole category. This is a derived functor.

But we don't just construct derived functors to show/prove that a given functor preserves weak equivalences, we can also construct them and analyze the extent to which they *fail* to preserve weak equivalences. If the functor is representable, for example, then this tells us things about the object it is representing.

A crucial obstruction to a functor respecting weak equivalences is the failure of (co)limits to respect weak equivalences. This is clear in the context of homotopy equivalences: [(co)limits do not respect homotopy equivalence](notes/ntpy/Key Ideas/Homotopy theory/(co)limits do not respect homotopy equivalence.md). In general, we would like for this to be the case. Now, it goes without saying that adjunctions are ubiquitous. They have the property that right adjoints preserve limits, and left adjoints preserve colimits. It is natural to ask whether such an adjunction descends to the homotopy category, i.e. respects weak equivalences. We can do this by constructing the derived functors. (In the case that the adjunction does descend, we call it a Quillen adjunction).

This may seem divorced from the context in which most of us first encounter derived functors: when working with exact or left/right exact sequences. In particular, we derive functors which are left or right exact. However, this can be seen as a special case of deriving adjunctions. For example, the most prevalent derived functors are $\text{Ext}$ and $\text{Tor}$, and these are derived from the hom-tensor adjunction. But even if we didn't know we were working with an adjunction, we might restate that left exact functors preserve finite limits and right exact functors preserve finite colimits. So not only are all adjunctions left/right exact functors (when they are between appropriate categories, see [lr adjoints imply lr exactness](notes/ntpy/lr adjoints imply lr exactness.md)), the adjoint functor theorem tells also us precisely when a left exact functor is part of an adjunction. So although an adjunctions is stronger than the notion of left/right exact functors (adjoint functors preserve all (co)limits, not just finite ones [adjoints preserve (co)limits](notes/ntpy/Theorems/Category theory/adjoints preserve (co)limits.md)), a very interesting class of left/right exact functors are adjoint functors, besides the fact that adjunctions are of high interest themselves.
# Examples
## ker and coker
Let $R$ be a commutative ring. We first claim that $\text{ker}:\text{Arr}(R\text{Mod})\to R\text{Mod}$ is left exact.

(diagram to be inserted)

Applying $\text{ker}$ induces a diagram $$0\to \text{ker}(f)\overset{f'}{\to}\text{ker}(g)\overset{g'}{\to}\text{ker}(h)\to 0.$$ We will show that this is exact if we remove the last arrow. The only nontrivial thing to show is that $\text{ker}(g')=0$. 

By the initial assumption on exactness, $\text{ker}(f)=0$, so the kernel of the second arrow is the image of the first which is 0. Then also $\text{im}(f')=0$. Obviously $g$ restricted to $\text{ker}(g)$ is 0, so $\text{ker}(g')=0$.

The last part of the exact sequence is no longer (necessarily) exact since $\text{im}(g')=0$ Again by assumption $\ker(g)=\text{im}(f)$ and $\text{im}(g)=C$. By construction above $\text{ker}(g')=\text{ker}(g)$. It suffices to show $\text{im}(f')=\text{ker}(g)$. 

## Ext and Tor
While Ext and Tor are commonly referred to as derived functors, we typically define them to be a little more than just that. Let $R$ be a commutative ring.

The functor we wish to approximate is $\text{Hom}(A,-):\text{Ch}_\bullet(R\text{Mod})\to \text{Ch}_\bullet(R\text{Mod})$. 

- In [inj proj resolutions](notes/ntpy/Definitions/Homological algebra/inj proj resolutions.md), we discuss that projective and injective resolutions play the role of cofibrant and fibrant replacement respectively (with respect to different model structures!).

For it to be a good idea to take the derived functor of $\text{Hom}(A,-)$, we should expect it to be particularly well-behaved on a fibrant or cofibrant replacement. This property is that they are right and left exact sequences, respectively. This is an important property because we can apply $\text{Hom}(A,-)$ to it and see if it preserves the exactness, which will tell us about $A$. If it doesn't preserve exactness we can measure the extent to which this is the case, which also tells us information about $A$. 

With respect to the injective (and projective) model structure, weak equivalences are quasi-isomorphisms, i.e. maps between chain complexes that preserve homology groups. Exact functors preserve quasi-isomorphisms. Hence the above can be interpreted as measuring the extent to which $\text{Hom}(A,-)$ preserves weak equivalences, which matches with our broader characterization of derived functors.

 Now, $\text{Hom}(A,-)$ is exact iff $A$ is a projective module. It is always left exact, so taking a projective resolution (which extends to the left) does not tell us anything new: it is going to remain exact no matter what $A$ is. On the other hand, this is not necessarily the case for an injective resolution (which extends to the right). In other words, the failure of $\text{Hom}(A,-)$ to preserve the exactness of the injective resolution is precisely the extent to which it fails to be an exact functor, i.e. how "far" $A$ is from being a projective module.
 
 Typically we don't speak of this derived functor specifically, but rather the resulting cohomology groups. This is a functor $R\text{Mod}\to \text{Ab}$, which is the composite
 $$
 R\text{Mod}\to \text{Ch}_\bullet(R\text{Mod})\to \text{Ch}_\bullet(R\text{Mod})\to \text{Ab},
 $$
 where the first map is the natural embedding, the second is the derived functor as described above, the third is taking the $i$th cohomology for some choice of $i$.
 Applying it to $B$, we call the result $\text{Ext}_R^i(A,B)$ or the composite functor as $i$th right derived functor.
 
 The presentation above suggests we can extend our notion of $\text{Ext}$ to more general settings.

Dually (adjointly?), the functor $T\otimes (-)$ is exact iff $T$ is flat. It is always right exact. So taking the projective resolution and applying the functor measures how far $T$ is from being flat.
# Related
- [model category](notes/ntpy/Definitions/Homotopy theory/model category.md)
