---
layout: page
title: A detailed journey
description: Daily record and sharing of Li Wuqiong's work, study and life 
permalink: /Daily/

---

Daily record and sharing of my work, study and life. Let's see how far I could walk towards my goal of becoming an entrepreneur, developer, writer and researcher.

<!-- Here I document my experiments, thoughts, and analyses on a variety of topics.
This page also includes my study notes on books I read or courses I follow. I
hope my notebook helps you as much as it has helped me. -->

<ul>
  {% for post in site.categories.daily %}
    <li>
        <span>{{ post.date | date_to_string }}</span> » {% if post.highlight %}&starf; {% endif %}<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title | truncate:72 }}</a>
    </li>
  {% endfor %}
</ul>
