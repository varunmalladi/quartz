# Definition
We specify the following:
1. *Formation rule*: given a type $A:\mathcal{U}$ and two elements $a,b: A$ we can form the type $(a=_A b):\mathcal{U}$.
2. *Construction*: we definition a dependent function called reflixivity: $$\text{refl}:\prod_{a: A}(a=_Aa)$$ which asserts that every element of $A$ is equal to itself, specifically in the way specified as a constant path at that point. In particular, if $a$ and $b$ are judgementally equal then there is an element $\text{refl}_a:a=_A b$.