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
  - extended MHD
  - ML surrogates
  - VDEs
---

Whenever the magnetic field inside a fusion device changes quickly, currents are induced in the conducting structures surrounding the plasma: the vacuum vessel, the passive plates, the support structure. Those induced currents interact with the background field and exert forces on the machine itself. A device that survives one such event may not survive a thousand.

Tokamak disruptions are the most dramatic version of this problem, since several megaamperes of plasma current terminate in milliseconds. But rapid plasma quenches have also been observed in [stellarators such as W7-X](https://www.sciencedirect.com/science/article/pii/S0920379623000765). The complex three-dimensional geometry of stellarator vessels and other components can concentrate these forces locally, motivating careful electromagnetic analysis.

This is the focus of my DOE Fusion Energy Sciences Postdoctoral Fellowship at Columbia, working with Prof. Carlos Paz-Soldan and Research Scientist Chris Hansen. The fellowship is organized around expanding modeling capability for inductively-induced currents along three axes.

## Breadth

Most eddy-current modeling has been developed for and validated against tokamaks, whose axisymmetry makes the problem tractable. Stellarators and mirrors break that assumption. Their fully three-dimensional geometry means the induced current paths cannot be reduced the way they can in an axisymmetric machine, and the tools that work well for tokamaks do not transfer directly.

I am extending [ThinCurr](https://github.com/hansec/OpenFUSIONToolkit), a thin-wall electromagnetic code, to model eddy currents from plasma transients across all of these device classes. Stellarator design is where I expect this to matter most, since stellarator programs are making structural decisions now without the electromagnetic modeling tools that tokamak designers have had for decades.

## Depth

Eddy-current codes typically treat the plasma as a prescribed source. You tell the code what the plasma did, and it tells you what the structure does in response. In reality the coupling runs both ways, because induced wall currents alter the field the plasma sees, which alters how the plasma moves. Coupling ThinCurr to an extended-MHD code (M3D-C1 or NIMROD) allows self-consistent simulation of the current quench and the vertical displacement event that usually accompanies it.

## Speed

High-fidelity coupled simulations are far too slow to sit inside a design-optimization loop, let alone a real-time controller. I am building accelerated, differentiable surrogates, both machine-learned and reduced-order, for the forces experienced by tokamaks and stellarators. Differentiability matters here: it means the force model can be a term in an optimizer's objective function rather than a check performed after the fact. For stellarator coil and structure optimization, where the design space is enormous and every candidate geometry has a different electromagnetic response, that difference is what makes the calculation practical at all.
