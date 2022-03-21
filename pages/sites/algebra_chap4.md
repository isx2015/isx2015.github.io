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

Let $$A=\left(\begin{array}{ll}a_{11} & a_{12} \\ a_{21} & a_{22}\end{array}\right), B=\left(\begin{array}{ll}b_{11} & b_{12} \\ b_{21} & b_{22}\end{array}\right)$$

By direct calculation, 

$$T\left(e_{11}\right)=A e_{11} B=\left(\begin{array}{ll}a_{11} b_{11} & a_{11} b_{12} \\ a_{21} b_{11} & a_{21} b_{12}\end{array}\right)$$

$$T\left(e_{12}\right)=\left(\begin{array}{ll}a_{11} b_{21} & a_{11} b_{22} \\ a_{21} b_{21} & a_{21} b_{22}\end{array}\right), T\left(e_{21}\right)=\left(\begin{array}{ll}a_{12} b_{11} & a_{12} b_{12} \\ a_{22} b_{11} & a_{22} b_{12}\end{array}\right)$$

$$T\left(e_{22}\right)=\left(\begin{array}{ll}a_{12} b_{21} & a_{12} b_{22} \\ a_{22} b_{21} & a_{22} b_{22}\end{array}\right)$$

So $$T\left(e_{11}\right)=\left(e_{11}, e_{12}, e_{21}, e_{22}\right)\left(\begin{array}{l}a_{11} b_{11} \\ a_{11} b_{12} \\ a_{21} b_{11} \\ a_{21} b_{12}\end{array}\right)=\mathbf{C} A_{1}$$
Where $\mathbf{C}$ is the basis, $A_{1}$ is the first column of the matrix of the operator.

Similarly for $T\left(e_{12}\right),T\left(e_{21}\right),T\left(e_{22}\right)$. so the mathix of operator, $A$, is obtained by assembling $A_1,A_2,A_3,A_4$ into the columns of $A$ by the formula: $T(\mathbf{C})=\mathbf{C}A$

$$A=\left(\begin{array}{llll}a_{11} b_{11} & a_{11} b_{21} & a_{12} b_{11} & a_{12} b_{21} \\ a_{11} b_{12} & a_{11} b_{22} & a_{12} b_{12} & a_{12} b_{22} \\ a_{21} b_{11} & a_{21} b_{21} & a_{22} b_{11} & a_{22} b_{21} \\ a_{21} b_{12} & a_{21} b_{22} & a_{22} b_{12} & a_{22} b_{22}\end{array}\right)$$

**Q2.2**

> Let $A$ be an $n \times n$ matrix. and let $V$ denote the space of $n$-dimensional *row* vectors. What is the matrix of the linear operator "right multiplication by $A$ " with respect to the standard basis of $V$ ?

The standard basis is $\mathbf{E}=\left(e_{1}, \cdots, e_{n}\right)$, 

Let $A=\left(a_{i j}\right)$,

$T\left(e_{j}\right)=e_{j} A=A_{j}$, where $A_{j}$ stands for the j-th row of $A$.

$$
\Rightarrow T\left(e_{j}\right)=A_{j}=a_{j 1} e_{1}+\cdots+a_{j n} e_{n}=\left(e_{1}, \cdots, e_{n}\right)\left(
\begin{array}{c}
a_{j 1} \\
\vdots \\
a_{j n}
\end{array}\right)=\mathbf{E} M_{j}
$$

$M_{j}$ is the $j$ th column of $M$, the matrix of the linear operator.
Assemble all $M_{j}$ into columns, we have,

$$
M=\left(\begin{array}{ccccc}
a_{11} & \cdots & a_{j 1} & \cdots & a_{n 1} \\
\vdots & & \vdots & & \vdots \\
a_{1 n}& \cdots & a_{j n} & \cdots & a_{n n}
\end{array}\right)
$$

So $M=A^t$, the transpose of $A$ is the matrix of the linear operator "right multiplication by $A$".

**Q2.3**

> Find all real $2 \times 2$ matrices that carry the line $y=x$ to the line $y=3 x$.

Using the standard basis, any vector on $y=x$ is of the form $k(1,1)^{t}$, under a $2 \times 2$ matrix multiplication,

$$k\left(\begin{array}{ll}a & b \\ c & d\end{array}\right)\left(\begin{array}{l}1 \\ 1\end{array}\right)=k\left(\begin{array}{l}a+b \\ c+d\end{array}\right)$$

To ensure $k(a+b, c+d)^{t}$ is on $y=3x$, simply let $a+b=3(c+d)$. Any $2 \times 2$ real matrices satisfying this rule will work.

