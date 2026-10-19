---
layout: page
permalink: /notes/
title: Notes
nav: true
nav_order: 3
---

Short pieces on designing and testing terahertz photonics, and what the lab teaches me along the way.

{%- assign sorted_notes = site.notes | sort: "order" | reverse -%}
<ul class="notes-list">
{%- for note in sorted_notes %}
<li>
<a class="note-link" href="{{ note.url | relative_url }}" target="_blank" rel="noopener">
<span class="note-title">{{ note.title }}</span>
{%- if note.tags and note.tags.size > 0 %}
<span class="note-tags">
{%- for tag in note.tags %}<span class="note-tag">{{ tag }}</span>{% endfor -%}
</span>
{%- endif %}
</a>
</li>
{%- endfor %}
</ul>
