---
title: "Dependent function types"
---

# Idea
Given a type $A:\mathcal{U}$, there is a notion of a [family](<notes/ntpy/Definitions/Logic/Type theory/Families of types.md>) $B:A\to \mathcal{U}$ which sends elements in $A$ to types. It is natural to want to extend this function to yield actual elements inside those types, as opposed to the types themselves. A dependent type is the type of such function, i.e. it is the type of functions which send elements $x:A$ to elements $f(x):B(x)$ in some type possibly dependent on $A$.

# Definition
We write the dependent type as $$\prod_{(x:A)}B(x).$$ An element $f:\prod_{(x:A)}B(x)$ is defined as $f(x):\equiv\Phi$, where $\Phi:B(x)$ is an expression possibly involving $x$.

# Polymorphic functions
A type itself is an element of a universe. Hence a dependent type can vary over types in a universe. Functions in this type take a type and acts on its elements. Consider the following examples:

1. The polymorphic identity function \begin{gather} \text{id}:\prod_{(A:\mathcal{U})}A\to A \\ \lambda(A:\mathcal{U}).\lambda(x:A).x\end{gather} which reads: given a type $A$, this function yields a function $A\to A$ which sends every $x:A$ to itself.
2. The "swap" function \begin{gather}\text{swap}:\prod_{A,B,C:\mathcal{U}}(A\to B\to C)\to (B\to A\to C) \\ \lambda b.\lambda a. g(a)(b)\end{gather} Evidently, this is changing the order of [currying](<notes/ntpy/Definitions/Logic/Type theory/Currying.md>).