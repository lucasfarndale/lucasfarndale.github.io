---
layout: page
permalink: /publications/
title: Publications
description: Peer-reviewed papers and preprints, in reverse chronological order. Citation counts are from <a href="https://scholar.google.com/citations?user=xYlqtP4AAAAJ">Google Scholar</a> (November 2026). Papers marked <em>Preprint</em> have not yet been peer reviewed.
years: [2026, 2025, 2024, 2023]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
