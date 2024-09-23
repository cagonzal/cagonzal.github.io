---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 1
display_categories: [Research]
horizontal: true
---

Modeling the transition from laminar to turbulent flow remains a significant challenge in the numerical simulation of boundary layers, especially at coarse grid resolutions. Accurately predicting this transition is crucial for the computation of the drag force, as well as identifying the state of the boundary layer in areas where flow separation may occur due to pressure gradient. 

Direct numerical simulation (DNS) and wall-resolved large-eddy simulations (WRLES) are scale resolving simulation techniques, that unfortunately, are too computationally expensive for engineering flows of interest at realistic Reynolds numbers. Wall-modeled LES (WMLES) offer significant computational savings by modeling the near wall region of turbulent flows, however, investigations at the Center for Turbulence research has shown that state-of-the-art techniques are not suitable for the simulation of transitional flows. 

My research tackles this problem by using the Falkner-Skan similarity solution as a wall model that is applicable in the laminar portion of flows. Additionally, my research leverages the parabolized stability equations to act as a physics-based, but computationally inexpensive, method to model the transitional portion of wall-bounded flows. Below are contours of near-wall spanwise velocity for three transition scenarios considered in my research. All figures come from WRLES computed using the charLES flow solver. The top figure is an oblique transition, the middle figure is K-type transition, and the bottom figure is H-type transition. For a detailed discussion on oblique transition, refer to [Berlin *et al.*](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/1ABE909F9852E87AAF88019579D86B86/S002211209900511Xa.pdf/numerical-and-experimental-investigations-of-oblique-boundary-layer-transition.pdf) For a discussion on H- and K-type transition, refer to [Sayadi *et al.*](https://www.cambridge.org/core/journals/journal-of-fluid-mechanics/article/direct-numerical-simulation-of-complete-htype-and-ktype-transitions-with-implications-for-the-dynamics-of-turbulent-boundary-layers/14A734E8A06691C4768538EE6C614E39)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/oblique_u_contour.png" title="oblique transition" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/ktype_extended_u_contour.png" title="ktype transition" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/htype_extended_u_contour.png" title="htype transition" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Reports
===

[Simulating an H-type transitional boundary layer in a coupled NLPSE and WMLES framework with a Falkner-Skan wall model](https://web.stanford.edu/group/ctr/ResBriefs/2023/27_Gonzalez.pdf)

[Temporal stability analysis of high Mach number
boundary layers over cooled impedance walls](https://web.stanford.edu/group/ctr/ctrsp22/vi02_Broeck.pdf)

[Falkner-Skan wall model baseflow generation for
the parabolized stability equations](http://web.stanford.edu/group/ctr/ResBriefs/2021/08_Gonzalez.pdf)

[Wall-stress modeling for laminar boundary layers
in coarse grids](http://web.stanford.edu/group/ctr/ResBriefs/2020/10_Gonzalez.pdf)


Presentations
===

Gonzalez, C., Harris, S., & Moin, P. (2023). Simulating an H-type transitional boundary layer in a coupled NLPSE and WMLES framework with a Falkner-Skan wall model. Bulletin of the American Physical Society.

Gonzalez, C., & Moin, P. (2022). Falkner-Skan wall model for laminar boundary layers. Bulletin of the American Physical Society.

De Broeck, L., Goertz, S., Flint, T., Gonzalez, C., Oberlack, M., & Lele, S. (2022). Suppression of acoustic instabilities in boundary layer flows by heating/cooling of the wall and wall impedance. Bulletin of the American Physical Society.

Gonzalez, C., Karp, M., Harris, S., & Moin, P. (2021). Reduced-order Modeling of Laminar Boundary Layers. Bulletin of the American Physical Society.

Gonzalez, C., Karp, M., & Moin, P. (2020). Wall-stress Modeling for Laminar Boundary Layers. Bulletin of the American Physical Society.

