---
layout: page
permalink: /news/
title: News
nav: true
nav_order: 1
groups : [mar23, feb23, jan23]
---

All news are listed in reversed chronological order.

<!-- _pages/news.md -->

{%- for g in page.groups %}
  <h2 class="year">{{g}}</h2>
  {%- assign news = site.news | reverse -%}
  {% assign n = news | where_exp:"item", "item.group == g" %}
    <table class="table table-sm table-borderless">
              {% for item in n %}
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
              {%- endfor %}
              </table>
{% endfor %}



