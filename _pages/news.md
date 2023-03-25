---
layout: news
permalink: /news/
title: News
nav: true
nav_order: 1
groups : [jan23, feb23, mar23]
---

All news are listed in reversed chronological order.

<!-- _pages/news.md -->
<div class="publications">

{%- for g in page.groups %}
  <h2 class="year">{{g}}</h2>
  {%- assign news = site.news | reverse -%}
  {%- news | where_exp:"item",
"item.group == g" -%}
{% endfor %}

</div>

