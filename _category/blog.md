---
layout: default
permalink: "/category/blog.html"
---

<h2>Pages (last updated, first):</h2>
Test5
{% comment %}

<ul>
	{% assign sorted = (site.pages | sort: 'last_modified_at') | reverse %}
	{% for p in sorted %}
		{% if p.categories contains "covid19" %}
	  	 <li> <a href="{{ p.url | absolute_url }}">{{ p.title }} | {{ p.last_modified_at | date: "%Y-%m-%d" }} </a></li>
		{% endif %}
 	{% endfor %}
	</ul>

{% endcomment %}
