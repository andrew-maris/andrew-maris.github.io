---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* **Massachusetts Institute of Technology**, Cambridge, MA (2020 - Present)
  * Ph.D. in Applied Plasma Physics, Department of Nuclear Science and Engineering
  * _Provisional thesis title_: Prediction and avoidance of the tokamak density limit via interpretable machine learning 
  * _Advisors_: Drs. Cristina Rea, Robert Granetz, and Earl Marmar
* **Carleton College**, Northfield, MN (2015 - 2019)
  * B.A. in Physics (*Distinction*), minor in Public Policy 


Research experience
======
**MIT Plasma Science and Fusion Center**, Cambridge, MA (September 2020 - August 2025)
  
Advisors: Cristina Rea, Robert Granetz, and Earl Marmar

My thesis research combines a multimachine database study and real-time control experiments at DIII-D to both elucidate and control the tokamak density limit.

* At the heart of the analysis is a multi-machine database I constructed including 150+ L-mode density limits (LDLs), 70+ H-mode density limits (HDLs), and 3,000+ non-disruptive shots from Alcator C-Mod, ASDEX-Upgrade, DIII-D, and TCV. I then created a machine learning pipeline that identified a novel scaling for the precursor to the LDL, ν<sub>\*,edge</sub>β<sup>-0.4</sup><sub>T,edge</sub>. This scaling outperforms others (ex. Greenwald fraction, Giacomin-Ricci scaling) as an LDL warning metric (Maris et al., NF 2024)
* I earned PhD runtime at DIII-D to test real-time feedback control on this metric as an LDL avoidance solution. This control scheme successfully avoided LDL disruptions in 16 of 17 shots across 4 run days
* Additionally, I analyzed the impact of disruptions on the economics of tokamak power plants, finding that the long warming/cooling cycles of the magnets and cryostat make unscheduled maintenance extremely costly (Maris et al., FS&T 2024)
* A future publication is planned on the topic of the HDL and LDL, including an expanded database with experiments from JET and the DIII-D negative triangularity campaign

<!-- * **National Ignition Facility (NIF) Summer Scholar**, Lawrence Livermore National Laboratory (Summer 2019 & 2020)
  * Developed machine learning models to predict neutron yield of inertial confinement fusion experiments at the NIF and provide an insight into yield degradation mechanisms
  * Supervisor: Dr. Shahab Khan -->

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
  
Leadership
======
* President and founding member, [Fusion Student Delegation (FuSD)](https://www.fusiondelegation.org/)