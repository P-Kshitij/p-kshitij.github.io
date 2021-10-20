---
layout: post
title:  "Statistical Guide to loss functions"
date:   2021-06-26 12:23:01 +0530
categories: [aitalk]
description: "A different perspective on loss functions using Statistical Learning Theory"
permalink: "/aitalk/statguide_lossfuncs/"
---

Often in practice, we are see a variety of loss functions in different domains. Intuitively, we may erroneously think (atleast I did) of them as computationally different ways of arriving at the same target.

<div>
<img src="/images/statguide_loss_fig1.png" width="600" />
</div>

<br> For example in a vanilla regression problem given $f(x)$ to be our estimate function and $y$ to be the true value, consider two loss functions:

$$\ell_1(f(x),y) = (f(x) - y)^2 \quad  \text{ and } \quad \ell_2(f(x),y) = |f(x) - y|$$ 

What is the advantage of choosing one over the other? In a "hand-wavy" sense both penalize our estimate when it is away from the true value, so it feels natural to assume that both lead our estimate towards the same optimal target. Although the optimization dynamics of both loss functions maybe different, they must be yielding the same end result (minimizer) right? Well not quite!

<div>
<img src="/images/statguide_loss_fig2.png" width="600" />
</div>

> Under construction! 🚧 

<script>
MathJax.Hub.Queue(["Typeset",MathJax.Hub]);
</script>
