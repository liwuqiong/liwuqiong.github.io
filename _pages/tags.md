---
layout: page
title: Tag Directory
---

All blog posts, grouped by tags.

{% assign tags = site.tags | sort %}

{% for tag in tags %}
  - [{{ tag[0] }}](#{{ tag[0] | slugify }}) ({{ tag[1].size }})
{% endfor %}

{% for tag in tags %}
<h3 id="{{ tag[0] | slugify }}">#{{ tag[0] }}</h3>

{% for post in tag[1] %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% endfor %}


<!-- 以上代码是通过chagpt一点点问出来的。
背景是该模板自带的tag插件功能发布在Github pages上后无法使用，因为Github pages出于某些安全原因考虑不允许使用第三方插件。

无奈做了个变通的手段，即写了一个标签页面，可以实现标签列表目录、数量，以及各个标签下的文章链接，在该页面内可以实现跳转。

 -->


<!-- 基础代码

All blog posts, grouped by tags.

{% assign tags = site.tags | sort %}

{% for tag in tags %}
<h3>#{{ tag[0] }}</h3>

{% for post in tag[1] %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% endfor %} -->


<!-- 只筛选出特定某个标签的文章，可用于创建新的主题页面

{% assign specific_tag = "descipline" %}

<h2>Blog posts with tag: #{{ specific_tag }}</h2>

{% for post in site.tags[specific_tag] %}
- [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %} -->