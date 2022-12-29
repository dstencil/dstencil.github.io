---
layout: page
title: Cheatsheets
permalink: /cheatsheets/
---

<ul>
  {% for post in site.posts %}
    {% if post.tags contains 'kubernetes' %}  
        <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        </li>
    {% endif %}    
  {% endfor %}
</ul>