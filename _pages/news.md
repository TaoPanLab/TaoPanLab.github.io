---
layout: page
permalink: /news/
title: News
nav: true
nav_order: 1
---

All news are listed in reversed chronological order.

{% assign postsByYearMonth = site.news | group_by_exp:"item", "item.date | date: '%Y %b'"  %}
{% for yearMonth in postsByYearMonth %}
  <h3>{{ yearMonth.name }}</h3>
    <table class="table table-sm table-borderless">
      {% for item in yearMonth.items %}
        <tr>
                  <th scope="row" class="news-date">{{ item.date | date: "%b %-d, %Y" }}</th>
                  <td>
                    {% if item.inline -%}
                      {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
                    {%- else -%}
                      <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
                    {%- endif %}
                  </td>
                </tr>
      {% endfor %}
    </table>
{% endfor %}



