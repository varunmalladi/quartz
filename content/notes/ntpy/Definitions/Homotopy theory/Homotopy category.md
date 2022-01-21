---
title: "Homotopy category"
---

# Relation to sSet
In [nerve of category](ntpy/Definitions/Category theory/nerve of category.md), we discuss that there is an adjunction

  
<img align="center" src="https://i.upmath.me/svg/%5Cbegin%7Btikzcd%7D%0A%09%7B%5Ctext%7BCat%7D%7D%20%26%20%7B%5Ctext%7BsSet%7D%7D%0A%09%5Carrow%5B%22N%22'%2C%20shift%20right%3D1%2C%20from%3D1-1%2C%20to%3D1-2%5D%0A%09%5Carrow%5B%22h%22'%2C%20shift%20right%3D1%2C%20from%3D1-2%2C%20to%3D1-1%5D%0A%5Cend%7Btikzcd%7D" alt="\begin{tikzcd} {\text{Cat}} &amp; {\text{sSet}} \arrow&quot;N&quot;', shift right=1, from=1-1, to=1-2[]() \arrow&quot;h&quot;', shift right=1, from=1-2, to=1-1[]() \end{tikzcd}" />

witnessing the category of 1-categories (not higher!) as a [reflective subcategory](ntpy/Definitions/Category theory/reflective subcategory.md) of $\text{sSet}$. Thus there is the counit isomorphism $C\cong \text{h}C$. Note this is clearly not an isomorphism in general for higher categories; it is only true in the case of 1-categories because there are no higher morphisms hence no non-isomorphism weak equivalences.

But of course not every simplicial set $X$ arises as the nerve of a 1-category. We must still define $\text{h}(-)$ for all other simplexes. The codomain being the category of small 1-categories is the sense in which we mean the homotopy category is the decategorification of a potentially higher category to a 1-category. For example, quasi-categories are in the domain of this functor.



