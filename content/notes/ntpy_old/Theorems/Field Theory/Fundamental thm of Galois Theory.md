---
title: "Fundamental thm of Galois Theory"
---

# Finite case
Suppose $K/k$ is a finite [Galois extension](ntpy/Definitions/Algebraic Number Theory/Field Theory/Galois extension.md). Let $G$ be its Galois group. Then 
1. There exists a one-to-one correspondence $$\begin{gather} \{\text{subgroups } H\subset G\} \ \leftrightarrow \ \{\text{subfields } k\subset M\subset K\} \\ H\mapsto K^H \\ \text{Gal}(K/M)\leftarrow M \end{gather}$$
2. $M/k$ is [normal](ntpy/Definitions/Algebraic Number Theory/Field Theory/Normal extensions.md) iff $H\triangleleft G$ (normal subgroup)

# Infinite case
Let $K/F$ be Galois, $G$ its Galois group equipped with the [Krull topology](ntpy/Definitions/Algebraic Number Theory/Field Theory/Krull topology.md).

1. There is an inclusion-reversing bijection $$\begin{gather}\{\text{subextensions }K/L/F\}\leftrightarrow\{\text{closed subgroups }H\subset G\} \\ L\mapsto \text{Gal}(K/L) \\ K^H \leftarrow H \end{gather}$$.
2. $L/F$ is Galois iff $\text{Gal}(K/L)\subset G$ is normal and open.
	1. $\text{Gal}(L/F)\cong G/\text{Gal}(K/L)$
