---
layout: default
title: ... home
date: 2020-01-29
last_modified_at: 2020-01-29 06:54 -6
---
<div class="blurb">
	<h1>Hi there, I'm Scott MacDonald!</h1>	
	<p>Going to create a personal site instead of a blog, I guess.</p>	

	<p>Notes:
		<ul>
			<li>I thought I would stick this link here to remind me why and how to journal - <a href="https://dariusforoux.com/how-to-journal/">https://dariusforoux.com/how-to-journal/</a></li>
			<li>Mood as of 2020-02-06 - Spring? Where are you?</li>
			<li>Currently watching - Disenchantment, Uncut Gems (30 minutes or so left)</li>
			<li>Currently attempting - 265 lbs (at 272.1, right now - 2020-02-06) ... See <a href="/pages/2020-01-28-blog.html">2020-01-28-blog</a> for more info...</li>
			<li>Current reading - the new William Gibson novel: <a href="https://en.wikipedia.org/wiki/Agency_(novel)">Agency</a>. </li>
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
