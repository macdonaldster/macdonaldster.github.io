---
layout: default
title: ... home
date: 2019-07-01
last_modified_at: 2019-09-03 06:54 -6
---
<div class="blurb">
	<h1>Hi there, I'm Scott MacDonald!</h1>	
	<p>Going to create a personal site instead of a blog, I guess.</p>	

	<p>Notes:
		<ul>
			<li>Currently watching - The Mandalorian on Disney+</li>
			<li>Currently attempting - 265 lbs (at 275, right now - 2019-12-09) ... Efforts have failed. Redoubling. :)</li>
			<li>Current mood - wow, what is going on in the US? Feeling lucky for many, many aspects of my life.</li>
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
