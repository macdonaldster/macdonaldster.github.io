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
			<li>I just decommissioned my linode vps, saving about $10 USD a month.</li>
			<li>I backed up my writefreely blog posts to a JSON file in this repo in case I want to ressurect any posts as "articles" here.</li>
			<li>This site will just be free-form, whatever I feel like writing about. No pressure to "blog". No structure, no outline, just some HTML docs online.</li>
		</ul>
	</p>

	<h2>Pages (last updated, first):</h2>
	<ul>
	{% assign sorted = (site.pages | sort: 'last_modified_at') | reverse %}
	{% for p in sorted %}
		{% if p.categories != [] %}
	  	 <li> <a href="{{ p.url | absolute_url }}">{{ p.title }} | {{ p.date }}</a></li>
		{% endif %}
 	{% endfor %}
	</ul>

</div><!-- /.blurb -->
