---
layout: default
permalink: /books/
---

<div>
    {% for cat in site.book-categories %}
        <div><h2>{{cat}}<hr></h2></div>
        <ul>
            {% for post in site.posts%}
                {% if post.category == cat %}
                    <li>
                        <a href="{{ post.url }}">{{ post.title }}</a>
                    </li>
                {% endif %}
            {% endfor %}
        </ul>
    {% endfor %}
</div>


