---
layout: page
title: "Body/Blade-Vortex Interaction"
description: "What happens when a vortex hits a cylinder, a wing or a rotor blade"
importance: 4
img: assets/img/projects/blade-vortex.jpg
category: current
---

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/blade-vortex.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

As a spin-off from the vortex ring collision problem, we started asking whether we could "cut" a ring by impacting it on a topologically thin wire. We soon found out that this problem is associated with a wide variety of applications, notably in the aerospace industry, where the vortices coming off helicopter blades impact the next blade of the rotor, producing significant sound. We also found that there was some research on this problem, but not many modern simulations.

To fill this research gap, we started off by [simulating the interaction between a cylinder and a vortex](https://doi.org/10.1103/PhysRevFluids.9.054701) of similar sizes, varying the speed of impact (controlling a non-dimensional number called the impact parameter). We were able to numerically reproduce "weak" and "strong" vortex regimes which had been experimentally observed, and to delineate transitions between both regimes. In a more recent study with Andrés Herrera-Gómez and Juan Antonio Tendero-Ventanas, we numerically compared the interaction between a vortex tube and a body to that between a ring and a thin cylinder (or wire). We found that [the role of topology was crucial](https://doi.org/10.1017/jfm.2026.11940) in determining the outcomes of the simulations, and that one could "cut" rings in half, or into even more pieces, with the correct obstacle shape.

We are now extending this work in several ways. First, the original study took place in a "normal" plane, where the vortex axis, the cylinder axis, and the impact direction were all perpendicular to each other. We are now varying the angles between vortex, impact direction and object, in order to investigate other types of Blade-Vortex Interaction. Second, we are simulating different sizes and types of bodies, attempting to progress beyond cylinders and vortices of the same size into bodies which are more applicable to the aerospace industry. Finally, we are also researching the industrial problem through DNS and RANS simulations of wings or the Caradonna-Tung rotor, in an attempt to characterize the relevant geometrical and dynamical parameters of blade-vortex interaction.
