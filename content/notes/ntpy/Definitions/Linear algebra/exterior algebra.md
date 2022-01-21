---
title: "exterior algebra"
---

# Idea
This construction forms the [exterior powers](notes/ntpy/Definitions/Linear algebra/exterior powers.md) into a graded algebra.

# Definition
The exterior algebra is defined as
$$\Lambda^\bullet V=\bigoplus_{k\geq 0}\Lambda^k V$$
We may define the multiplicative operation as follows: $$(e_{i_1}\wedge\cdots\wedge e_{i_r})\wedge(e_{j_1}\wedge\cdots\wedge e_{j_s})=e_{i_1}\wedge\cdots\wedge e_{i_r}\wedge e_{j_1}\wedge\cdots\wedge e_{j_s}.$$

# Properties
1. $\text{dim }\bigwedge^\bullet V=2^n$
2. By skew commutative being commutative after an even number of transpositions, if $w_1\in\bigwedge^{2k}V$ and $w_2\in \bigwedge^{2l}V$ then $w_1\wedge w_2=w_2\wedge w_1$.
	1. $\bigwedge^{\bullet}V\supset\bigwedge^{2\bullet}V$.
