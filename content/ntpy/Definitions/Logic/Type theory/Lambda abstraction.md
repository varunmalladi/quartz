---
title: "Lambda abstraction"
---

# Idea
We don't always need to define a function by name.

# Definition
Suppose we are defining functions from type $A$ to type $B$.

If we wanted to express $f(x)\coloneqq \Phi$ with $\lambda$-abstraction, we could write 
$$
\begin{gather}
(\lambda(x:A).\Phi):A\to B, \\
\lambda x.\Phi:A\to B, \\
(x\mapsto \Phi):A\to B.
\end{gather}
$$

We can also define it implicitly. For instance, $g(x,-)$ is another way to write $\lambda y.g(x,y)$.

# Properties
1. Given a function $f$, the lambda abstraction $\lambda x.f(x)$ is definitionally eqal to $f$, i.e. $$ f\equiv (\lambda x.f(x)).$$ While apparant, this implies that $f$ is uniquely determined by its values. This is the *uniqueness principle for function types*.