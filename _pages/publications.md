---
title: "Publications"
layout: home
permalink: /publications/
author_profile: false
---

<div class="hero" style="padding-bottom:1.6em">
  <span class="hero__eyebrow">Publications</span>
  <h1 class="hero__title" style="font-size:2em">Papers and preprints</h1>
  <p class="hero__lede">Also on <a href="{{ site.author.googlescholar }}">Google Scholar</a> and <a href="{{ site.author.orcid }}">ORCID</a>.</p>
</div>

<p class="section-label">First and co-first author</p>
<div class="entries">
{% assign firstauthor = site.publications | where_exp: "p", "p.firstauthor" | sort: "date" | reverse %}
{% for post in firstauthor %}{% include entry-publication.html %}{% endfor %}
</div>

<p class="section-label">Co-authored</p>
<div class="entries">
{% assign coauthored = site.publications | where_exp: "p", "p.firstauthor != true" | sort: "date" | reverse %}
{% for post in coauthored %}{% include entry-publication.html %}{% endfor %}
</div>
