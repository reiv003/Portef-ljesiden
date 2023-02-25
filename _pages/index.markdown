---
layout: default
title: Forside
permalink: /
---

<div class="sidebar">
<div class="sidebar__content">
    <div><h1 class="sidebar__title">Velkommen!</h1></div>
    <div>
     På denne siden har jeg lagt ut min CV, artikler om prosjektene jeg har jobbet med og innlegg om løst og fast innen IT.</div>
    </div>
</div>

<div class="index">
    <div>
        <h2>Siste blogginnlegg</h2>
        <ul>
            {% for post in site.posts limit: 1 %}
            <li class="blog__post"><h3>{{ post.title }}</h3>
                <div class="post__date">{{ post.date | date: "%b %-d, %Y" }}</div>
                {{ post.excerpt | strip_html | truncatewords: 50 }}
                <div class="post__link"><a href="{{ post.url }}">Les videre</a></div>
            </li>
            {% endfor %}
        </ul>
    </div>
    <div>
        <h2>Prosjekter</h2>
        <div>
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
            <div><a href="/prosjekter">Se alle ➜</a></div>
        </div>
    </div>
    
</div>
<div class="accent"><div class="accent2"></div></div>