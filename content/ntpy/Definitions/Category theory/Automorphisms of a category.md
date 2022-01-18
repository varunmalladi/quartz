Consider two categories $C$ and $D$. Let $F:C\to D$ be a functor. 

**Proposition.** $F$ induces a group homomorphism between the automorphism groups of $C$ and $D$. 

_Proof._ It suffices to show that invertible morphisms are mapped to invertible morphisms. Just consider the pasting diagram which follows from the definition of a functor:
$$
\begin{array}
zC & \overset{F}{\rightarrow} & D \\
\llap{{}^\phi}{\downarrow} & & \rlap{\ \ {}^{F(\phi)}}{\downarrow} \\
C & \overset{F}{\rightarrow} & D \\
\llap{{}^{\phi^{-1}}}{\downarrow} & & \rlap{\ \ {}^{F(\phi^{-1})}}{\downarrow} \\
C & \overset{F}{\rightarrow} & D
\end{array}
$$