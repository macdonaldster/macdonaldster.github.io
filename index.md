---
layout: default
title: Scott MacDonald
date: 2019-07-14
---
<div class="blurb">
	<h1>Hi there, I'm Scott MacDonald!</h1>	
	<p>Going to create a personal site instead of a blog, I guess.</p>
	<p>Pages:
<ul>

<li><a href="/pages/Lightning-2019-07-15.html">Lightning (last updated 2019-07-15)</a></li>

<li><a href="/pages/2019-07-14-organizing.html">Organizing (last updated 2019-07-15)</a></li>

</ul>
	</p>

	<p>Notes:
		<ul>
			<li>I just decommissioned my linode vps, saving about $10 USD a month.</li>
			<li>I backed up my writefreely blog posts to a JSON file in this repo in case I want to ressurect any posts as "articles" here.</li>
			<li>This site will just be free-form, whatever I feel like writing about. No pressure to "blog". No structure, no outline, just some HTML docs online.</li>
		</ul>
	</p>

	<h2>Pages:</h2>
	{% for p in site.pages %}
	  * [{{ p.title }}]({{ p.url | absolute_url }})
		 <small>{{ p.excerpt }}</small>
 	{% endfor %}

</div><!-- /.blurb -->
