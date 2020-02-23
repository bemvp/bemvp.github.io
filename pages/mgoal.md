---
layout: page
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
{% assign sorted_mgoal = site.mgoal | sort %}
{% for mgoal in sorted_mgoal %}
<h3>{{ mgoal | first }}</h3>
<ol class="mgoal-list" id="{{ mgoal[0] }}">
{% for mgoal in mgoal.last %}
<li class="mgoal-list-item">
<span class="mgoal-list-meta">{{ mgoal.date | date:"%Y-%m-%d" }}</span>
<a class="mgoal-list-name" href="{{ site.url }}{{ mgoal.url }}">{{ mgoal.title }}</a>
</li>
{% endfor %}
</ol>
{% endfor %}
</section>
<!-- /section.content -->

