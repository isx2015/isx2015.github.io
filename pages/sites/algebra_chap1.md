---
title: Solutions to Artin's Algebra Chapter 1
keywords: solution, artin, algebra, chapter,
last_updated: 
summary: ""
sidebar: mydoc_sidebar
permalink: algebra_chap1.html
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


### **Q1.11**
Suppose $A, B$ are triangular $n \times n$ matrices. Let $C=A B$.

$$
\begin{array}{l}
A=\left(a_{i j}\right), B=\left(b_{i j}\right), c=\left(c_{i j}\right) \\
\text { hence } a_{i j}=b_{i j}=0 \quad \forall{i}>j \\
\\
c_{i j}=\sum_{\nu} a_{i \nu} b_{\nu j} \quad(1 \leqslant \nu \leqslant n)
\end{array}
$$

Let $i> j$, 
when $1 \leqslant \nu < i, a_{i \nu}=0 \Rightarrow \sum_{1 \leqslant \nu < i}=0$.

$$
\begin{array}{l}
\quad j<i<\nu \leqslant n, \quad b_{\nu j}=0 \Rightarrow \sum_{i \leqslant \nu \leqslant n}=0 \\
\Rightarrow \sum_{\nu}=0 \\
\therefore \quad c_{i j}=0, \forall i>j
\end{array}
$$

<img src="images/q1.11.png" width="100" height="50">

transpose $C=AB$ gives similar result for lower triangular matrices.
### **Q1.13**
$$
(I+A)\left[I-A+A^{2}-\ldots+(-1)^{k} A^{k-1}\right]=I+(-1)^{k-1} A^{k}=I
$$

Inverse is 

$$I-A+A^{2}-\ldots+(-1)^{k} A^{k-1}$$

$$
\begin{array}{l}
\text{note that } A^k=0 \Rightarrow A \text{ is not invertible}\\
\text{because }0=det(A^k)=det(A)^k \Rightarrow detA=0
\end{array}
$$

### **Q1.15**
Using identities 1.1.23/25:

$$
e_{i j} e_{j \ell}=e_{i \ell} \text { and } e_{i j} e_{k \ell}=0 \text { if } j \neq k
$$

$$
e_{i j} e_{j}=e_{i} \text{ and } e_{i j} e_{k}=0 \text { if } j \neq k
$$

Express A in terms of matrix units: $A=\sum_{m, n} a_{m n} e_{m n}$

Then $e_{i j} A e_{k l}=\sum_{m, n} a_{m n} e_{i j} e_{m n} e_{k l}=\sum_{m=j, n} a_{m n} e_{i n} e_{k l}$
$=\sum_{m=j \atop n=k} a_{m n} e_{i l}=a_{j k} e_{i l}$

### **Q2.9**
**(a)**

Suppose there're two solutions $X_1,X_2$, then

$$
\begin{array}{l}
A X_{1}=B \\
A X_{2}=B \\
\\

\Rightarrow m A X_{1}=m B \\
\Rightarrow n A X_{2}=n B \\
\\
\Rightarrow A\left(m X_{1}+n X_{2}\right)=(m+n) B\\
\\
\Rightarrow A\frac{m X_{1}+n X_{2}}{m+n}=B
\end{array}
$$

$$
\begin{array}{l}
\text{Since } m,n \text{  can be any number,}\\
\text{there are infinitely many solutions}:
\frac{mX_1+nX_2}{m+n}
\end{array}
$$

Similarly, 
If $X_1,X_2,…,X_n (n\geq2）$ are solutions to $AX=B$,
Then all linear combinations of $X_k$: 

$$
\alpha_{1} X_{1}+\alpha_{2} X_{2}+\cdots+\alpha_{k} X_{k} \text{ such that }\sum \alpha_{k}=1
$$

are the solutions.


**(b)** suppose $A X=B$, where $X=Y+i Z, Y, Z$ are real matrices

$$
\begin{array}{l}
\quad A(Y+i Z)=B \\
\Rightarrow A Y+i A Z=B \\
\because A, B \text { are real, } \\
\therefore A Z=0 \\
\therefore A Y=B \\
\text { The real solution is } Y \text {. }
\end{array}
$$

### **Q2.10**

Reduce $A, B$ to row echelon matrices $A', B'$.

Since $A$ is square, $A'$ is either $I$ or its bottom row is zero (by Lemma 1.2.15).

If $A'$ bottom row is zero, to make sure the system have a solution, bottom entry of $B'$ must also be zero.

Now let $A'$ be of dimension n, then $X$ is also n-dimensional. With last row of $A'$ to be zero, there are $n-1$ equations and $n$ unknown variables. The solution cannot be unique. Hence $A'$ is identity.

So $A$ is invertible(Theorem 1.2.16), and the unique solution to the system is $X=A^{-1}B$ for every column vector $B$.

### **Q3.3**

Let elementary row and column matrices be $E_R$ and $E_C$,

by associative law, $(E_R A)E_C=E_R (A E_C)$, so the effects are the same if switching the order.

### **Q4.3**
By using recursive formula of determinant on the first row of this matrix $A_{n} \Rightarrow \operatorname{det} A_{n}=2 \operatorname{det} A_{n-1}-\operatorname{det} A_{n-2}$

The first three matrices are:

$$ A_{1}=(2),
A_{2}=\left(
    \begin{array}{cc}2 & -1 \\
    -1 & 2\end{array}\right),
A_{3}=\left(
    \begin{array}{ccc}2 & -1 & \\
     -1 & 2 & -1 \\
      & -1 & 2\end{array}\right)
$$

So
$\operatorname{det} A_{1}=2, \operatorname{det} A_{2}=3, \operatorname{det} A_{3}=4$.

Guess det $A_{n}=n+1$, for $n=1$, it works.

suppose det $A_{k}=k+1 \quad(k>1)$
Then by the recursive formula,
$\operatorname{det} A_{k+1}=2 \operatorname{det} A_{k} -\operatorname{det} A_{k-1}=2(k+1)-k=k+2$

Hence det $A_{n}=n+1$.

### **Q**

