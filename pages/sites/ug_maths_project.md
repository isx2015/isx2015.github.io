---
title: Undergraduate Maths Project
keywords: undergraduate, maths, project, maths project,
last_updated: 
summary: ""
sidebar: mydoc_sidebar
permalink: ug_maths_project.html
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


**<p style="color:#D95319">\*\*\*\*IN PROGRESS\*\*\*\*</p>**


## Normal form of the bifurcation
It is a iterative map $F: \mathbb{R}^{2} \rightarrow \mathbb{R}^{2}$ such that
$$\boldsymbol{x}_{n+1}= F(\boldsymbol{x_n})=\begin{cases}A_{L} \boldsymbol{x}+\boldsymbol{m} & x \leqslant 0 \\ A_{R} \boldsymbol{x_n}+\boldsymbol{m} & x \geqslant 0\end{cases}$$

where 

$$A_{\alpha}=\left[\begin{array}{cc}T_{\alpha} & 1 \\ -D_{\alpha} & 0\end{array}\right],\quad (\alpha=L \text{ or } R)$$
$L$ and $R$ indicate Left or Right side of the y-axis.

$$\boldsymbol{m}=\left[\begin{array}{l}\mu \\ 0\end{array}\right],(\mu \text{ is a constant}) \quad \boldsymbol{x_k}=\left[\begin{array}{l}x_{k}\\y_{k}\end{array}\right]$$

In matrix notation: 

$$\left[\begin{array}{l}x_{n+1} \\ y_{n+1}\end{array}\right]=\left[\begin{array}{cc}T_{\alpha} & 1 \\ -D_{\alpha} & 0\end{array}\right]\left[\begin{array}{l}x_{n} \\ y_{n}\end{array}\right]+\left[\begin{array}{l}\mu \\ 0\end{array}\right]$$
---
### **Some preliminary random test with the map $F$**

Four parameters $T_{L}, D_{L}, T_{R}, D_{R}$ are randomly chosen from the interval $(-2,2)$. 

Start the iteration $F$ from origin $$ \left[\begin{array}{l}0 \\ 0\end{array}\right]$$

Number of iterations $n=2000$ or $n=500$

Following pictures are observed.
{% include image.html file="pic_projects/n=2000(5).png" alt="" max-width="400" %}
