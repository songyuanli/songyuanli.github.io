---
layout: page
description: 
years: [2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017]
---

<h1 style="text-align: center;color: #003c3c;">Publications</h1>

Click <a href="https://scholar.google.com/citations?user=cESBqqkAAAAJ">here</a> to see <b>my Google Scholar profile</b>.

<h4 style="font-weight: normal;">Journal and conference rankings are based on <a href="https://www.core.edu.au/conference-portal">CORE (The Computing Research and Education Association of Australasia)</a>.</h4>
<li> Journal: A+: top 7%, A: top 17%;</li>
<li> Conferences: A+: top 4%, A: top 14%.</li>



<div class="publications">

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>

