---
title: Blogg
permalink: /blogg
---

 <div class="sidebar">
    {% include sidebar.html %}
    </div>
<div class="blog" id="dimmable">
    <div><h1>Blogg</h1></div>
    <div><ul>
        {% for post in site.posts %}
        <li class="blog__post">
            <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
            <div class="post__date">{{ post.date | date: "%-d %b %Y" }}</div>
            <div class="post__tags">
                <ul>
                    <li>
                        {% if post %}
                            {% assign tags = post.tags %}
                        {% else %}
                            {% assign tags = page.tags %}
                        {% endif %}
                        {% for tag in tags %}
                            <a href="/blogg/tags/{{tag|slugize}}">{{tag}}</a>
                        {% unless forloop.last %},&nbsp;{% endunless %}
                        {% endfor %}
                    </li>
                </ul>
            </div>
            <div class="post__content">
                {{ post.content }}
            </div>
        </li>
        {% endfor %}
    </ul></div>
</div>
<div class="accent"><div class="accent2"></div></div>