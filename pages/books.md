---
layout: default
permalink: /books/
---

<ul>
{% for cat in site.categories %}
{% capture cat %}{{ cat }}{% endcapture %}
<div class="TEST">{{cat}}</div>
  {% for post in site.posts %}
    {% if post.category == cat %}
            <li>
              <a href="{{ post.url }}">{{ post.title }}</a>
            </li>
    {% endif %}
  {% endfor %}
{% endfor %}
</ul>

