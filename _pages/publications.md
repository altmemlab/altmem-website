---
layout: page
permalink: /publications/
title: papers
description:
nav: true
nav_order: 3
_styles: >
  .publications h2.bibliography {
    color: rgba(0, 0, 0, 0.25);
    border-top-color: rgba(0, 0, 0, 0.25);
  }
  html[data-theme="dark"] .publications h2.bibliography {
    color: rgba(255, 255, 255, 0.25);
    border-top-color: rgba(255, 255, 255, 0.25);
  }
  .preprints .periodical-date {
    display: none;
  }
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

<u>lab member</u><br>
<sup>*†</sup> equal contribution

{% include bib_search.liquid %}

<div class="publications">

{% capture preprint_count %}{% bibliography_count --file preprints %}{% endcapture %}
{% assign preprint_count = preprint_count | plus: 0 %}
{% if preprint_count > 0 %}

<h2 class="bibliography">preprints</h2>

<div class="preprints">

{% bibliography --file preprints --group_by none %}

</div>

{% endif %}

{% bibliography %}

</div>
