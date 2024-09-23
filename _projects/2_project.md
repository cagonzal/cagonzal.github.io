---
layout: page
title: Investigation of Stochastic Models for Particle Dispersion
description: Final Project for ME461 (Advanced Topics in Turbulence)
img: assets/img/stochastic_project/ugrad_1000P_trajectories.png
importance: 2
category: Classes
---

This project follows the work of Paul Durbin from his paper <em>[A stochastic model of two-particle dispersion and concentration flucturations in homogenous turbulence](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/stochastic-model-of-twoparticle-dispersion-and-concentration-fluctuations-in-homogeneous-turbulence/6417933E6799E5669D0D97DED000023C)</em> in using a Lagrangian approach to model the dispersion of a passive scalar in homogenous turbulence.

Ornstein-Uhlenbeck processes are used in the context of the Langevin equations to model fluid parcel velocities as stochastic processes. By tracking particles, we can compute turbulent statistics of the flow.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stochastic_project/homogenous_shear_result4000.png" title="shear result" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stochastic_project/meanCcomp.png" title="concentration result" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
