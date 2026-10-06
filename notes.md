---
layout: page
title: Notes
permalink: /notes/
description: Short notes and fragments from Bereket Atakilt's notebook.
---

<div class="page-lede"><p class="label">Notes</p><h1>Fragments from the notebook.</h1><p>Shorter observations, useful papers, strange results, and things still being worked out.</p></div>
<div class="notes-list">{% for note in site.notes %}<article class="note-item"><time datetime="{{ note.date | date_to_xmlschema }}">{{ note.date | date: "%B %-d, %Y" }}</time><h2><a href="{{ note.url | relative_url }}">{{ note.title }}</a></h2><p>{{ note.excerpt | strip_html | truncatewords: 28 }}</p></article>{% else %}<p class="empty-state">The notes shelf is empty for now. Add a markdown file to <code>_notes/</code> to begin.</p>{% endfor %}</div>
