---
title: Algebra(Artin) Chapter 4
keywords: solution, artin, algebra, chapter,
last_updated: 
summary: ""
sidebar: mydoc_sidebar
permalink: algebra_chap4.html
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


## Section 1 The Dimension Formula
**Q1.4**

> Prove that every $m \times n$ matrix $A$ of rank 1 has the form $A=X Y^{\mathrm{t}}$, where $X, Y$ are $m$ - and $n$-dimensional column vectors. How uniquely determined are these vectors?

We have:

$$
A=X Y^{t}=\left[\begin{array}{c}
\mid \\
X \\
\mid
\end{array}\right]\left[\begin{array}{lll}
y_{1} \cdots & y_{n}
\end{array}\right]=\left[\begin{array}{cccc}
\mid & \mid & & \mid \\
y_{1} X & y_{2} X & \cdots & y_{n} X \\
\mid & \mid & & \mid
\end{array}\right]
$$

The column space formed by $X Y^t$ always has dimension 1, because all columns are scalar multiples of $X,$ therefore dependent on $X$ and $A$ has rank 1. Vice versa.

These vectors are uniquely determined up to scalar multiplication. 

For example, if we have $X, Y$ such that $A=X Y^t$, 

then if we let $X^{\prime}=c X, Y^{\prime}=\frac{1}{c} Y$ 

$\Rightarrow A=X^{\prime} {Y^{\prime}}^t=c X \cdot \frac{1}{c} Y^{t}=X Y^{t}$, 

still holds for $X^{\prime}$ and $Y^{\prime}.$

## Section 2 The Matrix of a Linear Transformation
**Q2.1**

> Let $A$ and $B$ be $2 \times 2$ matrices. Determine the matrix of the operator $T: M \leadsto A M B$ on the space $F^{2 \times 2}$ of $2 \times 2$ matrices, with respect to the basis $\left(e_{11}, e_{12}, e_{21}, e_{22}\right)$ of $F^{2 \times 2}$.

Let 

$$A=\left(\begin{array}{ll}a_{11} & a_{12} \\ a_{21} & a_{22}\end{array}\right), B=\left(\begin{array}{ll}b_{11} & b_{12} \\ b_{21} & b_{22}\end{array}\right)$$

By direct calculation, 

$$T\left(e_{11}\right)=A e_{11} B=\left(\begin{array}{ll}a_{11} b_{11} & a_{11} b_{12} \\ a_{21} b_{11} & a_{21} b_{12}\end{array}\right)$$

$$T\left(e_{12}\right)=\left(\begin{array}{ll}a_{11} b_{21} & a_{11} b_{22} \\ a_{21} b_{21} & a_{21} b_{22}\end{array}\right), T\left(e_{21}\right)=\left(\begin{array}{ll}a_{12} b_{11} & a_{12} b_{12} \\ a_{22} b_{11} & a_{22} b_{12}\end{array}\right)$$

$$T\left(e_{22}\right)=\left(\begin{array}{ll}a_{12} b_{21} & a_{12} b_{22} \\ a_{22} b_{21} & a_{22} b_{22}\end{array}\right)$$

So $$T\left(e_{11}\right)=\left(e_{11}, e_{12}, e_{21}, e_{22}\right)\left(\begin{array}{l}a_{11} b_{11} \\ a_{11} b_{12} \\ a_{21} b_{11} \\ a_{21} b_{12}\end{array}\right)=C A_{1}$$
Where $C$ is the basis. $A_{1}$ is the first column of the matrix of the operator.

Similarly for $T\left(e_{12}\right),T\left(e_{21}\right),T\left(e_{22}\right)$. so the mathix of operator, $A$, is obtained by assembling $A_1,A_2,A_3,A_4$ into the columns of $A$:

$$A=\left(\begin{array}{llll}a_{11} b_{11} & a_{11} b_{21} & a_{12} b_{11} & a_{12} b_{21} \\ a_{11} b_{12} & a_{11} b_{22} & a_{12} b_{12} & a_{12} b_{22} \\ a_{21} b_{11} & a_{21} b_{21} & a_{22} b_{11} & a_{22} b_{21} \\ a_{21} b_{12} & a_{21} b_{22} & a_{22} b_{12} & a_{22} b_{22}\end{array}\right)$$

