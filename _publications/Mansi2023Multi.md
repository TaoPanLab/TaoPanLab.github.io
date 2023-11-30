---
layout: post
date: 2023-04-28 15:59:00-0400
inline: true
bibliography: "_bibliography/papers.bib"
---

{% assign entry = site.data.papers[Mansi2023Multi] %}

{% bibliography -f papers -q @*[key='Mansi2023Multi']* %}

The authors of this entry are {% for author in entry.author %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}.


{% cite Mansi2023Multi %}.

References
----------

{% bibliography %}