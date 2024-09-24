---
layout: page
title: 3D Compressible Navier-Stokes Solver for Jet Flows
description: Project for ME344 (High Performance Computing)
img: assets/img/comp_solver/phi_iso_39000.png
importance: 1
category: Classes
---

This project was done in a collaboration with my classmate, Michael Whitmore. A 3D, compressible, finite difference code was written to solve the Navier-Stokes equations in Python. The motivation behind the project was to develop a solver that can simulate jet flows with an immersed passive tracer, a case that is representative of coughs and sneezes contaminated with COVID-19 viral droplets. The code was parallelized using mpi4py. 

The compressible Navier-Stokes equations are solved using a second order MacCormack scheme. The scheme uses a two-step time integration that uses first-order forward differences at the first step and first-order backward differences at the second step. 

Predictor Step:

\begin{equation}
    \overline{U}_{i,j,k}^{t+\Delta t} = U_{i,j,k}^t - \frac{\Delta t}{\Delta x} \left( E_{i+1,j,k}^t - E_{i,j,k}^t \right) - \frac{\Delta t}{\Delta y} \left( F_{i,j+1,k}^t - F_{i,j,k}^t \right) - \frac{\Delta t}{\Delta z} \left( G_{i,j,k+1}^t - G_{i,j,k}^t \right)
\end{equation}

Corrector Step

\begin{equation}
    U_{i,j,k}^{t+\Delta t} = \frac{1}{2}\left(U_{i,j,k}^t + \overline{U}_{i,j,k}^{t+\Delta t} - \frac{\Delta t}{\Delta x} \left(\overline{E}_{i,j,k}^{t+\Delta t} - \overline{E}_{i-1,j,k}^{t+\Delta t}\right) - \frac{\Delta t}{\Delta y} \left(\overline{F}_{i,j,k}^{t+\Delta t} - \overline{F}_{i,j-1,k}^{t+\Delta t}\right) - \frac{\Delta t}{\Delta z} \left(\overline{G}_{i,j,k}^{t+\Delta t} - \overline{G}_{i,j,k-1}^{t+\Delta t}\right)\right)
\end{equation}

where 

\begin{equation}
U = \begin{bmatrix}
\rho, \, \rho u, \, \rho v, \, \rho w, \, E_t, \, \rho \phi
\end{bmatrix}
\end{equation}

\begin{equation}
E = \begin{bmatrix}
\rho u^2 + p - \tau_{xx}, \, \rho uv - \tau_{xy}, \, \rho uw - \tau_{xz}, \, (E_t + p)u - u\tau_{xx} - v\tau_{xy} - w\tau_{xz} + q_x, \, \rho \phi - D\frac{\partial \phi}{\partial x}
\end{bmatrix}
\end{equation}

\begin{equation}
F = \begin{bmatrix}
\rho v, \, \rho uv - \tau_{xy}, \, \rho v^2 + p - \tau_{yy}, \, \rho vw - \tau_{yz}, \, (E_t + p)v - u\tau_{xy} - v\tau_{yy} - w\tau_{yz} + q_y, \, \rho \phi - D\frac{\partial \phi}{\partial y}
\end{bmatrix}
\end{equation}

\begin{equation}
G = \begin{bmatrix}
\rho w, \, \rho uw - \tau_{xz}, \, \rho vw - \tau_{yz}, \, \rho w^2 - \tau_{zz}, \, (E_t + p)w - u\tau_{xz} - v\tau_{yz} - w\tau_{zz} + q_z, \, \rho \phi - D\frac{\partial \phi}{\partial z}
\end{bmatrix}
\end{equation}

A rectangular prism is used for the computational domain. Ambient pressure boundary conditions are used on the top and bottom walls and periodic boundary conditions are used in the spanwise direction. The size of the computational domain is $$50h \times 25h \times 1h$$ where $$h$$ is the height of the jet inlet. The inlet height is chosen to approximate the diameter of a human mouth ($$h = 0.04m$$). Numerical sponges are used at the top and bottom boundaries as well as the outlet boundary in order to dampen any reflectd flow characteristics. To approximate the conditions of a human cough, a max inlet velocity of $$10m/s$$ is used with an approximately parabolic profile for stability considerations. Additionally, a coflow of about $$10\%$$ of the jet inlet velocity is added to prevent spurious circulations towards the inlet. A conserved passive scalar contaminant is used to model the transport of aerosols. The scalar contaminant has a value of unity at the inlet and zero everywhere else. 

Shown below are iso-surface contours of $$\phi = {0.1, 0.33, 0.57}$$ at $$t = 0.88$$. We see that high concentration of the passive scalar persists well into the two meter domain, with significant mixing in the normal direction. The implications of this result are that the "six feet" rule is not effective to limit the spread of aerosols by flows from coughs or sneezes. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/comp_solver/phi_iso_39000.png" title="phi isocontour" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The strong scaling analysis of the code gave promising results. It is continuing to speed up without hitting diminishing results on up to 48 processors (the limit available during this project). The weak scaling analysis shows that the code does tradeoff some efficiency to run on larger numbers of processors. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/comp_solver/strong_scaling.png" title="strong scaling" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/comp_solver/weak_scaling.png" title="weak scaling" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


