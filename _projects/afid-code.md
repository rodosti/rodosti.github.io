---
layout: page
title: "AFiD: an open-source code for DNS of turbulent flows"
description: "A massively parallel finite-difference solver, with CPU and GPU versions"
importance: 8
img: assets/img/projects/afid.jpg
category: earlier
---

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/afid.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The simulations in the other research lines are performed using a second order finite difference code with fractional time integration. Other add-ons to the basic simulations are the addition of a Lagrangian second phase in the flow, and the use of a multiple resolution scheme to [decouple the grids where scalars and momentum are discretized](http://www.sciencedirect.com/science/article/pii/S0021999115005586).

The numerical code is written in Fortran 90 and has an MPI parallelization. The MPI domain decomposition is two-dimensional, i.e. in pencils. It uses parallel HDF5 for output, and FFTW/LAPACK libraries for some mathematical operations. Simulations run with this code won in 2012 the Wim Nieuwpoort award for the most efficient use of HPC computing time in the Netherlands. It has run on up to 10k cores on IBM (Fermi@Cineca), Cray (Hermit@HLRS) and Bull (Curie@TGCC) systems, and was shown to scale up to 64k cores on Curie Thin Nodes. The Rayleigh-Bénard version of the code, based on the library [2DECOMP](http://www.2decomp.org/), was open sourced under the name of AFiD, and is available for [download](http://www.afid.eu/). The numerical schemes and computational algorithms are detailed in [this reference](http://www.sciencedirect.com/science/article/pii/S0045793015001164). Thanks to help from people at nVidia, a GPU (CUDA) version of the semi-implicit code is also available.

Due to the flexibility of second-order finite differences, it is easy to extend the code to include objects in the flow through the immersed boundary method. Currently, it is possible to include not only fixed objects such as rough boundaries, but also full fluid-structure interaction, with both weak and strong coupling, and an immersed boundary formulation based on moving least squares. Further developments outside my involvement include the ability to simulate objects which deform and naturally move in the flow, and the simulation of multiphase flows through the Cahn-Hilliard model.

An add-on developed by myself was the [simulation of electro-kinetic flows](http://pubs.rsc.org/en/Content/ArticleLanding/2017/FD/C6FD00247A#!divAbstract). However, the near-wall region of these flows requires substantial resolution, and numerical instabilities due to the accumulation of discretization errors in exponential Debye layers rendered the application of this code quite limited.
