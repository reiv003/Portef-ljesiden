---
layout: default
title: Forside
permalink: /
---

<div class="index">
    <div><h1>Velkommen!</h1>Dette er forsiden</div>
    <div class="index__latest-blog">
        <h2>Siste blogginnlegg</h2>
        <ul>
            {% for post in site.posts limit: 1 %}
            <li><h3>{{ post.title }}</h3>
                <div class="post__date">{{ post.date | date: "%b %-d, %Y" }}</div>
                {{ post.excerpt }}
                <div class="post__link"><a href="{{ post.url }}">Les videre</a></div>
            </li>
            {% endfor %}
        </ul>
    </div>
</div>