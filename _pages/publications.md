---
layout: page
permalink: /experiences/
title: Experiences
description: 
yearsa: [2022,2021,2019]
yearsb: [2022,2020,2019]
types: [work, edu]
nav: true
---

Know more about my experiences via [LinkedIn](https://www.linkedin.com/in/maqliu/).

<div class="publications">
<h2 class="category">Work Experiences</h2>
{% for y in page.yearsa %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>

<div class="publications">
<h2 class="category">Education</h2>
{% for y in page.yearsb %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers1 -q @*[year={{y}}]* %}
{% endfor %}

</div>
