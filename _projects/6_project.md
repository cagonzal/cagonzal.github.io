---
layout: page
title: DNS Database of Bypass Transition Boundary Layer
description: CTR Summer Program 2024
img: assets/img/wu_bl/collapse_curve.png
importance: 1
category: Research
---

In this research project, we report a comprehensive set of direct numerical simulation benchmark statistics of bypass transition in the 
narrow sense with inlet freestream turbulent intensity levels $0.75\%$, $1.5\%$,  $2.25\%$,  $3.0\%$ and $6.0\%$,
respectively. This database is freely available for download at the [Center for Turbulence Research](https://ctr.stanford.edu/about-center-turbulence-research/research-data). 

The principal contribution of this work was the identification of two breakdown methods from laminar to turbulent at intermediate freestream turbulence intensities. 

Additionally, an intermittency correlation formula is proposed and compared with literature data, and the classical Abu-Ghannam and Shaw correlation is found to describe the beginning, rather than the completion, of the late transitional stage. 

<div class="row">
    <div class="col-sm">
        {% include figure.liquid loading="eager" path="assets/img/wu_bl/comp_to_AGS.png" title="comparison to Abu-Ghannam and Shaw correlation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm">
        {% include figure.liquid loading="eager" path="assets/img/wu_bl/correlation_plot.png" title="intermittency correlation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Our proposed correlation curve can be used to identify the onset of transition where the intermittency function $$\gamma = 0$$. Using this value of Reynolds number to normalize our skin friction data, and by plotting against a properly scaled skin friction, we are able to collapse the skin friction curves from all of our DNS through the laminar, transitional, and turbulent regimes.

<div class="row">
    <div class="col-sm">
        {% include figure.liquid loading="eager" path="assets/img/wu_bl/collapse_curve.png" title="skin friction collapse" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

It was also shown that some existing RANS models for predicting boundary layer transition are highly sensitive to the choice of free parameters, such as characteristic inflow turbulence length scales. In particular, we used the $$k-\omega$$ SST turbulence model coupled to the $$\gamma-Re_{\theta}$$ transition model in OpenFOAM. We found the free parameter in this setup, a length-scale associated with the turbulence at the inlet of the computational domain, could dramatically alter the results of the RANS simulation. 

<div class="row">
    <div class="col-sm">
        {% include figure.liquid loading="eager" path="assets/img/wu_bl/rans_L_sensitivity.png" title="RANS length-scale sensitivity" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


Published in [Physical Review Fluids](https://doi.org/10.1103/g72g-q82r) ([arXiv](https://arxiv.org/abs/2503.03844)) and the [Journal of Fluids Engineering](https://doi.org/10.1115/1.4070700) ([arXiv](https://arxiv.org/abs/2502.19609)).
