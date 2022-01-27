---
title: "ring of integers"
---

# Operations
1. ([norm](<>)) Suppose $I$ is an $\mathcal{O}_K$-[fractional ideal](<notes/ntpy/Definitions/Algebraic Number Theory/fractional ideal.md>) in $K$. Then its norm is $$N_{K/k}(I)\coloneqq(\mathcal{O}_K:I)_\mathcal{O}$$

# Properties
1. $N_{K/k}:\mathcal{F}(\mathcal{O}_K)\to\mathcal{F}(\mathcal{O})$ is a group homomorphism. (see [dedekind domain](<notes/ntpy/Definitions/Algebraic Number Theory/dedekind domain.md>)]])
2. Suppose $P_x$ is Eisenstein wrt $p$. Then $p\nmid (\mathcal{O}_K:\mathbb{Z}[x])$.
3. Let the bar symbol denote elements of $\mathcal{O}_K$ modulo $\mathfrak{B}$.
4. (reduction of homomorphisms)
	1. Suppose $K/k$ and $K'/k$ are finite separable [extensions](<notes/ntpy/Definitions/Algebraic Number Theory/Field Theory/Field extension.md>), $\sigma:K/k\to K'/k$ a homomorphism. Then the map $\sigma_\mathfrak{p}:\mathcal{O}_K/\mathfrak{B}\to\mathcal{O}_K'/\mathfrak{B}'$ defined as $\sigma_\mathfrak{p}(x\mod\mathfrak{B})\coloneqq\sigma(x)\mod\mathfrak{B}'$ is a correctly defined homomorphism of extensions $K_\mathfrak{B}/k_\mathfrak{p}\to K'_{\mathfrak{B}'}/k_\mathfrak{p}$.
	2. Reduction commutes with composition of homomorphisms, so reduction of an isomorphism is an isomorphism.

# Related
- [integral extensions](<notes/ntpy/Definitions/Ring theory/integral extensions.md>)