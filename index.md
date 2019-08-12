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
			<li>Lately, I feel like I am going crazy. I feel like we are stuck in the world where the show Scandal takes place. The Epstein thing... it's so in your face. Just brazenly taken out before he could be compelled to testify. Or, maybe, he really did do this himself. How will we ever know? It just seems like the onslaught of crazy news never ends. It started really going nuts when Trump was elected and keeps accellerating. Where does it stop? How can it keep getting crazier? We're try to raise a kid over here.
			<a href="http://imoviequotes.com/wp-content/uploads/2015/02/1-Midnight-Cowboy-quotes.gif" />
			
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
