---
layout: page
permalink: /publications/
title: Publications
years: [2023, 2022, 2021, 2020, 2019, 2018, 2017]
nav: true
showbib: true
nav_order: 2
---
All publications are listed in reversed chronological order.

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
