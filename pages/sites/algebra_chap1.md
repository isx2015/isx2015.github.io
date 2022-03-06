---
title: Artin's Algebra Chapter 1
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
Prove that the product of upper triangular matrices is upper triangular.

---
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

<!-- <img src="images/q1.11.png" width="100" height="50"> -->

{% include image.html file="q1.11.png" alt="" caption="relations between indices" max-width="400" %}

transpose $C=AB$ gives similar result for lower triangular matrices.

### **Q1.13**
A square matrix $A$ is nilpotent if $A^{k}=0$ for some $k>0$. Prove that if $A$ is nilpotent, then $I+A$ is invertible. Do this by finding the inverse.

---
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
With $A$ arbitrary, determine the products $e_{i j} A, A e_{i j}, e_{j} A e_{k}, e_{i i} A e_{j j}$, and $e_{i j} A e_{k \ell}$

---
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
Consider an arbitrary system of linear equations $A X=B$, where $A$ and $B$ are real matrices.

(a) Prove that if the system of equations $A X=B$ has more than one solution then it has infinitely many.

(b) Prove that if there is a solution in the complex numbers then there is also a real solution.

---
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
Let $A$ be a square matrix. Show that if the system $A X=B$ has a unique solution for some particular column vector $B$, then it has a unique solution for all $B$.

---
Reduce $A, B$ to row echelon matrices $A', B'$.

Since $A$ is square, $A'$ is either $I$ or its bottom row is zero (by Lemma 1.2.15).

If $A'$ bottom row is zero, to make sure the system have a solution, bottom entry of $B'$ must also be zero.

Now let $A'$ be of dimension n, then $X$ is also n-dimensional. With last row of $A'$ to be zero, there are $n-1$ equations and $n$ unknown variables. The solution cannot be unique. Hence $A'$ is identity.

So $A$ is invertible(Theorem 1.2.16), and the unique solution to the system is $X=A^{-1}B$ for every column vector $B$.

### **Q3.3**
Suppose we make first a row operation, and then a column operation, on a matrix $A$. Explain what happens if we switch the order of these operations, making the column operation first, followed by the row operation.

---
Let elementary row and column matrices be $E_R$ and $E_C$,

by associative law, $(E_R A)E_C=E_R (A E_C)$, so the effects are the same if switching the order.

### **Q4.3**
Compute the determinant of the following $n \times n$ matrix using induction on $n$ :
$$
\left[\begin{array}{rrrrrr}
2 & -1 & & & & \\
-1 & 2 & -1 & & & \\
& -1 & 2 & -1 & & \\
& & -1 & \cdot & & \\
& & & & \cdot & & \\
& & & & & 2 & -1 \\
& & & & & -1 & 2
\end{array}\right]
$$

---
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

### **Q4.4**
Let $A$ be an $n \times n$ matrix. Determine $\operatorname{det}(-A)$ in terms of $\operatorname{det} A$.

---
From the relation

$$
det(rA)=r^n det(A) \\
(r \text{ is a constant,} n \text{ is the dimension of square matrix } A )
$$

$$
\Rightarrow det(-A)=(-1)^n det(A)
$$

### **Q4.5**
Use row reduction to prove that $\operatorname{det} A^{t}=\operatorname{det} A .$

---
To define $det(A^t)$ and $det(A)$, $A$ must be square.

when $A$ is not invertible, both sides are zero, so it holds.

when $A$ is invertible, then we have series of elementary matrices $E_k$ such that,

$$
\begin{array}{l}
E_k...E_1 A=I,\\
\text{transpose it}\Rightarrow A^tE_1^t...E_k^t=I\\
\text{so }det(I)=det(E_k...E_1 A)=det(A^tE_1^t...E_k^t)\\
\end{array}
$$

Because $det(AB)=det(A)det(B)$, and the determinant of transpose of elementary matrices doesn't change, we get,

$$
det(A^t)=det(A)
$$

### **Q4.6**
Prove that 

$$\begin{array}{l}\operatorname{det}\left[\begin{array}{cc}A & B \\ 0 & D\end{array}\right]=(\operatorname{det} A)(\operatorname{det} D)\end{array}$$

if $A$ and $D$ are square blocks.

---

### **Q5.3**
Prove that the inverse of a permutation matrix $P$ is its transpose.

---
Let permutation matrix be $P=\sum_{i} e_{pi, i}$. Where $pi\equiv p(i)$ (permutation $p$).
Thus, $P^{t}=\sum_{j} e_{j, p j}$ (reverse the order of indices of $e$),

$$
\Rightarrow P P^{t}=\sum_{i, j} e_{pi, i} e_{j, pj}=\sum_{i=j} e_{pi, pi}=I
$$

### **Q5.4**
What is the permutation matrix associated to the permutation of $n$ indices defined by $p(\mathbf{i})=\mathbf{n}-\mathbf{i}+\mathbf{1}$ ? What is the cycle decomposition of $p ?$ What is its sign?

---
$p(1)=n$ 

$p(2)=n-1$

…

$p(n-1)=2$

$p(n)=1$

the permutation interchanges row $i$ and row $n-i+1$, symbolically this corresponds to matrix 

$$\left(\begin{array}{lll}1 & & \\ & \ddots & \\ & & 1\end{array}\right)$$

cycle decomposition is $(1,n )(2, n-1) \cdots\left(\frac{n}{2}, \frac{n}{2}+1\right)$ if $n$ is even, $(1,n )(2, n-1) \cdots\left(\frac{n+1}{2}, \frac{n+1}{2}\right)$ if $n$ is odd.

Hence, the sign of the permutation is + if n is even, - if n is odd.

### **Q6.2**
Let $A$ be an $n \times n$ matrix with integer entries $a_{i j}$. Prove that $A$ is invertible, and that its inverse $A^{-1}$ has integer entries, if and only if $\operatorname{det} A=\pm 1$.

---
First prove the necessary condition:
Suppose $\operatorname{det} A \neq \pm 1$
The $(i, j)$ th entries of $A^{-1}$ is $\left(A^{-1}\right)_{i j}=\frac{(-1)^{i+j}}{\operatorname{det} A} \operatorname{det} A_{j i}$
So $\left(A^{-1}\right)_{i j}$ is integer iff $\operatorname{det} A$ divides $\operatorname{det} A_{ji}$
But $\operatorname{det} A=\sum_{\nu}(-1)^{j+\nu} a_{j \nu} \operatorname{det} A_{j \nu}=\sum_{\nu \neq i}(-1)^{j+\nu} a_{j\nu} \operatorname{det} A_{j\nu}$ $+(-1)^{j+i} a_{j i} \operatorname{det} A_{j i}$
$\operatorname{det} A$ divides $\operatorname{det} A_{j i}$ ony if $\operatorname{det} A \leqslant \operatorname{det} A_{j i}$
However, this is not alway true. Consider the terms in $\operatorname{det} A$:  $\sum_{\nu \neq i}(-1)^{j+\nu} a_{j\nu}$  could be postive and $(-1)^{j+i} a_{j i}$ can be greater than 1 .
So $\operatorname{det} A=\pm 1$

Now prove the sufficient condition:
Since $\operatorname{det} A=\pm 1$,
the entry $\left(A^{-1}\right)_{i j}=(-1)^{m} \operatorname{det} A_{j i}$ must be integer because det $A_{j i}$ is integer (entries of $A$ are integers by assumption). $\operatorname{det} A \neq 0$, so A is invertible. 

Q.E.D.