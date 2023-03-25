---
layout: page
permalink: /news/
title: News
nav: true
nav_order: 1
---

All news are listed in reversed chronological order.

<div class="publications">
    {% assign postsByYearMonth = site.news | group_by_exp:"item", "item.date | date: '%b %Y'" | reverse %}
    {% for yearMonth in postsByYearMonth %}
      <h2 class="year">{{ yearMonth.name }}</h2>
        <ol class="bibliography">
            {%- assign news = yearMonth.items | reverse -%}
            {% for item in news %}
                <li>
                    <div class = "row">
                        <div class="col-sm-2">
                            {{ item.date | date: "%b %-d, %Y" }}
                        </div>
                        <div class="col-sm-8">
                            {% if item.inline -%}
                              {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
                            {%- else -%}
                              <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
                            {%- endif %}
                        </div>
                    </div>
                </li>
          {% endfor %}
        </ol>
    {% endfor %}
</div>


