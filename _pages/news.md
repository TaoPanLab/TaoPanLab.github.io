---
layout: page
permalink: /news/
title: News
nav: true
nav_order: 1
groups : [Mar, Feb, Jan]
---

All news are listed in reversed chronological order.

{% assign postsByYearMonth = site.news | group_by_exp:"item", "item.date | date: '%Y %b'"  %}
{% for yearMonth in postsByYearMonth %}
  <h3>{{ yearMonth.name }}</h3>
    <ul>
      {% for post in yearMonth.items %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
      {% endfor %}
    </ul>
{% endfor %}



