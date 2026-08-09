---
title: "Consequences: electromagnetic loads in W7-X"
subtitle: "What happens to the machine when the plasma pops."
eyebrow: "01 / Current work"
thread: 1
order: 1
permalink: /research/modeling-consequences/
excerpt: "Whenever the magnetic field inside a fusion device changes quickly, currents are induced in the conducting structures. Those currents interact with the background field and pull on the machine. Predicting the resulting forces is a prerequisite for designing future tokamaks and stellarators and safely operating the ones we have now."
tags:
  - ThinCurr
  - stellarators
  - MHD
  - ML surrogates
---

Whenever the magnetic field inside a fusion device changes quickly, currents are induced in the conducting structures surrounding the plasma: the vacuum vessel, the passive plates, the support structure. Those induced currents interact with the background field and exert forces on the machine itself. A device that survives one such event may not survive a thousand.

Tokamak disruptions are the most dramatic version of this problem, since several megaamperes (MAs) of plasma current terminate in milliseconds. But rapid plasma quenches have also been observed in [stellarators such as W7-X](https://www.sciencedirect.com/science/article/pii/S0920379623000765) carrying MAs of diamagnetic current, and future quasi-axisymmetric (QA) devices amy also carry large toroidal plasma currents. The complex three-dimensional geometry of stellarator vessels and other components can concentrate these forces locally, motivating careful electromagnetic analysis.

This is the focus of my DOE Fusion Energy Sciences Postdoctoral Fellowship at Columbia, working with Prof. Carlos Paz-Soldan and Research Scientist Chris Hansen. The fellowship is organized around expanding modeling capability for inductively-induced currents along three axes:

## 1) Breadth

Most eddy-current modeling has been developed for and validated against tokamaks, but rapid plasma quenches can also be problematic for stellarators. I am applying [ThinCurr](https://github.com/hansec/OpenFUSIONToolkit), a thin-wall electromagnetic code, to model eddy currents from plasma transients in W7-X. This work will contribute to setting operational limits in W7-X, demonstrate the challenge for future devices, and develop a modeling approach that can help tame this problem.

## 2) Depth

Sophisticated plasma models of disruptions still generally rely on simplistic wall models.Coupling ThinCurr to an M3D-C1 will allow for self-consistent simulation of the current quench and the vertical displacement event that include 3D eddy current effects.

## 3) Speed

High-fidelity coupled simulations are far too slow to sit inside a design-optimization loop. I will build differentiable surrogates, both machine-learned and reduced-order, for the forces experienced by tokamaks and stellarators. Differentiability matters here: it means the force model can be a term in an optimizer's objective function rather than a check performed after the fact. For stellarator coil and structure optimization, where the design space is enormous and every candidate geometry has a different electromagnetic response, that difference may be what makes the calculation practical at all.