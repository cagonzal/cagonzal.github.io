---
layout: page
title: Conjugate Heat Transfer in a Ribbed Channel
description: Final Project for ME469 (Computational Methods in Fluid Dynamics)
img: assets/img/conj_channel/pv_streamlines.png
importance: 4
---

This project was done in collaboration with my classmate, Kimberly Liu. Our project was based upon the work in <em>[Conjugate heat transfer in a channel with staggered ribs](https://www.sciencedirect.com/science/article/pii/0017931085901425)</em>. We studied the effects of conductive walls for laminar flow through a ribbed channel. This problem is relevant to many applications, such as the thermal management and cooling of electronics and machinery. Simulations were performed using [Nalu](https://nalu.readthedocs.io/en/latest/), a generalized, unstructured, massively parallel, low-Mach flow solver built and managed by Sandia Labs.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/conj_channel/combined.png" title="temp and velocity contour" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
