---
title: "Euler totient function"
---

## Totient function
Let $a$ and $n$ be positive integers. Then the **Euler totient function** $\phi(n)$ is defined as
$$
\phi(n)\coloneqq \# \{a\leq n: \text{gcd}(a,n)=1\},
$$
or the number of integers $\leq n$ that are relatively prime to $n$.

## Totient Number
A **totient number** is a positive integer $m$ that is in the image of the [[Euler totient function]], i.e. there exists $n$ such that there $\phi(n)=m$.

A **nontotient** is a positive integer that is not a totient number.

A totient number has **multiplicity** $k$ if there are exactly $\phi(n)=m$ has exactly $k$ solutions.

# References
1. https://en.wikipedia.org/wiki/Euler%27s_totient_function#Totient_numbers