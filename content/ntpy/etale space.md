# Definition
Let $B\in\text{Top}$, and $x\in B$.
- An *etale space* over $B$ is an object $E\in\text{Top}$ equipped with a map $$p:E\to B$$ such that $p$ is a local homeomorphism.
	- $E$ may be called the *total space*.
	- $p$ may be called the *projection*.
- $E_x=p^{-1}(x)$ is called the *stalk* of $p$ over $x$.

# Relation to sheaves
Consider an arbitrary map $p:E\to B$. Recall (from [[sheaf]]) the sheaf of sections of $p$, denoted $$\Gamma_p(E/B).$$
1. If $p$ is etale, then the images of local sections form a base for the topology of the total space $E$.
2. If $p$ is etale, then the sheaf of sections