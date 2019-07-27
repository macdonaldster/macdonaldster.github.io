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
			<li>Look, you can't argue with a Trump Supporter. Here's why:
				<ul>
					<li>They don't win by being right, they win by out lasting you or angering you to the point where you storm off or lose your temper.</li>
					<li>Facts don't matter. They don't care about that citation. And they know it makes you angry. Sure, they read the Mueller report! And, totally, wilfully misunderstood it. And no amount of legal scholarship about obstruction of justice is going to make a difference.</li>
					<li>They just don't care about you at all, so they don't care if you agree with them. And they don't care if they are wrong because being wrong only matters if you care about how other people see you. They don't care about that. </li>
					<li>There's more here: <a href="/pages/trump-supporters-2019-07-20.html">Trump Supporters</a></li>
				</ul>
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
