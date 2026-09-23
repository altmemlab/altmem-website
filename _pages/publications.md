---
layout: page
permalink: /publications/
title: papers
description:
nav: true
nav_order: 3
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

{% bibliography --file preprints --group_by none %}

{% endif %}

{% bibliography %}

</div>
