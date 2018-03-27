---
title: News
date: 2018-02-28 12:44:00 Z
permalink: "/news/"
---

{% for post in site.posts %}
<article class="post">
  <p class="date">{{ post.date | date: "%B %e, %Y" }}</p>
  <a href="{{ post.url }}" title="{{ post.title }}">
    <h3>{{ post.title }}</h3>
  </a>
</article>
{% endfor %}