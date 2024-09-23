---
layout: page
title: 3D Compressible Navier-Stokes Solver for Jet Flows
description: Project for ME344 (High Performance Computing)
img: assets/img/comp_solver/phi_iso_39000.png
importance: 1
category: Classes
---

This project was done in a collaboration with my classmate, Michael Whitmore. A 3D, compressible, finite difference code was written to solve the Navier-Stokes equations in Python. The motivation behind the project was to develop a solver that can simulate jet flows with an immersed passive tracer, a case that is representative of coughs and sneezes contaminated with COVID-19 viral droplets. The code was parallelized using mpi4py.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/comp_solver/u_snapshot_goodish_001.png" title="velocity snapshot" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/comp_solver/strong_scaling.png" title="strong scaling" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/comp_solver/weak_scaling.png" title="weak scaling" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

