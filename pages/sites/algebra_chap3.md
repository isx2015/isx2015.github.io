---
title: Algebra(Artin) Chapter 3
keywords: solution, artin, algebra, chapter,
last_updated: 
summary: ""
sidebar: mydoc_sidebar
permalink: algebra_chap3.html
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

## Section 3 Bases and Dimension
**Q3.1**

> Find a basis for the space of $n \times n$ symmetric matrices $\left(A^{t}=A\right)$.

A symmetric matrix is uniquely determined by its entries on and above the diagnal. 

One basis is $$\left\{e_{i j}+e_{j i}, \forall~ 1 \leqslant i \leqslant j \leqslant n\right\}$$

where $e_{i j}$ is in the usual sense, stands for a $n\times n$ matrix with 1 at $(i, j)$ position and zero elsewhere.

**Q3.3**

> Prove that the three functions $x^{2}, \cos x$, and $e^{x}$ are linearly independent.

This three functions are linearly independent if 

$\forall x \in \mathbb{R}, a x^{2}+b \cos x+c e^{x}=0~~(1)$

implies $a=b=c=0$.

$~$

Now if we take $x=0$ in Eq. (1),
then $b+c=0$

Differentiate Eq. (1),
$$
2 a x-b \sin x+c e^{x}=0
$$

plug in $x=0 \Rightarrow c=0$

so $b=0$ and $a=0$.

Q.E.D.

**Q3.4**

>Let $A$ be an $m \times n$ matrix, and let $A^{\prime}$ be the result of a sequence of elementary row operations on $A$. Prove that the rows of $A$ span the same space as the rows of $A^{\prime}$.

Let $S=\left(v_{1}, \cdots v_{m}\right)$ be ordered set of row vectors of A in $\mathbb{R^n}$.

We only need to check Span $S$ is unchanged under three types of elementary operation:
1. permutation between $v_{i}, v_{j}$ in $S$ doesn't change Span $S$.
2. scalar multiplication of $v_{i}$ to $c v_{i}$ doesn't change Span $S$.
3. add $a v_{j}(a \neq 0)$ to $v_{i}$, then $S$ becomes $S^{\prime}=\left(v_{1}, \cdots v_{i}+a v_{j}, \cdots v_{j},\cdots ,v_{m}\right)$

    So span $S^{\prime}=x_{1} v_{1}+\cdots+x_{i}\left(v_{i}+a v_{j}\right)+\cdots+x_{j} v_{j}+x_{m} v_{m}$

    $$
    \begin{array}{l}
    =x_{1} v_{1}+\cdots+x_{i} v_{i}+\cdots+\left(a x_{i}+x_{j}\right) x_{j}+\cdots+x_{m} v_{m} \\
    =\text { Span } S
    \end{array}
$$

Hence, row space is unchanged under elementary operations.

**Q3.5**

> Let $V=F^{n}$ be the space of column vectors. Prove that every subspace $W$ of $V$ is the space of solutions of some system of homogeneous linear equations $A X=0$.

**Q3.7**

> Let $\left(X_{1}, \ldots, X_{m}\right)$ and $\left(Y_{1}, \ldots, Y_{n}\right)$ be bases for $\mathbb{R}^{m}$ and $\mathbb{R}^{n}$, respectively. Do the $m n$ matrices $X_{i} Y_{j}^{\mathrm{t}}$ form a basis for the vector space $\mathbb{R}^{m \times n}$ of all $m \times n$ matrices?


**Q3.8**

> Prove that a set $\left(v_{1}, \ldots, v_{n}\right)$ of vectors in $F^{n}$ is a basis if and only if the matrix obtained by assembling the coordinate vectors of $v_{i}$ is invertible.

Suppose the matrix obtained is $A$.

If the set $\left(v_{1}, \cdots, v_{n}\right)$ is a basis, then it is independent by definition. So columns of $A$ are independent and $A$ is invertible.

If $A$ is invertible, then $\left(v_{1}, \ldots, v_{n}\right)$ is independent. Reduce $A$ to identity matrix $I$. The set $\left(e_{1}, \cdots, e_{n}\right)$ formed by $I$ is a standard basis and span $F^n$. So $\left(v_{1}, \ldots, v_{n}\right)$ must also span $F^{n}$ by $[Q 3.4]$.
Hence $\left(v_{1}, \ldots, v_{n}\right)$ is a basis for $F^{n}$.

Q.E.D.

