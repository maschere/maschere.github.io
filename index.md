---
theme: jekyll-theme-slate
title: Hank Quinlan's Blog
---
	<h1>{{ page.title }}</h1>
	<ul>

	  {% for post in site.posts %}
	    <li><span>{{ post.date | date_to_string }}</span> » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
	  {% endfor %}
	</ul>