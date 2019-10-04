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
			<li>Currently watching - Top Boy: Summerhouse (Netflix)</li>
			<li>Currently attempting - 265 lbs (at 270, right now - 2019-10-01)</li>
			<li>Trump is a moron (Ukraine) - he clearly released the call transcript because he didn't explicitly come out and say "give us dirt, or Putin is going to roll all over you". However, there is SO MUCH MORE evidence. So much more. He's such an idiot. He keeps saying it was a "perfect call" because he wants that to the be only thing you think matters. So stupid. And yet, there he is. President. Wow. This is what happens to a country when you radically underfund public education for generations.</li>
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
