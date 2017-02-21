---
layout: default
---

{% for category in site.categories %}
<h2>{{ category | first }}</h2>
<ul class="posts">
{% for posts in category %}
  {% for post in posts %}
    {% if post.url %}
    <li><span>{{ post.date | date_to_string }}</span> » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
    {% endif %}
  {% endfor %}
{% endfor %}
</ul>
{% endfor %}
