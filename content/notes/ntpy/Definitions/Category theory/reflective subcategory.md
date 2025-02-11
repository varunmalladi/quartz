---
title: "reflective subcategory"
---

# Idea
Let $C$ be a category and $U$ a class of morphisms. An object $c\in C$ is called $U$-local if its representable functor $C(-,c)$ is an isomorphism for all $f\in U$. One way to think about why it is called "local" is that, from the perspective of $c$, maps in $U$ look like isomorphisms. Indeed generally if $f:a\to b$ is an isomorphism then the precomposition $C(b,c)\to C(a,c)$ is an isomorphism.

A reflective subcategory $D\subset C$ is a setting in which every object is local. Accordingly, the functor $L:C\to D$ is called a *localization*, or reflector. Formally, it is the left adjoint along the inclusion.

This localization agrees with the standard notion of "inverting a class of morphisms", but why is it stronger? This is essentially because localization is now a left adjoint, meaning it preserves certain limits and colimits. This explains why "good" localizations, such as the localization of a commutative ring at a monoid ([see here](<notes/ntpy/Definitions/Ring theory/Localization of a ring.md>)), commute with other constructions.