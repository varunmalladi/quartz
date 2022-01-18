---
title: "residue class degree, ramification index"
---

# Definition
Suppose $\mathcal{O}_1\subset\mathcal{O}_2$ are [[dedekind domain]]s, $\mathfrak{p}_1\subset\mathcal{O}_1$ and $\mathfrak{p}_2\subset\mathcal{O}_2$ are nonzero prime ideal such that $\mathfrak{p}_2$ [[Prime ideal|lies over]] $\mathfrak{p}_1$ (i.e. $\mathfrak{p}_1=\mathfrak{p}_2\cap\mathcal{O}_1$). 
- The residue class degree, or inertia index, is $$f(\mathfrak{p}_2/\mathfrak{p}_1)\coloneqq [k_{\mathfrak{p}_2}:k_{\mathfrak{p}_1}]$$ (notice nonzero prime ideals are maximal in Dedekind domains, so the above is the degree of the [[Field extension]]). We allow infinite values.
- The ramification index is the (necessarily finite) number $$e(\mathfrak{p}_2/\mathfrak{p}_1)\coloneqq v_{\mathfrak{p}_2}(\mathfrak{p}_1\mathcal{O}_2)$$

# Properties
1. Suppose $\mathcal{O}_1\subset\mathcal{O}_2\subset\mathcal{O}_3$ and $\mathfrak{p}_3\mid \mathfrak{p}_2\mid\mathfrak{p}_1$. Then
	1. $f(\mathfrak{p}_3/\mathfrak{p}_1)=f(\mathfrak{p}_3/\mathfrak{p}_2)f(\mathfrak{p}_2/\mathfrak{p}_1)$ so long as two out of the three are finite
	2. $e(\mathfrak{p}_3/\mathfrak{p}_1)=e(\mathfrak{p}_3/\mathfrak{p}_2)e(\mathfrak{p}_2/\mathfrak{p}_1)$ so long as two out of the three are finite
	3. If $\mathcal{O}_1=\mathcal{O}_\mathfrak{p}$ is a [[discrete valuation ring]], $\mathcal{O}_2=\widehat{\mathcal{O}}_\mathfrak{p}$ its completion. Then $$f(\mathfrak{p}\widehat{\mathcal{O}}_\mathfrak{p}/\mathfrak{p})=e(\mathfrak{p}\widehat{\mathcal{O}}_\mathfrak{p}/\mathfrak{p})=1.$$ (see [[associated p-adic algebra]])