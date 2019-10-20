---
layout: page
title: Mgoal
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
{% for mgoal in site.mgoals %}
{% if mgoal.title != "Mgoal Template" %}
<li class="listing-item"><a href="{{ site.url }}{{ mgoal.url }}">{{ mgoal.title }}</a></li>
{% endif %}
{% endfor %}
</ul>

