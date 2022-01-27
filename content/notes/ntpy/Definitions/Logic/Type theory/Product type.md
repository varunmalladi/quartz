---
title: "Product type"
---

# Idea
In set theory, given two small sets $A$ and $B$ we define their Cartesian product $A\times B$ to be the set of elements of the form $(a,b)$ where $a\in A$ and $b\in B$. You could say this is precisely the defining property of the Cartesian product of sets. From this we can derive what functions of the form $f:A\times B\to C$ look like. For example, we can deduce that because elements of $A\times B$ are by definition those of the form $(a,b)$, to define $f$ it suffices to define $f$ on pairs $(a,b)$.

In type theory, we do the opposite, that is declare that to define $f$ it suffices to define $f$ on pairs $(a,b)$, and then we can deduce that every element in $A\times B$ is equal to a pair $(a,b)$. Let's break that down in more detail.

Type theory takes a different approach. In sort of a Haskellian view of functions as "first-class citizens", it says that what really matters about the Cartesian product is how functions (out of it) are defined. Why should that matter as opposed to how elements are defined? Well the Cartesian product serves a very special purpose. It is the *left adjoint* of exponentiation, by which we mean the creation of functions.

What does this mean, specifically? Recall that while we could have defined functions of multiple variables, this wasn't necessary. By [currying](<notes/ntpy/Definitions/Logic/Type theory/Currying.md>), a function that takes inputs from $A$ and $B$ to yield an element in $C$ can be thought of as a function $A\to (B\to C)$.

Did you catch that? We just said something that isn't well defined. We implied that "a function that takes inputs from $A$ and $B$ to yield an element in $C$" was a well-defined statement, but it isn't yet. The curried function $A\to B\to C$ by definition takes an input from $A$ and yields an element/function in $(B\to C)$; it doesn't take one element from $A$ and one element from $B$ and return an element in $C$.

The Cartesian product type serves to make the statement "a function that takes inputs from $A$ and $B$ to yield an element in $C$" well-defined. Indeed, this statement pretty much tells us how to define the Cartesian product. Given elements $a:A$ and $b:B$ define an element $(a,b):A\times B$. Now keeping in mind that we want functions $A\times B\to C$ to be equivalent to their curried counterpart $A\to B\to C$, we say that given $g:A\to B\to C$, define $f:A\times B\to C$ by $f((a,b))=g(a)(b)$. 

We just said something that again has a subtle implication. We implied that to define $f:A\times B\to C$, it sufficed to define its value on pairs $(a,b)$. To be clear, this is an actual constraint we are imposing in our definition; it is not a derivable fact. Indeed, if we did not make this constraint, there is no reason to believe that it suffices to define $f$ only on pairs $(a,b)$, for we did not declare (unlike in Set Theory!) that every element in $A\times B$ was of the form $(a,b)$. 

So just to recap, while in Set Theory we defined the Cartesian product as the set of elements of the form $(a,b)$, in type theory we are defining functions, in particular that to define a function $A\times B\to C$ it suffices to define it on pairs $(a,b):A\times B$. This statement is the _recursion principle for products_ in type theory.

From this recursion principle we can prove the _uniqueness principle_, which is subtle in its own right. This is the proposition (emphasis on proposition) that every element in $A\times B$ is _equal_ to a pair $(a,b)$. Why is this so subtle? Well this is due to how the identity type is defined in type theory. So lets say that we are asserting $x:A\times B$ is equal to the pair $(a,b)$. In type theory this means that the type $x=_{A\times B}(a,b)$ is inhabited, meaning there is an element $p:x=_{A\times B}(a,b)$.

At this point, it is actually beneficial to think of homotopy type theory. In homotopy type theory types are spaces up to homotopy, and elements of a type are points on that space. Equality is the type whose elements are paths on that space. All of this is to set up what I think is a really intuitive idea: two elements of a type are equal when there is a path connecting them. Now it is immediate to see the subtlety I was alluding to before. Just because $x$ and $(a,b)$ are equal, it doesn't mean they are the same element, just that there exists a path connecting them!

And yes, when we are taking about sets the type theoretic and set theoretic definitions are equivalent. Spelled out, if we were to regard a set as a space then it is a totally disconnected one: the only paths are the constant ones from an element to itself, so equality in the sense of type theory collapses to the idea that two elements are equal if and only if they are definitionally the same.

The advantage of the type theoretic definition is that it generalizes the set theoretic one. I've been studying homotopy theory on my own for a bit now, and had always heard that we only care about things "up to homotopy". Even in general we rarely care about things up to strict equality, it is far more useful to consider things that are equal "up to something", whether that be isomorphism, homeomorphism, or homotopy. For some reason it was only through unpacking the product type that I understood how ideas from homotopy theory played into logic. As we just saw, we have the ability to specify how strong a notion of equality we want to work with.

Here is the familiar adjunction we were working hard to define: $$\text{hom}(A\times B,C)=\text{hom}(A,\text{hom}(B,C)).$$ The above discussion could essentially be described as saying, the definition of the product type is defined in such a way as to be the left adjoint to exponentiation.

# Definition
Given types $A$ and $B$, we define the type $A\times B$:
- *Formation*: $A$ is a type and $B$ is a type
- *Construction*: given $a:A$ and $b:B$ we may form $(a,b):A\times B$.
- *Eliminator*: for any $g:A\to B\to C$, define $f:A\times B\to C$ by $$f((a,b)):\equiv g(a)(b).$$ In other words the recursor for product types is \begin{gather}\text{rec}_{A\times B}:\prod_{C\in\mathcal{U}}(A\to B\to C)\to (A\times B\to C) \\ \text{rec}_{A\times B}(C,g,(a,b)):\equiv g(a)(b).\end{gather}