---
theme: jekyll-theme-slate
title: Hank Quinlan's Blog
---
test10

{% assign posts = (site.posts | sort: 'date') | reverse %}
{% for post in posts %}

{{ post.date | date_to_string }}
## [{{ post.title }}]({{ post.url }})

{{ post.content | strip_html | truncatewords: 3 }}

[{{ read more }}]({{ post.url }})


{% endfor %}

