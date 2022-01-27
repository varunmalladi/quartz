---
title: "Tate field"
---

# Definition

The function $v_p$ extends in a unique way from $\mathbb{Q}_p^\ast$ to $\overline{\mathbb{Q}_p^\ast}$ with the formula $$v_p(x)\coloneqq\frac{1}{\text{deg }x}v_p(N_{\mathbb{Q}_p(x)/\mathbb{Q}_p}(x))$$ with values in $\mathbb{Q}$ and defined (after choice of $1<s\in\mathbb{R})$ a nonarchimedean [absolute value](<notes/ntpy/Definitions/Ring theory/Absolute value.md>) $\|x\|\coloneqq s^{-v_p(x)}$ on the field $\overline{\mathbb{Q}_p}$.

The Tate field $\mathbb{C}_p$ is the completion of the field $\overline{\mathbb{Q}_p}$ with respect to the absolute value defined above.

# Properties

1. The field $\mathbb{C}_p$ contains some elements which are transcendental over $\mathbb{Q}_p$.
3. $\mathbb{C}_p$ is algebraically closed.
4. For a power series $$F(T)=\sum_{i=0}^\infty a_iT^i\in\mathbb{C}_p[[T]],$$ define $$v_p(F)\coloneqq\lim\inf\frac{v_p(a_i)}{i}.$$ (v_p(F) may be finite or $\pm\infty$.) Then $F(x)$ converges if $v_p(x)>-v_p(F)$ and defines a continuous function. If $v_p(x)< -v_p(F)$ then $F(x)$ does not conerge.