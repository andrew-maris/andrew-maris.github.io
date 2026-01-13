---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Experience
======
**DOE Fusion Energy Sciences Postdoctoral Fellow**, Columbia University, New York, NY (2026 - Present)

Principle Investigator: Prof. Carlos Paz-Soldan

The fellowship award is aimed to expand the breadth, depth, and speed of modeling tools for inductively-induced currents in magnetic fusion devices. In particular, I will increase: 
* *breadth* by modeling eddy currents due to plasma transients in multiple magnetic
fusion devices (ex. stellarators, mirrors) using the ThinCurr code.
* *depth* by coupling ThinCurr to an extended MHD code (M3D-C1 or NIMROD)
to enable self-consistent simulations of the tokamak current quench and accompanying
vertical displacement event.
* *speed* by developing accelerated models of forces experienced by
tokamaks and stellarators via machine learning surrogates and reduced-order
models.

**MIT Plasma Science and Fusion Center**, Cambridge, MA (2020 - 2026)
  
Advisors: Drs. Cristina Rea, Robert Granetz, and Earl Marmar

My thesis research combined a multimachine database study and real-time control experiments at DIII-D to both elucidate and control the tokamak density limit.

* At the heart of the analysis is a multi-machine database I constructed including 150+ L-mode density limits (LDLs), 70+ H-mode density limits (HDLs), and 3,000+ non-disruptive shots from Alcator C-Mod, ASDEX-Upgrade, DIII-D, and TCV. I then created a machine learning pipeline that identified a novel scaling for the precursor to the LDL, ν<sub>\*,edge</sub>β<sup>-0.4</sup><sub>T,edge</sub>. This scaling outperforms others (ex. Greenwald fraction, Giacomin-Ricci scaling) as an LDL warning metric (Maris et al., NF 2024)
* I earned PhD runtime at DIII-D to test real-time feedback control on this metric as an LDL avoidance solution. This control scheme successfully avoided LDL disruptions in 16 of 17 shots across 4 run days
* Additionally, I analyzed the impact of disruptions on the economics of tokamak power plants, finding that the long warming/cooling cycles of the magnets and cryostat make unscheduled maintenance extremely costly (Maris et al., FS&T 2024)
* A future publication is planned on the topic of the HDL and LDL, including an expanded database with experiments from JET and the DIII-D negative triangularity campaign

<!-- * **National Ignition Facility (NIF) Summer Scholar**, Lawrence Livermore National Laboratory (Summer 2019 & 2020)
  * Developed machine learning models to predict neutron yield of inertial confinement fusion experiments at the NIF and provide an insight into yield degradation mechanisms
  * Supervisor: Dr. Shahab Khan -->

Education
======
* **Massachusetts Institute of Technology**, Cambridge, MA (2020 - 2026)
  * Ph.D. in Applied Plasma Physics, Department of Nuclear Science and Engineering
  * _Thesis title_: Prediction and control of the tokamak density limit
  * _Advisors_: Drs. Cristina Rea, Robert Granetz, and Earl Marmar
* **Carleton College**, Northfield, MN (2015 - 2019)
  * B.A. in Physics (*Distinction*), minor in Public Policy 

Publications and preprints
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Awards and Leadership
======
* DOE Fusion Energy Sciences Postdoctoral Fellowship (2026)
* President and founding member, [Fusion Student Delegation (FuSD)](https://www.fusiondelegation.org/)