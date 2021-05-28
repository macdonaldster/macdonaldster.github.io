---
layout: default
title: ... home
date: 2020-08-12
last_modified_at: 2020-08-12 06:54 -6
---
<hr/>
<br/>
<div class="blurb">
	{% assign sorted = site.pages | sort: 'last_modified_at' | reverse %}
	{% for p in sorted limit:1 %}
		<div>
			{{p.content | markdownify }}
		</div>
		<hr/>
		      <section>

	<div class="tags">
	  {% assign sortedCategories = p.categories  %}
	  {% for category in sortedCategories %}
          <span class="tag">
            <a href="/category/{{ category }}.html">#{{ category }}</a>
          </span>
	  {% endfor %}
	</div>
	
      </section>

 	{% endfor %}
<br/>
<hr/>
<br/>
	<h1>Notes:</h1>
	<p>
		<ul>
		<li>I added category pages to this site so now can refer you to the <a href="/category/covid19.html">COVID19</a> page where I am collecting thoughts on life during this pandemic. </li>
			<li>I thought I would stick this link here to remind me why and how to journal - <a href="https://dariusforoux.com/how-to-journal/">https://dariusforoux.com/how-to-journal/</a></li>
			<li>The phrase "isn't there anything faster than a microwave" from The Simpons crosses my mind between 1 and 20 times a day.</li>
			<li>Why are we still designing new styles of pants? After all this time, shouldn't we have figured that out?</li>
		</ul>
	</p>
<hr/>
<br/>
	<h2>Blogs (last updated, first):</h2>
	<ul>
	{% assign sorted = site.pages | sort: 'last_modified_at' | reverse %}
	{% for p in sorted %}
	   {% if p.title contains '2020-' or p.title contains '2021-'  %}
	      <li> <a href="{{ p.url | absolute_url }}">{{ p.title }}</a></li>
	   {% endif %}
 	{% endfor %}
	</ul>

<hr/>
<br/>
<h2>All other pages (last updated, first):</h2>
	<ul>
	{% assign sorted = site.pages | sort: 'last_modified_at' | reverse %}
	{% for p in sorted %}
		{% if p.categories.size > 0  %}
		   {% unless p.categories contains 'blog' %}
	  	      <li> <a href="{{ p.url | absolute_url }}">{{ p.title }} | {{ p.last_modified_at | date: "%Y-%m-%d" }} </a></li>
		   {% endunless %}
		{% endif %}
 	{% endfor %}
	</ul>

</div><!-- /.blurb -->
