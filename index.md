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
			<li>Not much to say except our child started school today! Wow. Milestone. He's very happy. That, our 10th anniversary, and watching Cobra Kai have eaten all my non-work, non-normal-life time. Things are good. I am not sure what I want to do with this site, if anything. Why do I even have it? 
			</li>
			
			<li><img src="/assets/page-images/20190905_155941-tomatoes.jpg" width="200" />
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
