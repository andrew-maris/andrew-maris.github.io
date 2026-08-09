---
permalink: /
title: "Andrew D. Maris"
excerpt: "Understanding and taming plasma instabilities."
layout: home
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---

<div class="hero">
  <span class="hero__eyebrow">DOE FES Postdoctoral Fellow · Columbia University</span>
  <h1 class="hero__title">Understanding and taming plasma instabilities</h1>
  <p class="hero__lede">I use machine learning to find the physics hiding in tokamak databases, then put it into real-time control. Recently: the first closed-loop avoidance of the tokamak density limit, demonstrated on DIII-D.</p>
  <div class="tag-row">
    <span class="tag tag--1">MHD &amp; induced currents</span>
    <span class="tag tag--2">interpretable ML</span>
    <span class="tag tag--3">fusion economics</span>
  </div>
</div>

<div class="threads">
  <p class="threads__label">What I work on</p>
  {% assign threads = site.research | sort: "order" %}
  {% for post in threads %}
    {% include archive-single-research.html %}
  {% endfor %}
</div>

<div class="recent">
  <div>
    <p class="recent__label">Latest paper</p>
    <p class="recent__value"><a href="{{ site.baseurl }}/publication/realtime-avoidance-density-limit">Real-time avoidance of the L-mode and H-mode density limit</a><br/><span class="recent__meta">Nuclear Fusion, 2026</span></p>
  </div>
  <div>
    <p class="recent__label">Recent talk</p>
    <p class="recent__value">Collisionality scaling of the tokamak density limit<br/><span class="recent__meta">APS DPP 2025, ITER Session</span></p>
  </div>
  <div>
    <p class="recent__label">Elsewhere</p>
    <p class="recent__value"><a href="{{ site.author.googlescholar }}">Google Scholar</a> · <a href="https://github.com/{{ site.author.github }}">GitHub</a> · <a href="{{ site.author.orcid }}">ORCID</a><br/><span class="recent__meta">{{ site.author.email }}</span></p>
  </div>
</div>

<div style="margin-top:2.6em;padding-top:1.6em;border-top:1px solid #e6e6e6">
<p style="margin:0 0 1em"><strong>Dr. Andrew D. Maris</strong> is a DOE Fusion Energy Sciences Postdoctoral Fellow at Columbia University, where he works with Prof. Carlos Paz-Soldan on transient off-normal phenomena in magnetically confined fusion plasmas.</p>

<p style="margin:0 0 1em">He earned his B.A. from Carleton College in 2019 and his Ph.D. from the MIT Plasma Science and Fusion Center in 2026, advised by Cristina Rea, Robert Granetz, and Earl Marmar. His thesis, <em>Prediction and control of the tokamak density limit</em>, used machine-learning methods to understand, predict, and ultimately avoid the density limit in tokamaks.</p>

<p style="margin:0">Alongside plasma physics he works on fusion energy economics and policy, including published work on the cost of plasma disruptions to fusion power plants. He is a co-founder and former President of the <a href="https://www.fusiondelegation.org/">Fusion Student Delegation</a>, a student-led organization connecting early-career researchers with policymakers in the fusion ecosystem.</p>
</div>
