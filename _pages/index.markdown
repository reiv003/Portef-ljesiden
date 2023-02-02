---
layout: default
title: Forside
permalink: /
---

<div class="sidebar">
    Dette er forsiden
</div>

<div class="index">
    <div><h1>Velkommen!</h1></div>
    <div>
        <h2>Siste blogginnlegg</h2>
        <ul>
            {% for post in site.posts limit: 1 %}
            <li class="blog__post"><h3>{{ post.title }}</h3>
                <div class="post__date">{{ post.date | date: "%b %-d, %Y" }}</div>
                {{ post.excerpt }}
                <div class="post__link"><a href="{{ post.url }}">Les videre</a></div>
            </li>
            {% endfor %}
        </ul>
    </div>
    
</div>
<div class="accent"><div class="accent2"></div></div>