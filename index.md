---
theme: jekyll-theme-slate
---

{% assign posts = (site.posts | sort: 'date') | reverse %}
{% for post in posts %}

### [{{ post.title }}]({{ post.url }})
<p style='line-height: 1%;'>{{ post.date | date_to_string }}</p>
<br>
{{ post.excerpt }} [read more]({{ post.url }})

___
<br><br>



{% endfor %}

