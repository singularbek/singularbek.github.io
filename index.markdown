---
layout: home
title: Heruy — Bereket Atakilt
description: Backend engineering, AI/ML, and complex systems.
---

<section class="intro-block" aria-labelledby="intro-title">
  <div class="notebook-strip"><span>Personal Research Notebook</span><span>Vol. I · 2026</span></div>
  <div class="home-cover"><span>Bereket Atakilt · ሕሩይ</span></div>
  <h1 id="intro-title">Bereket Atakilt</h1>
  <p class="alias">Heruy</p>
  <p class="identity-role">Ethiopian Software and AI/ML Engineer</p>
  <div class="intro-copy">
    <p>My name is Bereket Atakilt but you can call me Heruy. In Ge'ez Heruy or Hiruy means 'the Chosen one' or 'the Exalted one'. I am an Ethiopian software and AI/ML engineer working, building and learning around machine learning, language models and AI agents, computational systems, simulations and reinforcement learning with one unifiying theme - the strange ways simple rules can produce complex behavior.</p>
    <p>I intended this site to be a sort of journal or logbook as I explore these ideas in English and code.</p>
  </div>
  <div class="link-row" aria-label="Contact links">{% include social-links.html %}</div>
</section>

<section class="home-section focus-section" aria-labelledby="focus-title">
  <div class="section-label-row"><p class="label">Focus</p><span class="section-index">01</span></div>
  {% assign featured_post = site.posts | where: "featured", true | first %}
  {% if featured_post %}
    <article class="feature-essay">
      <!-- <a class="feature-media{% if featured_post.image %} has-image{% endif %}" href="{{ featured_post.url | relative_url }}" aria-label="Read {{ featured_post.title }}">
        {% if featured_post.image %}<img src="{{ featured_post.image | relative_url }}" alt="{{ featured_post.image_alt | default: featured_post.title | escape }}" loading="lazy" decoding="async">
        {% else %}<span class="placeholder-art" aria-hidden="true"><span>ሰላም ዓለም</span><i></i><b>01</b></span><span class="sr-only">Cover image placeholder; add an image in the post front matter.</span>{% endif %}
      </a> -->
      <div class="feature-copy">
        <div class="post-meta"><span>{{ featured_post.categories | first | default: "Essay" }}</span><time datetime="{{ featured_post.date | date_to_xmlschema }}">{{ featured_post.date | date: "%B %-d, %Y" }}</time></div>
        <h2 id="focus-title"><a href="{{ featured_post.url | relative_url }}">{{ featured_post.title }}</a></h2>
        <p>{{ featured_post.excerpt | strip_html | default: "A developing essay from the notebook." | truncatewords: 42 }}</p>
        <a class="text-link" href="{{ featured_post.url | relative_url }}">Read essay <span aria-hidden="true">→</span></a>
      </div>
    </article>
  {% else %}<p class="empty-state">Mark one post with <code>featured: true</code> to place it here.</p>{% endif %}
</section>

<section class="home-section" aria-labelledby="selected-work-title">
  <div class="section-label-row"><p class="label">Selected works</p><span class="section-index">02</span></div>
  <p class="section-note">Selected experiments, implementations, and computational studies.</p>
  <div class="project-list" id="selected-work-title">{% for project in site.data.projects limit:4 %}{% include project-item.html project=project index=forloop.index %}{% endfor %}</div>
  <a class="text-link section-end-link" href="{{ '/projects/' | relative_url }}">View all projects <span aria-hidden="true">→</span></a>
</section>

<section class="home-section" aria-labelledby="writing-title">
  <div class="section-label-row"><p class="label">Writing</p><span class="section-index">03</span></div>
  <div class="writing-list" id="writing-title">{% for post in site.posts limit:3 %}{% include post-card.html post=post index=forloop.index %}{% endfor %}</div>
  <a class="text-link section-end-link" href="{{ '/writing/' | relative_url }}">View all writing <span aria-hidden="true">→</span></a>
</section>

<section class="home-section exploring-section" aria-labelledby="exploring-title">
  <div class="section-label-row"><p class="label">Currently exploring</p><span class="section-index">04</span></div>
  <h2 id="exploring-title">Questions before answers.</h2>
  <div class="topic-list"><span>Artificial intelligence</span><span>Language models</span><span>Reinforcement learning</span><span>Complex systems</span><span>Scientific computing</span><span>Computation</span></div>
</section>
