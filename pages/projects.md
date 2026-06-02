---
title: Projects
permalink: /projects/
---

<section class="page-hero compact">
  <div class="container">
    <p class="eyebrow">Projects</p>
    <h1>Selected Projects</h1>
    <p class="lead">A portfolio of work across HPC, AI, workforce development, technical systems, and web publishing.</p>
  </div>
</section>

<section class="section">
  <div class="container project-list">
    {% for project in site.projects %}
    <a class="card project-card" href="{{ project.url | relative_url }}">
      <h2>{{ project.title }}</h2>
      <p>{{ project.summary }}</p>
      <div class="tag-row">
        {% for tag in project.tags %}<span class="tag">{{ tag }}</span>{% endfor %}
      </div>
    </a>
    {% endfor %}
  </div>
</section>
