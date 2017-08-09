---
theme: jekyll-theme-slate
title: Hank Quinlan's Blog
---
test13

{% assign posts = (site.posts | sort: 'date') | reverse %}
{% for post in posts %}

### [{{ post.title }}]({{ post.url }})
{{ post.date | date_to_string }}
{{ post.content | strip_html | truncatewords: 3 }} [read more]({{ post.url }})

___
<br><br>



{% endfor %}

