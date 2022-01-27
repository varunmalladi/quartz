---
title: "homotopy category, nerve, and decategorification"
---

# Introduction

We generally understand ordinary categories pretty well. By ordinary, we mean a (potentially small) category which is a collection of objects and morphisms adhering to a set of conditions. We have a grasp of what it means to "do category theory" in this setting: functors, limits, adjunctions, etc. 

This is not enough for homotopy theory. In topology, we can have a pair of paths, and be able to continuously deform one path into the other. This is a homotopy, and viewing a path as a morphism we get that a homotopy is just a morphism of morphisms, a 2-morphism.

The problem is that our ordinary categorical constructions don't account for higher morphisms, like the 2-morphisms. They don't have defined behavior there, so 1-categorical constructions can't directly tell us anything about the higher morphisms.

At this point, we have two options. The first is to develop category theory for higher categories. This seems like the morally correct approach, but it is quite difficult, and an area of active research. The specialization to the special case of $(\infty,1)$-categories is the subject of "infinity category theory".

The second approach is far easier, and therefore worth considering: somehow compress the higher category into a 1-category, and then do our normal categorical constructions. The hope is that this will tell us something about the higher category. Naturally, we lose information when we do this, but the hope is that we preserve just enough to say something about the higher category.

The difficult part is deciding how to compress a higher category into a 1-category.

# Approach 1: forget higher structure
Well the first idea one might suggest is to simply "forget" the higher structure. This means, entirely ignore all morphisms higher than 1. In the category of topological spaces, this looks like forgetting all homotopies, for example. If we do this, we are left with a 1-category and then we can do our usual constructions. To summarize this approach, we are simply regarding the higher category as a 1-category and ignoring all higher structure.

There is nothing wrong here, except that it does little for the homotopy theorist! Indeed, by forgetting higher structure we have forgotten that two paths are homotopic: we have forgotten homotopies, the very thing we were trying to study!

# Approach 2: homotopy category
The second approach is to form the homotopy category. The idea is the following: when we just forgot the higher structure, we completely destroyed any relationship that two homotopic morphisms had to each other. Instead, we could simply forget *how* they are related. By this we mean we just treat homotopic maps as isomorphic, i.e. identify homotopic maps. This immediately makes all higher morphisms trivial, and we again obtain a 1-category. As opposed to the first method, this preserves a little more information. 

There is, of course, the question of how to construct it, and what properties it preserves of the higher category. Here I want to take a slightly more pedantic and motivated approach via the nerve construction.

# Simplicial sets and higher categories
There is a way of conceptualizing higher morphisms using simplicial sets. Let's take 2-morphisms. 

As alluded to above, in homotopy theory we are concerned with $(\infty,1)$-categories. As you might expect, we can model such a category as a special simplicial set. In fact, there are several models, all of which generally agree with each other. We take here the quasi-category model, developed by Joyal and expanded on by Lurie.

# Nerve construction
There is a simple way to construct a simplicial set out of a 1-category, and this construction is called the nerve construction. It sends the objects to 0-simplices, morphisms to 1-simplices, and compositions to higher simplices. For instance, the composition $h=g\circ f$ would be represented as a 2-simplex:


<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%26%20b%20%5C%5C%0A%09a%20%26%26%20c%0A%09%5Carrow%5B%22%22%7Bname%3D0%2C%20anchor%3Dcenter%2C%20inner%20sep%3D0%7D%2C%20%22h%22'%2C%20from%3D2-1%2C%20to%3D2-3%5D%0A%09%5Carrow%5B%22f%22%2C%20from%3D2-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22g%22%2C%20from%3D1-2%2C%20to%3D2-3%5D%0A%09%5Carrow%5Bshorten%20%3C%3D5pt%2C%20shorten%20%3E%3D5pt%2C%20Rightarrow%2C%20from%3D1-2%2C%20to%3D0%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd}
	&amp; b \\
	a &amp;&amp; c
	\arrow&quot;&quot;{name=0, anchor=center, inner sep=0}, &quot;h&quot;', from=2-1, to=2-3]
	\arrow&quot;f&quot;, from=2-1, to=1-2]
	\arrow&quot;g&quot;, from=1-2, to=2-3]
	\arrowshorten &lt;=5pt, shorten &gt;=5pt, Rightarrow, from=1-2, to=0]
\end{tikzcd}" />

The vertical 2-morphism just being the identity, witnessing the equality of $g\circ f$ and $h$. 3-simplices would correspond to the composition of 3 morphisms, which makes sense because it would need to include the data of the composition of pairs of morphisms within that set.

We are being informal here to get to the point, but it is not too difficult hopefully to see that this defines a simplicial set. In fact, it would appear the nerve really preserves all the information about the original category. This is indeed the case, as one shows that the nerve construction is fully faithful. In other words, the set of functors between two categories are in bijection with the morphisms between their nerves.

# Reflective subcategories
When a fully faithful functor $C\to D$ admits a left adjoint, we call the left adjoint the reflector or localization. We say that $C$ is a [reflective subcategory](notes/ntpy/Definitions/Category theory/reflective subcategory.md) of $D$. 

Localizations are of course central to many areas of mathematics, such as commutative algebra for example. Now, this isn't intended to be a video on localization or reflective subcategories, so I will just say a few things. 

Firstly, that this is an adjunction means that we aren't arbitrarily moving between categories: constructions and considerations in one category carry over, to an extent, to the other category. This is what we were hoping to do with the homotopy category: obtain a 1-category that tells us something about the higher category.

Secondly, not every localization need arise in this manner, i.e. there are more general ways to define localization. However, a localization presented as a reflective subcategory does agree with the standard notion of universally inverting a class of morphisms. The strength of being a reflective subcategory is the following:

1. the inclusion $C\hookrightarrow D$ creates all limits that $C$ admits
2. $D$ has all colimits that $C$ admits, formed by applying the reflector to the colimit in $C$.

This adjunction also constitutes an idempotent monad, by which we just mean that localizing twice does not provide any "extra" information.

# Fundamental category functor
So we have a canonical way to move from small 1-categories to simplicial sets $$N:\text{Cat}\longrightarrow \text{sSet}$$ and moreover this is a fully faithful functor. So we should try to construct its left adjoint, a localization functor.