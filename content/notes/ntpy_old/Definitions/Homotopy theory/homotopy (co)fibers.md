---
title: "homotopy (co)fibers"
---

# Idea
It is a rich complexity in homotopy theory that [(co)limits do not respect homotopy equivalence](ntpy/Key Ideas/Homotopy theory/(co)limits do not respect homotopy equivalence.md). Given a map $f:X\to Y$, we understand that fiber of $y\in Y$ is the set of $x\in X$ such that $f(x)=y$. The can be regarded as a limit, in particular the pullback
$$
\begin{array}
z\text{fib}(f) & \to & X \\ 
\downarrow & {}^{(\text{pb})} & \rlap{\ \ {}^f}{\downarrow} \\
\ast & \to & Y
\end{array}
$$
Perhaps this it is not surprising that this is not respected under homotopy equivalence: we are weakening our notion of "equality" on the spaces in the limit diagram but not weaking the notion of equality of the fiber $f(x)=y$. 

So if we want a version of $\text{fib}(f)$ that respects homotopy equivalence, we might ask instead that the fiber of $f$ over $y$ is the set of all $x$ such that $f(x)\cong y$ in the sense of, say, homotopy type theory; i.e. there exists a path from $f(x)\to y$. (As in homotopy type theory, the path itself carries information: there may be two witnesses (=paths) to the isomorphisms that belong to different homotopy classes.)

The path is indespensible, as the following example will illustrate. Let $X=\{y\}$, and let $f$ be the inclusion. What is the fiber of $f$ "up to isomorphism"? As a set, the fiber is only a single point: $\{y\}$. Certainly this is in the fiber as there is the trivial path connecting $y$ to itself. However, there may be other paths from $y$ to itself that are not homotopic to the trivial path, in which case we ought to regard those witnesses as distinct elements from the trivial one. So we can model elements in the _homotopy fiber_ as a pair $(x,p)$ where $x$ is a point and $p:f(x)\to y$ is a path. So the homotopy fiber of $f$ here is the set of $(y,p)$ where $p$ is a representative of a homotopy class of paths from $y$ to itself. This is precisely the data of a loop space, so in this case $\text{hofib}(f)=\Omega Y$ (at $y$).

# Definition
As stated above, the homotopy fiber of $f:X\to Y$ at $y\in Y$ is the set of $x\in X$ equipped with paths from $f(x)\to y$ modulo homotopy. Diagramatically:
$$
\begin{array}
z\text{hofib}(f) & \rightarrow & \ast \\
\downarrow & \Leftarrow & \downarrow \\
X & \underset{f}{\rightarrow} & Y
\end{array}
$$
(the homotopy is between the two compositions; unfortunately obsidian does not allow rotation of the symbols).

# Properties
1. 

# References
- https://www.quora.com/What-is-an-intuitive-explanation-of-a-homotopy-fiber
- 
