---
layout: page
permalink: /publications/
title: publications
description: Here are my publications by categories in reversed chronological order.
journals_years: [2021, 2020]
conferences_years: [2020, 2019, 2018]
nav: true
---

<div class="publications">

<H1>Journals</H1>

{% for y in page.journals_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

<H1>Conferences</H1>

{% for y in page.conferences_years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f conferences -q @*[year={{y}}]* %}
{% endfor %}

</div>