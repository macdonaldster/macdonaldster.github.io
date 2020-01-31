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
			<li>Mood as of 2020-01-31 - unseasonably warm, sunny day! feeling good... cooking some prime rib tonight - what a treat!
			<li>Currently watching - Disenchantment</li>
			<li>Currently attempting - 265 lbs (at 273, right now - 2020-01-29) ... See <a href="/pages/2020-01-28-blog.html">2020-01-28-blog</a> for more info...</li>
			<li>Current mood - I just finished a 550 piece Harry Potter puzzle we got for my son. Well, I left three pieces for him to finish in the morning because I am not a selfish jerk. I've been working on it in my free time for a while now and I love the feeling of placing each piece but am glad it is done. :)</li>
			<li>Current reading - the new Willing Gibson novel: <a href="https://en.wikipedia.org/wiki/Agency_(novel)">Agency</a>. </li>
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
