---
layout: page
title: 月目标
description: 我的月目标
keywords: mouth-goals 月目标
comments: false
menu: 维基
permalink: /mouth-goals/
---

> 记多少命令和快捷键会让脑袋爆炸呢？

<ul class="listing">
{% for mouth-goals in site.mouth-goals %}
{% if mouth-goals.title != "mouth-goals Template" %}
<li class="listing-item"><a href="{{ site.url }}{{ mouth-goals.url }}">{{ mouth-goals.title }}</a></li>
{% endif %}
{% endfor %}
</ul>