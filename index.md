---
layout: default
title: ... home
date: 2020-08-12
last_modified_at: 2020-08-12 06:54 -6
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
			<li>The phrase "isn't there anything faster than a microwave" from The Simpons crosses my mind between 1 and 20 times a day.</li>
			<li>Why are we still designing new styles of pants? After all this time, shouldn't we have figured that out?</li>
		</ul>
	</p>

	<h2>Blogs (last updated, first):</h2>
	<ul>
	{% assign sorted = (site.pages | sort: 'last_modified_at') | reverse | where_exp:"p", "p.title contains '2020'" %}
	{% for p in sorted %}
	  	 <li> <a href="{{ p.url | absolute_url }}">{{ p.title }} | {{ p.last_modified_at | date: "%Y-%m-%d" }} </a></li>
 	{% endfor %}
	</ul>



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
