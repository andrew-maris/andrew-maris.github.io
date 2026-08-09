---
title: "CV"
layout: home
permalink: /cv/
author_profile: false
redirect_from:
  - /resume
---

{% include base_path %}

<div class="hero" style="padding-bottom:1.6em">
  <span class="hero__eyebrow">Curriculum vitae</span>
  <h1 class="hero__title" style="font-size:2em">Andrew D. Maris</h1>
  <p class="hero__lede">New York, NY &nbsp;·&nbsp; {{ site.author.email }} &nbsp;·&nbsp; <a href="{{ site.author.googlescholar }}">Google Scholar</a> &nbsp;·&nbsp; <a href="{{ site.author.orcid }}">ORCID</a></p>
</div>

<div class="cv" markdown="1">

## Research

### DOE Fusion Energy Sciences Postdoctoral Fellow
<p class="cv__where">Columbia University, New York, NY &nbsp;·&nbsp; 2026 – present &nbsp;·&nbsp; Supervisor: Prof. Carlos Paz-Soldan</p>

Expanding the breadth, depth, and speed of modeling tools for inductively-induced currents in magnetic fusion devices.

* *Breadth*: modeling eddy currents from plasma transients across multiple device classes, including stellarators and mirrors, using the ThinCurr code
* *Depth*: coupling ThinCurr to an extended MHD code (M3D-C1 or NIMROD) for self-consistent simulation of the current quench and the accompanying vertical displacement event
* *Speed*: developing accelerated, differentiable models of the forces experienced by tokamaks and stellarators via machine learning surrogates and reduced-order models

### PhD research, MIT Plasma Science and Fusion Center
<p class="cv__where">Cambridge, MA &nbsp;·&nbsp; 2020 – 2026 &nbsp;·&nbsp; Advisors: Cristina Rea, Robert Granetz, and Earl Marmar</p>

A multi-machine database study combined with real-time control experiments at DIII-D, aimed at both explaining and controlling the tokamak density limit.

* Built a comprehensive multi-machine density limit database: 258 L-mode density limits, 90 H-mode density limits, and 4,739 non-disruptive discharges spanning Alcator C-Mod, ASDEX Upgrade, DIII-D, JET, and TCV. Released publicly as the [Open Density Limit Database](https://github.com/MIT-PSFC/open_density_limit_database)
* Created a machine learning pipeline that identified simple, dimensionless power laws predicting density limit onset more accurately than the Greenwald fraction, providing evidence for a theorized RBM-destabilization mechanism (*NF* 2025; in preparation 2026)
* Demonstrated real-time avoidance of the density limit on DIII-D via feedback control of the machine-learned stability metrics (*NF* 2026)
* Quantified the economic consequences of disruptions in tokamak power plants, showing cryogenic system recovery time to be a potentially dominant cost driver (*FS&T* 2024)

### Quantum Chaos Research Assistant
<p class="cv__where">Carleton College, Northfield, MN &nbsp;·&nbsp; 2017 – 2019</p>

* Characterized the convergence of the Duffing oscillator's dynamical complexity in the semiclassical regime via numerical simulation (*PRE* 2021)

## Education

### Massachusetts Institute of Technology
<p class="cv__where">PhD in Applied Plasma Physics, Department of Nuclear Science and Engineering &nbsp;·&nbsp; February 2026</p>

* *Thesis*: Prediction and control of the tokamak density limit
* *Advisors*: Cristina Rea, Robert Granetz, and Earl Marmar

### Carleton College
<p class="cv__where">B.A., Northfield, MN &nbsp;·&nbsp; June 2019</p>

* Major in Physics (*Distinction*), minor in Public Policy

## Industry experience & research internships

### Associate Photonics Engineer
<p class="cv__where">L3Harris Technologies, Palm Bay, FL &nbsp;·&nbsp; September 2019 – June 2020</p>

* Programmed a quantum computing demonstration for an aerospace optimization problem
* Lead author of an R&D funding request for an adiabatic quantum computing project

### National Ignition Facility Summer Scholar
<p class="cv__where">Lawrence Livermore National Laboratory, Livermore, CA &nbsp;·&nbsp; Summers 2019 &amp; 2020</p>

* Developed machine learning models to predict neutron yield of inertial confinement fusion experiments at NIF and to identify yield degradation mechanisms (*PoP* 2023)

</div>

<div class="cv">

<h2>Publications</h2>
<div class="entries">
{% assign pubs = site.publications | sort: "date" | reverse %}
{% for post in pubs %}{% include entry-publication.html %}{% endfor %}
</div>

<h2>Invited talks</h2>
<div class="entries">
{% assign all = site.talks | sort: "date" | reverse %}
{% for post in all %}{% if post.type == "Invited talk" %}{% include entry-talk.html %}{% endif %}{% endfor %}
</div>

<h2>Contributed talks</h2>
<div class="entries">
{% for post in all %}{% if post.type == "Contributed talk" %}{% include entry-talk.html %}{% endif %}{% endfor %}
</div>

<h2>Seminars and outreach</h2>
<div class="entries">
{% for post in all %}{% if post.type == "Guest seminar" or post.type == "Outreach talk" %}{% include entry-talk.html %}{% endif %}{% endfor %}
</div>

<h2>Posters</h2>
<div class="entries">
{% for post in all %}{% if post.type == "Poster" %}{% include entry-talk.html %}{% endif %}{% endfor %}
</div>

<h2>Teaching</h2>
<div class="entries">
{% assign teach = site.teaching | sort: "date" | reverse %}
{% for post in teach %}{% include entry-teaching.html %}{% endfor %}
</div>

</div>

<div class="cv" markdown="1">

## Awards

* **DOE Fusion Energy Sciences Postdoctoral Fellowship**, July 2025
* **Outstanding Poster Award**, 13th ITER International School, Nagoya, Japan, December 2024
* **Distinction in Physics**, Carleton College, 2019

## Service and leadership

### President and Co-Founder, Fusion Student Delegation
<p class="cv__where">Washington, DC &nbsp;·&nbsp; 2023 – 2025 (Vice President 2024, President 2025)</p>

* Founded a national graduate-student delegation connecting early-career fusion scientists with policymakers in Washington
* Organized the schedule for the inaugural visit, including meetings with DOE FES Director J.P. Allain and Nuclear Regulatory Commissioner Chris Hansen
* Led recruitment and governance design for the national program; the 2025 cohort drew 60 applicants for 10 slots

</div>
