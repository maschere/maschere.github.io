---
theme: jekyll-theme-slate
title: Hank Quinlan's Blog
---
test5

## {{ page.title }}

{% assign posts = site.posts | sort: 'date' %}
{% for post in posts %}

* {{ post.date | date_to_string }} [{{ post.title }}]({{ post.url }})

   {{ post.content | strip_html | truncatewords: 3 }}
   
   {% if post.content contains '<!--break-->' %}
   [{{ read more }}]({{ post.url }})
   {% endif %}

{% endfor %}

