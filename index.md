---
layout: default
title: ... home
date: 2019-07-01
last_modified_at: 2019-07-20 06:54 -6
---
<div class="blurb">
	<h1>Hi there, I'm Scott MacDonald!</h1>	
	<p>Going to create a personal site instead of a blog, I guess.</p>	

	<p>Notes:
		<ul>
			<li>Lately I have been watching a lot of van conversion videos: <a href="https://www.youtube.com/watch?v=3YcD5XJNzkM">https://www.youtube.com/watch?v=3YcD5XJNzkM</a>
			</li>

			<li>
			Recognized Lake Banook in the intro of the Canadian Amazing Race tonight. :)
			</li>

		</ul>
	</p>

	<h2>Pages (last updated, first):</h2>
	<ul>
	{% assign sorted = (site.pages | sort: 'last_modified_at') | reverse %}
	{% for p in sorted %}
		{% if p.categories != [] %}
	  	 <li> <a href="{{ p.url | absolute_url }}">{{ p.title }} | {{ p.last_modified_at | date: "%Y-%m-%d" }} </a></li>
		{% endif %}
 	{% endfor %}
	</ul>

</div><!-- /.blurb -->
