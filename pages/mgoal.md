---
layout: pages
title: mouth-goals
description: 我的月目标
keywords: mouth-goals, 月目标
comments: false
menu: mgoal
permalink: /mgoal/
---

> **我的月目标**

> God made relatives. Thank God we can choose our friends.
> 
<ul class="listing">
{% for mgoal in site.mgoal %}
{% if mgoal.title != "Mgoal Template" %}
<li class="listing-item"><a href="{{ site.url }}{{ mgoal.url }}">{{ mgoal.title }}</a></li>
{% endif %}
{% endfor %}
</ul>

<section class="container mgoal-content">
{% assign sorted_categories = site.categories | sort %}
{% for category in sorted_categories %}
<h3>{{ category | first }}</h3>
<ol class="mgoal-list" id="{{ category[0] }}">
{% for mgoal in category.last %}
<li class="mgoal-list-item">
<span class="mgoal-list-meta">{{ mgoal.date | date:"%Y-%m-%d" }}</span>
<a class="mgoal-list-name" href="{{ site.url }}{{ mgoal.url }}">{{ mgoal.title }}</a>
</li>
{% endfor %}
</ol>
{% endfor %}
</section>
<!-- /section.content -->

