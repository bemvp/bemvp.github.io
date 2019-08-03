---
layout: page
title: 月目标
description: 我的月目标
keywords: mouth-goals, 月目标
comments: false
menu: mgoals
permalink: /mgoals/
---

> 记多少命令和快捷键会让脑袋爆炸呢？

<ul class="listing">
{% for mgoal in site.mgoals %}
{% if mgoal.title != "Mgoals Template" %}
<li class="listing-item"><a href="{{ site.url }}{{ mgoal.url }}">{{ mgoal.title }}</a></li>
{% endif %}
{% endfor %}
</ul>