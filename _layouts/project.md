---
layout: default
---

<div class="sidebar">
  <div class="sidebar__content"> 
    <nav class="sidebar__toc">
      <div class="sidebar__title">Innholdsfortegnelse</div>
      {{ page.sidebar-content | markdownify }}
    </nav>
  </div>
</div>

<div class="text__content">
  <div class="content__wrapper">
    <h1>{{ page.title }}</h1>
    {{ content }}
    <div class="project__date-info">Først publisert {{ page.published_date | date: "%-d. %b %Y" }}, sist endret {{ page.last_edited_date | date: "%-d. %b %Y" }} </div>
  </div>
</div>

<div class="accent"><div class="accent2"></div>
</div>