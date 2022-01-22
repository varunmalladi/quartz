---
title: "Currying"
---

# Idea
When defining functions of multiple variables, we could use the cartesian product. Alternatively, we can define them without product types by using currying.

In particular, a function $f:A\times B\to C$ can be thought of as a function $f:A\to (B\to C)$.

Letting $f(x,y):\equiv \Phi$, we can write this in [Lambda abstraction](<notes/ntpy/Definitions/Logic/Type theory/Lambda abstraction.md>) as $f:\equiv\lambda x.\lambda y.\Phi$, or even $f:\equiv x\mapsto y\mapsto \Phi$. Implicitly, $g(-,-)$ means $\lambda x.\lambda y.g(x,y)$.
