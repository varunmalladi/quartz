---
title: "Grothendieck coverage"
---

# Idea
An abstraction of the manner in which open sets cover a topological space.

A category with a Grothendieck coverage is a [site](<notes/ntpy/site.md>).

# Definition
Let $C$ be a category.
1. A *Grothendieck coverage* of $C$ assigns to each $c\in\text{Obj}(C)$ a collection of "covering" [sieve](<notes/ntpy/Definitions/Category theory/sieve.md>)s $J(c)$ such that 
	1. (stability under base change) if $F\in J(c)$ and $g:d\to c$, then $$g^\ast F\in J(d).$$
	2. (local character condition) let $S\in J(c)$ and $T$ any sieve on $c$. If for every $d\in\text{Obj}(C)$ and  $g:d\to c\in S$ we have that $g^\ast T\in J(d)$, then $T\in J(c)$.
	3. (maximial sieve is a covering sieve) $\text{Obj}(C/c)\in J(c)$

**Remarks on Definition 1**
- Stability under base change
	- Let $C=\text{Op}(X)$, the category of open sets of a topological space $X$ under inclusion. This condition tells us that if $\{U_i\}$ covers $U$ and $g:V\hookrightarrow U$, it must be the case that $g^\ast \{U_i\}=\{U_i\cap V\}$ covers $V$.
- Local character condition
	- This is a sort of converse for the first statement, saying that if the pullback along every arrow in a covering sieve is also a  covering sieve, then it itself is a covering sieve.
	- Going with our example above, let $\{U_i\}$ be a covering sieve for $U$. Every arrow in this sieve is of the form $g:U_i\to U$. Now suppose we had a set $\{V_{ij}\}$ such that $g^\ast \{V_{ij}\}$ is a covering sieve, i.e. $\{V_{ij}\}$ covers each $U_i$.Then it should (and is) the case that the $\{V_{ij}\}$ cover $U$.
	- So another way of seeing this is that if a sieve covers each local component of a covering sieve, then we ought to be able to piece it all together to conclude that it is globally a  covering sieve.
- Maximal sieve is a covering sieve
	- Going with our example above, this tells us that a space ought to be covered by the collection of all its (open?) subsets
