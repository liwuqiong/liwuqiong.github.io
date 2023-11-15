---
layout: page
title: Tags
---

{% assign sorted_tags = site.tags | sort %}
{% for tag in sorted_tags %}
  - [{{ tag[0] }}]({{ site.baseurl }}/tag/{{ tag[0] }}) ({{ tag[1].size }})
{% endfor %}