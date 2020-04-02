
---
layout: archive
title: COVID19
date: 2020-04-01
last_modified_at: 2020-04-01 15:00 -6
---

{% for category in site.categories %}
  <h3>{{ category[0] }}</h3>
  <ul>
    {% for post in category[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}