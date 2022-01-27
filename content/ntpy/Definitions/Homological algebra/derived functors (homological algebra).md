---
title: "derived functors (homological algebra)"
---

---
title: "derived functors (homological algebra)"
---

# Idea
Let us consider $A$-modules. Consider a functor $F$. Then given maps $M_1\to N$ and $M_1\hookrightarrow M_2$, if an extension $M_2\to N$ exists then the extension $F(M_2)\to F(N)$ also exists. However, it can be the case that the extension only exists after passing to $F$ and does not exist before.

[model categories and derived functors](notes/ntpy/Key Ideas/Homotopy theory/model categories and derived functors.md)<notes/ntpy/Key Ideas/Homotopy theory/model categories and derived functors.md>)

Consider an exact sequence $$0\to M'\to M\to M''\to 0.$$ Applying a functor $F$ will result in one of three outcomes:
1. The sequence is exact
2. The sequence is left or right exact, but not fully exact
3. The sequence is neither left nor right exact

Derived functors deal with the second case. Let us, for example, deal with the case where the resulting sequence is right exact, i.e. $$F(M')\to F(M)\to F(M'')\to 0$$ is exact. The idea is that there ought to be a canonical long exact sequence for which this is the end of. Derived functors give us such a construction: in this case, since we are completing to the left, we would take the left derived functor $L^\bullet F$ to obtain a long exact sequence $$\cdots\to L_1F(M')\to L_1F(M)\to L_1F(M'')\to FM'\to FM\to FM''\to 0.$$ Now, if the left derived functors were 0 for $n\geq 1$, then we would just have a short exact sequence, which would mean that actually $F$ was fully exact. So in this sense the left derived functor is measuring the failure of $F$ to be exact.

Lurking here is the idea that a [ses of chain complexes induces les of homology]()<>). What we are doing is creating a long exact sequence over $FM'$, $FM$, and $FM''$ respectively, 
