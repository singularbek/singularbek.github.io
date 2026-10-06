---
layout: page
title: Projects
permalink: /projects/
description: Selected software projects and computational experiments by Bereket Atakilt.
---

<div class="page-lede"><p class="label">Projects</p><h1>Things built to be understood.</h1><p>A working archive of software, experiments, and small systems. The descriptions below are intentionally short; each project can grow its own documentation over time.</p></div>
<div class="project-list project-list-page">{% for project in site.data.projects %}{% include project-item.html project=project index=forloop.index %}{% endfor %}</div>
