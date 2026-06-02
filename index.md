---
title: Home
description: Portfolio for Je'aime H. Powell, focused on HPC, AI, science gateways, and workforce development.
---

<section class="hero">
  <div class="container hero-grid">
    <div>
      <p class="eyebrow">Portfolio</p>
      <h1>HPC, AI, and workforce development for practical research computing.</h1>
      <p class="lead"><strong>Je'aime H. Powell</strong> builds bridges between research infrastructure, student training, AI systems, and technical storytelling.</p>
      <div class="hero-actions">
        <a class="button" href="{{ '/projects/' | relative_url }}">View Projects</a>
        <a class="button secondary" href="{{ '/contact/' | relative_url }}">Contact Me</a>
      </div>
    </div>
    <aside class="profile-card">
      <h2>Focus Areas</h2>
      <ul>
        <li>High Performance Computing</li>
        <li>AI agents and local LLM workflows</li>
        <li>Science Gateway training</li>
        <li>Undergraduate workforce development</li>
        <li>GitHub Pages and Jekyll sites</li>
      </ul>
    </aside>
  </div>
</section>

<section class="section">
  <div class="container">
    <div class="section-header">
      <p class="eyebrow">What I Do</p>
      <h2>I turn complex research computing work into usable systems, training programs, and clear communication.</h2>
    </div>
    <div class="grid three">
      {% for item in site.data.experience %}
      <div class="card">
        <h3>{{ item.title }}</h3>
        <p><strong>{{ item.organization }}</strong></p>
        <p>{{ item.summary }}</p>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

<section class="section muted">
  <div class="container">
    <div class="section-header">
      <p class="eyebrow">Selected Skills</p>
      <h2>Technical depth with education-focused delivery.</h2>
    </div>
    <div class="grid two">
      {% for group in site.data.skills %}
      <div class="card">
        <h3>{{ group.category }}</h3>
        <div class="tag-row">
          {% for skill in group.items %}<span class="tag">{{ skill }}</span>{% endfor %}
        </div>
      </div>
      {% endfor %}
    </div>
  </div>
</section>

<section class="section">
  <div class="container">
    <div class="section-header">
      <p class="eyebrow">Projects</p>
      <h2>Featured work</h2>
    </div>
    <div class="grid three">
      {% assign featured_projects = site.projects | where: "featured", true %}
      {% for project in featured_projects limit:3 %}
      <a class="card project-card" href="{{ project.url | relative_url }}">
        <h3>{{ project.title }}</h3>
        <p>{{ project.summary }}</p>
        <div class="tag-row">
          {% for tag in project.tags limit:3 %}<span class="tag">{{ tag }}</span>{% endfor %}
        </div>
      </a>
      {% endfor %}
    </div>
  </div>
</section>
