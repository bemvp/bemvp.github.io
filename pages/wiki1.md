---
layout: page
title: Wiki
description: 人越学越觉得自己无知
keywords: 维基, Wiki
comments: false
menu: 维基
permalink: /wiki/
---

> 记多少命令和快捷键会让脑袋爆炸呢？

<ul class="listing">
{% for wiki1 in site.wiki %}
{% if wiki1.title != "Wiki1 Template" %}
<li class="listing-item"><a href="{{ site.url }}{{ wiki1.url }}">{{ wiki1.title }}</a></li>
{% endif %}
{% endfor %}
</ul>
