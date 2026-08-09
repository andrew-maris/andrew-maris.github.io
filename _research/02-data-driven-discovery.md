---
title: "Causes: interpretable machine learning"
subtitle: "Clarifying the density limit threshold across five tokamaks."
eyebrow: "02 / PhD thesis"
thread: 2
order: 2
permalink: /research/data-driven-discovery/
excerpt: "The density limit is one of the fundamental bounds on tokamak operating space, and for forty years it has been estimated with a scaling that does not involve the plasma edge conditions. Assembling a database across five machines showed that edge collisionality is the primary organizing parameter for the limit, and that a two-parameter dimensionless boundary predicts the threshold far better. I measured and applied feedback on that boundary in real time to avoid disruptions at DIII-D."
tags:
  - interpretable ML
  - multi-machine database
  - real-time control
  - DIII-D
  - Alcator C-Mod
  - ASDEX-Upgrage
  - JET
  - TCV
---

Tokamaks disrupt or experience H/L back-transitions when they are pushed to high density. Where that limit sits is usually estimated with the Greenwald scaling, an empirical formula from 1988 built on line-averaged density, plasma current, and minor radius. It is remarkably simple, widely used, but does not involve the plasma edge at all, even though it has been understood for decades that the disruptive boundary is set by edge physics.

This matters practically. ITER and most tokamak pilot-plant concepts need to operate at or above the Greenwald limit to meet their objectives. If the scaling is wrong in either direction, the consequences are expensive.

## The database

My thesis work assembled the largest cross-machine density limit database I am aware of: 258 L-mode density limits, 90 H-mode density limits, and 4,739 non-disruptive discharges spanning Alcator C-Mod, ASDEX Upgrade, DIII-D, JET, and TCV. The device list matters, because it covers both metal-wall and carbon-wall machines. That coverage is what makes it possible to separate physics from machine-specific artifacts. I have released a portion of this dataset from Alcator C-Mod in the [**Open Density Limit Database**](https://github.com/MIT-PSFC/open_density_limit_database) (other data restricted by user agreements).

## The result

A machine-learning pipeline applied to this database identified a two-variable, dimensionless boundary in the plasma edge, dominated by effective edge collisionality. It predicts density limit disruptions substantially more accurately than the Greenwald fraction, with a false positive rate of 2.3% at 95% true positive rate against 13.4% for Greenwald, and it retains the accuracy of a far more sophisticated neural network while remaining a closed-form expression a physicist can read.

Because burning plasmas have naturally low edge collisionality from self-heating, the scaling suggests they may be able to operate at higher densities than the Greenwald limit would indicate.

## Closing the loop: control experiments

An accurate stability metric is only interesting if a machine can act on it. I earned run time at DIII-D to test exactly that. The "DL Supervisor" control scheme regulated the machine-learned risk metric in real time by lowering the density target or raising neutral-beam heating.

Density limit instabilities were reproducibly suppressed. Applying an analogous H-mode metric during a current ramp-down also avoided an H/L back-transition. These are the first demonstrations of real-time density limit avoidance using machine-learned risk metrics.

## Papers

- [Real-time avoidance of the L-mode and H-mode density limit via machine-learned stability metrics]({{ site.baseurl }}/publication/realtime-avoidance-density-limit), *Nuclear Fusion* (2026)
- [Correlation of the L-mode density limit with edge collisionality]({{ site.baseurl }}/publication/correlation-density), *Nuclear Fusion* (2025)
- Collisionality scaling of the tokamak density limit, *in preparation* (2026)
