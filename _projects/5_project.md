---
layout: page
title: Lid Driven Cavity Solver
description: Incompressible Fractional Step Method 
img: assets/img/lid_driven_cavity/Re5000_lid_snapshot.png
importance: 1
category: Fun
---

I was interested in this project mostly because I had never implemented an incompressible flow solver. Though there are fewer equations in the incomressible Navier-Stokes compared to the compressible equations, they can be more challenging to solve. The reason for this is because the incompressibility contraint requires you to solve a Poisson equation for the pressure. 

In this solver, I've elected to use the fractional step method of Kim and Moin (1985). 

The incompressible Navier-Stokes equations are given as 

1.	Momentum equation:

    \begin{equation}
        \frac{\partial \mathbf{u}}{\partial t} + \mathbf{u} \cdot \nabla \mathbf{u} = -\frac{1}{\rho} \nabla p + \nu \nabla^2 \mathbf{u}
    \end{equation}

2. Continuity equation:
    \begin{equation}
        \nabla \cdot \mathbf{u} = 0
    \end{equation}

The fractional step method breaks the velocity update into two stages. The idea is to compute an intermediate velocity field without enforcing incompressibility and then correct it using a pressure Poisson equation.

A predictor step computes a provisional velocity field \mathbf{u}^*, ignoring the pressure gradient term:

\begin{equation}

\frac{\mathbf{u}^* - \mathbf{u}^n}{\Delta t} = -\mathbf{u}^n \cdot \nabla \mathbf{u}^n + \nu \nabla^2 \mathbf{u}^n

\end{equation}

where \mathbf{u}^n is the velocity at the current time step and \mathbf{u}^* is the provisional velocity. This step evolves the velocity based on the nonlinear convective term and the viscous term.

In the second step, the pressure term is used to adjust the provisional velocity to enforce the incompressibility condition. A pressure correction term is introduced:

\begin{equation}
\frac{\mathbf{u}^{n+1} - \mathbf{u}^*}{\Delta t} = -\frac{1}{\rho} \nabla p^{n+1}
\end{equation}

The pressure on the RHS of the equation above can be found by taking the divergence of the the momentum equations and using the incompressibility constraint. Carrying out this math one would identify the equation

\begin{equation}
\nabla^2 p^{n+1} = \frac{\rho}{\Delta t} \nabla \cdot \mathbf{u}^*
\end{equation}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/img/cavity_flow_speed_pressure_animation.gif" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
