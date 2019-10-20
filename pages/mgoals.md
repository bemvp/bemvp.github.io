---
layout: page
title: mgoals
description: 我的月目标
keywords: mouth-goals, 月目标
comments: false
menu: mgoals
permalink: /mgoals/
---

> **我的月目标**

<ul class="listing">
{% for mgoals in site.mgoals %}
{% if mgoals.title != "Mgoals Template" %}
<li class="listing-item"><a href="{{ site.url }}{{ mgoals.url }}">{{ mgoals.title }}</a></li>
{% endif %}
{% endfor %}
</ul>
