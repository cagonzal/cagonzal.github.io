---
title: "3D Compressible Navier-Stokes Solver for Jet Flows"
excerpt: "Project for ME344 (High Performance Computing)"
collection: portfolio
---

This project was done in a collaboration with my classmate, Michael Whitmore. A 3D, compressible, finite difference code was written to solve the Navier-Stokes equations in Python. The motivation behind the project was to develop a solver that can simulate jet flows with an immersed passive tracer, a case that is representative of coughs and sneezes contaminated with COVID-19 viral droplets. The code was parallelized using mpi4py.

<div class="row">
	<div class="column">
		<img src='/images/me344/u_snapshot_goodish_001.png' style="width=200">
	</div>
	<div class="column">
		<img src='/images/me344/phi_snapshot_goodish_001.png' style="width=200">
	</div>
</div>

<div class="row">
	<div class="column">
		<img src='/images/me344/phi_iso_39000.png' style="width=200">
	</div>
</div>

<div class="row">
	<div class="column">
		<img src='/images/me344/strong_scaling.png' style="width=200">
	</div>
	<div class="column">
		<img src='/images/me344/weak_scaling.png' style="width=200">
	</div>
</div>

