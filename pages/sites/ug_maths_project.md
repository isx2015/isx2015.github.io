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

**<font color="#D95319">*****IN PROGRESS*****</font>**

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

Let $\mu=1$ without loss of generality.

Start the iteration $F$ from origin $$ \left[\begin{array}{l}0 \\ 0\end{array}\right]$$

Number of iterations $n=2000$ or $n=500$

Following pictures are observed.

{% include image.html file="pic_projects/n=2000(5).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=500(2).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=500(3).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=500(5).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=500(15).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=500(20).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=2000(10).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=2000(20).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=2000(22).png" alt="" max-width="400" %}

Some uninteresting pictures where a straight line appears are omitted. For example,

{% include image.html file="pic_projects/n=500(7).png" alt="" max-width="400" %}


### **Restrictions on $A_R$**
Now if we put restriction on $A_R$, i.e. $T_{R}, D_{R}$, such that under $n$ iterations on the right, the point lands on y-axis:

$$F^n(O)=\left[\begin{array}{l}0 \\ y_n\end{array}\right]$$

It is no doubt that $$\left[\begin{array}{l}0 \\ y_n\end{array}\right]$$ will then be mapped to some point on the x-axis: $$\left[\begin{array}{}y_n+\mu \\ 0\end{array}\right]$$

Let $y_n=-2$ in our case.

Still let $\mu=1$.

Following ploygons are generated for different $n$.

{% include image.html file="pic_projects/n=3(1).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=6(2).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=13(5).png" alt="" max-width="400" %}
{% include image.html file="pic_projects/n=20(9).png" alt="" max-width="400" %}



For a series of $n$, under the same scale in axes, it is easy to see the behaviour of the ploygons for increasing $n$ with an GIF image:

{% include image.html file="pic_projects/f3.gif" alt="" max-width="400" %}