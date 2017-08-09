---
theme: jekyll-theme-slate
title: Hank Quinlan's Blog
---
test15

{% assign posts = (site.posts | sort: 'date') | reverse %}
{% for post in posts %}

### [{{ post.title }}]({{ post.url }})
<p style='line-height: 90%;'>{{ post.date | date_to_string }}</p>

{{ post.content | strip_html | truncatewords: 3 }} [read more]({{ post.url }})

___
<br><br>



{% endfor %}

