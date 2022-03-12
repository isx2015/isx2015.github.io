---
title: Vector Spaces
keywords: vector, spaces, space,
last_updated: 
summary: ""
sidebar: mydoc_sidebar
permalink: vec-space.html
folder: sites
---

## Definitions

**Def. 1**

A **field** $F$ is a set together  with two laws of composition:

addition: $F \times F \stackrel{+}{\rightarrow} F \quad (a, b \rightarrow a b)$

multiplication: $F \times F \stackrel{\times}{\rightarrow} F \quad (a, b \rightarrow a+b)$ 

that satisfy 3 axioms:

1. Addition makes $F$ into an abelian group $F^{+}$ with identity element 0.
2. Multiplication is commutative, and it makes the set of nonzero elements of $F$ into an abelian group $F^{\times}$ with identity element 1.
3. distributive law: For all $a, b$, and $c$ in $F, a(b+c)=a b+a c$.

> Notice, the axiom 1,2 describe the properties of $\times$ and $+$. Axiom 3 relates axioms 1,2.

**Def. 2**

A **subfield** of the field $\mathbb{C}$ (complex numbers) is a subset that is ==closed== under four operations $+, -, \times, \div$ and contains $1$.

i.e. $F$ is a subfield of $\mathbb{C}$ if it has following properties:

$$
\begin{array}{ll}
 (+)\quad a,b \in F &\Rightarrow a+b \in F\\
 (-)\quad a \in F &\Rightarrow -a \in F\\
 (\times)\quad a,b \in F &\Rightarrow ab \in F\\
 (\div)\quad a \in F(a\neq 0) &\Rightarrow a^{-1} \in F\\
(1)\quad 1\in F
\end{array}
$$

> The above implies
> 1. $0\in F$
> 2. $F$ is a subgroup of additive group $\mathbb{C^+}$
> 3. $F \backslash\{0\}$ is a subgroup of the multiplicative group $\mathbb{C^\times}$

