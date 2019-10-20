---
layout: page
title: mgoals
description: 我的月目标
keywords: mouth-goals, 月目标
comments: false
menu: mgoal
permalink: /mgoal/
---

> **我的月目标**

<ul class="listing">
{% for mgoal in site.mgoal %}
{% if mgoal.title != "Mgoal Template" %}
<li class="listing-item"><a href="{{ site.url }}{{ mgoal.url }}">{{ mgoal.title }}</a></li>
{% endif %}
{% endfor %}
</ul>

