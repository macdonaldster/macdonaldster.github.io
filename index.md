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
			<li>Currently watching - ... nothing? Top Boy: Summerhouse (Netflix) got too dark for me, can only watch little kids getting forced into drug dealing for so long before it gets very hard to watch; reminds of The Wire without the police aspect.</li>
			<li>Currently attempting - 265 lbs (at 270, right now - 2019-10-01) ... this is going poorly. :)</li>
			<li>You know what might be fun? If we enjoy what we have, and stop trying to get more if we have enough. That might help the world be a better place.</li>
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
