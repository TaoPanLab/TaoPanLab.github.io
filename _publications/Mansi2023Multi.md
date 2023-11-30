---
layout: post
date: 2023-04-28 15:59:00-0400
inline: true
bibliography: "_bibliography/papers.bib"
---

{% assign entry = site.data.papers[Mansi2023Multi] %}

{% bibliography -f papers -q @*[key='Mansi2023Multi']* %}

The authors of this entry are {% for author in entry.author %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}.


Another stuff

{% assign myKeyData = site.data.papers[Mansi2023Multi] %}

{% if myKeyData %}
  <p>Authors: {{ myKeyData.author | join: ', ' }}</p>
  <p>Title: {{ myKeyData.title }}</p>
{% else %}
  <p>Key not found</p>
{% endif %}


{% assign my_paper_key = "Mansi2023Multi" %}

{% bibliography %}
{% assign paper_entry = site.data.scholar.bibliography[my_paper_key] %}

<h2>{{ paper_entry.author }}</h2>
<p>{{ paper_entry.title }}</p>


{% cite Mansi2023Multi %}.

References
----------

{% bibliography %}