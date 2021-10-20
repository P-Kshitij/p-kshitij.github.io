---
layout: post
title:  "On Open Sets of Reals"
date:   2021-06-26 12:23:01 +0530
categories: [mathtalk]
description: "Some perspectives on the theorem: <em>A non-empty open set of reals is the disjoint union of countably many open intervals</em>"
permalink: "/:title/"
---


Reading <em>Real Analysis</em> by <em>Royden</em>, one of the results which I found a bit surprising is the following:

<div class="theorem">
A non-empty open set of reals is the disjoint union of countably many open intervals
</div>
Just to recap, let us have some definitions to clear the way.
<div class="definition">
A set $ E $ is <strong>open </strong> if for each point $p \in E$, there is a radius $r$ such that $N_r(p) \subset E$ (neighbourhood of $p$ of radius r). This is equivalent to saying that each point of $E$ is an interior point.
</div>
For $\mathbb{R}$, this just boils down to having an interval $(p-r,p+r) \subset E$. 

Though nowhere online could I find a very precise definition of an (open) interval of reals, the following might just work for our purposes.
<div class="definition">
An <strong>open interval </strong> $I$ is a set of reals, characterized by two extended real numbers $a,b$ with $a < b$ such that $I = \{\ x \ | \ a< x < b\}$. Notation $I = (a,b)$
</div>

Note than we say extended real numbers to account for unbounded open intervals, meaning that $a,b$ can also take values $\pm \infty$



Now what the original statement is essentially saying is that somehow any non-empty open set of reals (which does not seem like that strong of a constraint) can be written as:
<ol>
<li>a union of open intervals </li>
<li> which are disjoint </li>
<li> and only countably many of them </li>
</ol>
## A first proof
First we see the following proof from Royden:
<div class="proof">
Let $E$ be a non-empty open set of reals and let $x \in E$. Then because $E$ is open, there exist $a,b$ with $a < x < b$ such that $(a,x) \subseteq E$ and $(x,b) \subseteq E$. Consequently, this lets us define two extended real numbers $y_x,z_x$ as follows:
$$
\begin{align}
y_x = \inf\{ \ a \ | \ (a,x) \subseteq E\}  \\ z_x = \sup\{ \ b \ | \ (x,b) \subseteq E\}
\end{align}
$$
Again we say extended real numbers to accomodate the possibility of $y$ and $z$ being $-\infty$ and $\infty$ respectively.
Let $I_x = (y_x, z_x)$. 

<div class = "claim">
$I_x \subseteq E$ but $y_x,z_x \notin E$
</div>

To see the first part, let $x < w < z_x$. As $z_x$ is the supremum, there exist a $y > w$ such that $(x, y) \subseteq E$, which implies that $w \in E$. The second part can seen by contradiction, by assuming $y_x \in E$. As $E$ is open, this means that there is a $r$ such that $(y_x - r, y_x + r)$, which implies that $(y_x-r,x) \subseteq E$, which contradicts the assumption that $y_x$ is the infimum.
<br><br>
Now consider $\{I_x\}_{x \in E}$. Clearly, $ E \subseteq \bigcup\{I_x\}_{x \in E}$. Also, using the above claim $\bigcup\{I_x\}_{x \in E} \subseteq E$. Thus $E = \bigcup\{I_x\}_{x \in E}$. It also follows from the claim that these are disjoint. For two distinct $I_a, I_b \in \{I_x\}_{x \in E}$ either $y_a \neq y_b$ or $z_a \neq z_b$ (or both). WLOG assume that $y_a < y_b$. Also let $\alpha \in I_a$ and $\alpha \in I_b$. Note that $(y_a, \alpha) \subseteq E$ and $(y_b, \alpha) \subseteq E$. Also as $y_a < y_b$, $y_b \in (y_a, \alpha)$ and so $y_b \in E$ which contradicts the claim proved above.
<br><br>
So we have shown that $E = \bigcup \{I_x\}_{x \in E}$, where each $I_x$ is an <strong>open interval</strong> and <strong>pairwise disjoint</strong>. Showing the countable part is relatively easier. We know that the rationals are dense in $\mathbb{R}$. Hence in each $I_x$ there is a rational $q_x$. Hence we get a mapping from each $I_x$
to a distinct rational $q_x$ (disjoint), which implies that $\{I_x\}_{x \in E}$ is countable.
</div>
More proofs to be added soon.

<script>
MathJax.Hub.Queue(["Typeset",MathJax.Hub]);
</script>


