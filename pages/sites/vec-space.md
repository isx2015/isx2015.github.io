---
title: Vector Spaces
keywords: vector, spaces, space,
last_updated: 
summary: ""
sidebar: mydoc_sidebar
permalink: vec-space.html
folder: sites
---

<script>
MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']]
  },
  svg: {
    fontCache: 'global'
  }
};
</script>
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-svg.js">
</script>

## Definitions

**Def. 1**

A **field** $F$ is a set together  with two laws of composition:

- addition: $F \times F \stackrel{+}{\rightarrow} F \quad (a, b \rightarrow a b)$

- multiplication: $F \times F \stackrel{\times}{\rightarrow} F \quad (a, b \rightarrow a+b)$ 

that satisfies 3 axioms:

1. Addition makes $F$ into an abelian group $F^{+}$ with identity element 0.
2. Multiplication is commutative, and it makes the set of nonzero elements of $F$ into an abelian group $F^{\times}$ with identity element 1.
3. distributive law: For all $a, b$, and $c$ in $F, a(b+c)=a b+a c$.

> Notice, the axiom 1,2 describe the properties of $\times$ and $+$. Axiom 3 relates axioms 1,2.

**Def. 2**

A **subfield** of the field $\mathbb{C}$ (complex numbers) is a subset that is <mark>*closed*</mark> under four operations $+, -, \times, \div$ and contains $1$.

i.e. $F$ is a subfield of $\mathbb{C}$ if it has the following properties:

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
> 3. $F \backslash \{0\}$ is a subgroup of the multiplicative group $\mathbb{C^\times}$

**Def.3**

A **vector space** $V$ over a field $F$ is a set together with two laws of composition:
- *addition*: 
$V \times V \rightarrow V\quad (v, w \rightarrow v+w$ for $v,w \in V)$
- *scalar multiplication* by elements of the field: 
  
    $F \times V \rightarrow V\quad (c, v \rightarrow cv$ for $c \in F, v\in V)$

that satisfies 4 axioms:
1. Addition makes $V$ into a commutative group $V^+$ with identity element $0$.
2. $1v=v$ for all $v\in V$.
3. associative law: $(ab)v=a(bv)$, for all $a,b \in F$ and $v\in V$.
4. distributive laws: $(a+b)v=av+bv$ and $a(v+w)=av+aw$, for all $a,b \in F$ and $v,w \in V$.

**Def.4**

A subset $W$ of $\mathbb{R^n}$ is a **subspace** if
1. $w,w'\in W\Rightarrow w+w'\in W$.
2. $c\in \mathbb{R},w \in W \Rightarrow cw\in W.$
3. zero vector $\in W$

This is equivalent of saying:
1. $W$ is non-empty.
2. $c_1,c_2,...,c_n\in \mathbb{R}, w_1,w_2,...,w_n\in W$
   
   $\Rightarrow$ linear combination $c_1w_1+...+c_nw_n \in W$