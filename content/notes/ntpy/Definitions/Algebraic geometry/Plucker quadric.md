---
title: "Plucker quadric"
---

# Idea

(include from [Grassmanian](notes/ntpy/Definitions/Algebraic geometry/Grassmanian.md))

A *net* in $Q$ is a linear embedding $\mathbb{P}^2\subset\mathbb{P}^5$ such that $$\mathbb{P}^2\subset Q\subset\mathbb{P}^5.$$

Let $\pi$ be a net. Consider three non-colinear points $p_1,p_2,p_3\in\pi$.

**Lemma.** If $p\in \mathbb{P}^k\subset Q\subset\mathbb{P}^N$, then $\mathbb{P}^k\subset T_p Q$.

It follows that $$\pi\subset T_{p_1}Q\cap T_{p_2}Q\cap T_{p_3}Q\cap Q.$$ Recall that $T_{p_i}Q\cap Q=\{l\subset\mathbb{P}^3\mid l\cap l_{p_i}\neq\emptyset\}$, where $l$ is a projective line. So $$l_{p_1}\cap l_{p_2}\neq \emptyset,\quad l_{p_2}\cap l_{p_3}\neq \emptyset,\quad l_{p_1}\cap l_{p_3}\neq\emptyset.$$ These three lines could have three points of intersection with no common intersections (a $\beta$-net), or one point of common intersection (an $\alpha$-net).

# Affine cell decomposition 
We discuss the affine cell decomposition for $Q=Gr(2,4)$.

We can decompose projective space in the following way: $$\mathbb{P}^n=\mathbb{A}^n\cup\mathbb{A}^{n-1}\cup\dots\cup\mathbb{A}^1\cup\mathbb{A}^0$$
This decomposition has geometric meaning.

Consider a point $p\in Q=Gr(2,4)$, and fix a projective subspace $H\subset T_pQ$ of codimension 1 (i.e. dimension 3) such that $p\not\in H$. Let $C= Q\cap T_pQ$. This is a quadric in $\mathbb{P}^4$, but is not smooth (in the sense that it has full rank). It has corank 1. So actually $C$ is a cone over $\mathbb{P}^1\times\mathbb{P}^1$. Now let $G=Q\cap H$. This is a smooth quadric. We may identify $G=\mathbb{P}^1\times\mathbb{P}^1$, so that $C$ is a cone over $G$.
