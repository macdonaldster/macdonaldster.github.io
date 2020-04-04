---
layout: default
permalink: "/category/blog.html"
---

<h2>Pages (last updated, first):</h2>
Test5

<ul>
	{% assign sorted = (site.pages | sort: 'last_modified_at') | reverse %}

	{% for p in sorted %}
		{% comment %}
		{% if p.categories contains "covid19" %}
	  	 <li> <a href="{{ p.url | absolute_url }}">{{ p.title }} | {{ p.last_modified_at | date: "%Y-%m-%d" }} </a></li>
		{% endif %}
		{% endcomment %}
 	{% endfor %}
	</ul>




