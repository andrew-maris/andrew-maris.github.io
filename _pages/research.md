---
title: "Research"
layout: home
permalink: /research/
author_profile: false
---

<div class="hero" style="padding-bottom:1.8em">
  <span class="hero__eyebrow">Research</span>
  <h1 class="hero__title" style="font-size:2em">Three threads, one problem.</h1>
  <p class="hero__lede">Fusion devices fail in ways that are predictable in principle and costly in practice. I work on modeling what those failures do to the machine, on seeing them coming early enough to steer away, and on asking what all of this is worth to the future of fusion energy.</p>
</div>

<div class="threads">
  {% assign threads = site.research | sort: "order" %}
  {% for post in threads %}
    {% include archive-single-research.html %}
  {% endfor %}
</div>
