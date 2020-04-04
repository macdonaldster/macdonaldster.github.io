---
layout: default
title: ... home
date: 2020-01-29
last_modified_at: 2020-01-29 06:54 -6
---

<div class="blurb">
	<h1>Latest page: {% assign sorted = (site.pages | sort: 'last_modified_at') | reverse %}
	{% for p in sorted limit:1 %}
	  	 <a href="{{ p.url | absolute_url }}">{{ p.title }}</a>
 	{% endfor %}
	 </h1>

	<p>Notes:
		<ul>
		<li>I added category pages to this site so now can refer you to the <a href="/category/covid19.html">COVID19</a> page where I am collecting thoughts on life during this pandemic. </li>
			<li>I thought I would stick this link here to remind me why and how to journal - <a href="https://dariusforoux.com/how-to-journal/">https://dariusforoux.com/how-to-journal/</a></li>
			<li>Mood as of 2020-04-03 - Sick of this Winter, need some spring weather...</li>
			<li>Currently watching - Godless (Netflix)</li>
			<li>Currently attempting - 265 lbs (gained it back from stress eating! starting again)</li>
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
