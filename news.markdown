---
title: News
date: 2018-02-28 12:44:00 Z
permalink: "/news/"
---

{% for post in site.posts %}
<article>
  <small>{{ post.date | date: "%B %e, %Y" }}</small>
  <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
</article>
{% endfor %}