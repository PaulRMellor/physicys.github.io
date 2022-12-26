---
layout: default
title: Tags
---

{% include group-by-array.html %}

{% assign docs_by_tags = site.documents | group_by: 'tags' %}
{% for tag in docs_by_tags %}
<h2>{{ tag.name }}</h2>
<ul>
    {% for item in tag.items %}
    <li><a href="{{ item.url }}">{{ item.title }}</a></li>
    {% endfor %}
</ul>
{% endfor %}

