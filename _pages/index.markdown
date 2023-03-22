---
layout: default
title: Forside
permalink: /
---

<div class="sidebar">
<div class="sidebar__content">
    <div><h1 class="sidebar__title">Velkommen!</h1></div>
    <div class="sidebar__blurb">
     På denne siden har jeg lagt ut min CV, artikler om prosjektene jeg har jobbet med og innlegg om løst og fast innen IT.</div>
    </div>
</div>

<div class="index">
        <div class="index__blog">
            <h2>Siste blogginnlegg</h2>
                {% for post in site.posts limit: 1 %}
                <div class="index__post"><h3>{{ post.title }}</h3>
                    <div class="post__date">{{ post.date | date: "%d.%m.%y" }}</div>
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
                                {% unless forloop.last %}, {% endunless %}
                                {% endfor %}
                            </li>
                        </ul>
                    </div>
                    <div class="post__content">{{ post.excerpt | strip_html | truncatewords: 50 }}</div>
                    <div class="post__link"><a href="{{ post.url }}">Les videre ➜</a></div>
                </div>
                {% endfor %}
    </div>
        <div class="index__projects">
            <h2>Prosjekter</h2>
                <ul>
                    <li>
                        <h3><a href="/prosjekter">Prosjekt 1 ➜</a></h3>
                        <div>En linje om prosjektet, som omfatter eksisterende nettsider og designskisser.</div>
                    </li>
                    <li>
                        <h3>
                        <a href="/prosjekter">Prosjekt 2 ➜</a></h3>
                        <div>En linje om prosjektet, som omfatter eksisterende nettsider og designskisser.</div>
                    </li>
                    <li>
                        <h3><a href="/prosjekter">Prosjekt 3 ➜</a></h3>
                        <div>En linje om prosjektet, som omfatter eksisterende nettsider og designskisser.</div>
                    </li>
                </ul>
                <div class="index__follow-link"><a href="/prosjekter">Se alle ➜</a></div>
    </div>
    
</div>
<div class="accent"><div class="accent2"></div></div>