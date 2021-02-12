---
layout: page
permalink: /publications/
title: Publications
description: Below you can find the list of my latest publications that might not be listed yet in public repositories <a style="color:green" href="https://dblp.uni-trier.de/pid/145/3999.html">[DBLP]</a> <a style="color:green" href="https://scholar.google.com/citations?user=PNagLbIAAAAJ&hl=it&oi=ao"> [Schoolar]</a> .
years: [2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012]
---

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
