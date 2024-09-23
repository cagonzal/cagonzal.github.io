---
layout: page
title: Galiliean Invariance Preserving Deep Learning for Canonical Fluid Flows
description: Final Project for CS230 (Deep Learning)
img: assets/img/deep_learning/tbnn1_linear_3.png
importance: 3
category: Classes
---

This project was done in a collaboration with my classmate, Kimberly Liu. The goal of this project was to use the Tensor Basis Neural Network (TBNN)<sup>[1]</sup> to predict the Reynolds stress tensor in canonical flow configurations. We tested our model on turbulent channel and turbulent Couette flow using data from the UT Austin Oden Institute. Pictured below is a comparison between the DNS and TBNN values of the b<sub>12</sub> component of the Reynolds anisotropy tensor as a function of wall-normal height for channel flow at Re<sub>$\tau$</sub> = 550. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/deep_learning/tbnn1_linear_3.png" title="tbnn result" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

[1]Ling, J., Kurzawski, A., & Templeton, J. (2016). Reynolds averaged turbulence modelling using deep neural networks with embedded invariance. Journal of Fluid Mechanics, 807, 155-166.

