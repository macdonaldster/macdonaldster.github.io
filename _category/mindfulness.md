---
layout: default
tag: mindfulness
permalink: "/category/mindfulness.html"
---

<h1>#{{ page.tag }} (oldest first):</h1>

<ul>
	{% assign sorted = (site.pages | sort: 'last_modified_at')  %}

	{% for p in sorted %}

		{% if p.categories contains page.tag %}
	  	 <li> <a href="{{ p.url | absolute_url }}">{{ p.title }} | {{ p.last_modified_at | date: "%Y-%m-%d" }} </a></li>
		{% endif %}

 	{% endfor %}
	</ul>



