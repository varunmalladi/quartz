# Definition
The Grassmanian $Gr(k,n)$ is, as a set, the collection of $k$-dimensional subspaces of the $n$-dimensional vector space $V$.
$$Gr(k,n)=Gr(k,V)=\{W\subset V\mid \text{dim }W=k\}$$

As we will see in the examples, in certain cases the Grassmanian can be endowed with the structure of projective space. We might ask in which cases we have the structure of a manifold. It turns out that we can always do this.

The Plucker embedding is the canonical injection $$\begin{gather}p:Gr(k,V)\hookrightarrow\mathbb{P}(\Lambda^kV)\\ W\mapsto [u_1\wedge\cdots u_k]\end{gather}.$$ One can show that the image of this map is an [[Algebraic subset|algebraic variety]].

# Examples
1. ([[Projective space]]) 
	1. $Gr(1,n)=\mathbb{P}^{n-1}$.
	2. $Gr(n-1,V)=Gr(1,V^\ast)=Gr(n-1,n)=\mathbb{P}^{n-1}$.
2. ($k=2$, $n=4$)	
	1. Consider $Gr(2,4)\subset\mathbb{P}(\bigwedge^2 V_4)=\mathbb{P}^5$
	2. The [[Plucker quadric]] $Q\subset\mathbb{P}^5$ is the smooth [[quadric]] defined as $$Q=\{\omega\in\Lambda^2V\mid \omega\wedge\omega=0\}$$
3. Generalizing the above, there is an embedding $$Gr(k,n)\hookrightarrow\mathbb{P}(\Lambda^k V_n)=\mathbb{P}^{{n\choose k}-1}.$$

# Properties
1. For $l_1,l_2\subset \mathbb{P}^3$. $$l_1\cap l_2\neq\emptyset\quad\iff\quad p(l_1)\wedge p(l_2)=0.$$