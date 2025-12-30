---
layout: page
title: DNS Database of Bypass Transition Boundary Layer
description: CTR Summmer Program 2024
img: 
importance: 1
category: Research
---

In this research project, we report a comprehensive set of direct numerical simulation benchmark statistics of bypass transition in the 
narrow sense with inlet freestream turbulent intensity levels $0.75\%$, $1.5\%$,  $2.25\%$,  $3.0\%$ and $6.0\%$,
respectively. This database is freely available for download at the [Center for Turbulent Research](https://ctr.stanford.edu/about-center-turbulence-research/research-data). 

The pricipal contribution of this work was the identification of two breakdown methods from laminar to turbulent at intermediate freestream turbulence intensities. 

Additionally, an intermittency correlation formula is proposed and compared with literature data, and the classical Abu-Ghannam and Shaw correlation is found to describe the beginning, rather than the completion, of the late transitional stage. 

<div class="row">
    <div class="col_sm">
        {% include figure.liquid loading="eager" path="assets/img/wu_bl/comp_to_AGS.png" title="tbnn result" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col_sm">
        {% include figure.liquid loading="eager" path="assets/img/wu_bl/correlation_plot.png" title="tbnn result" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Our propsed correlation curve can be used to identify the onset of transition where the intermittency function $$\gamma = 0$$. Using this value of Reynolds number to normalize our skin friction data, and by plotting against a properly scaled skin friction, we are able to collapse the skin friction curves from all of our DNS through the laminar, transitional, and turbulent regimes.

<div class="row">
    <div class="col_sm">
        {% include figure.liquid loading="eager" path="assets/img/wu_bl/collapse_curve.png" title="tbnn result" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

It was also shown that some existing RANS models for predicting boundary layer transition are highly sensitive to the choice of free parameters, such as characteristic inflow turbulence length scales. In particular, we used the $$k-\omega$$ SST turbulence model coupled to the $$\gamma-Re_{\theta}$$ transition model in OpenFOAM. We found the the free parameter in this setup, a length-scale associated with the turbulence at the inlet of the computational domain, could dramatically alter the results of the RANS simulation. 

<div class="row">
    <div class="col_sm">
        {% include figure.liquid loading="eager" path="assets/img/wu_bl/rans_L_sensitivity.pdf" title="tbnn result" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


Reports and publications coming soon!
