---
layout: page
permalink: /presentations/
title: Presentations
description: Invited talks, research demonstrations, and conference presentations.
nav: true
nav_order: 5
---

## Invited talks

**Joint-Associated Mechanical Sounds**<br>
Division of Pediatric Rheumatology, Emory University School of Medicine, Atlanta, GA (March 25, 2026)

**Personalized Robotic Intervention for Children with Autism Spectrum Disorder**<br>
Talking Robotics Podcast (2023) <a href="https://www.youtube.com/watch?v=hiKEESTVQ9I" target="_blank" rel="noopener" title="Watch on YouTube" aria-label="Watch on YouTube" style="font-size: 1.25rem; margin-left: 0.35rem;"><i class="fa-brands fa-youtube"></i></a> <a href="https://open.spotify.com/episode/1QLsrHM0W1cJ4ixrY6GgjV" target="_blank" rel="noopener" title="Listen on Spotify" aria-label="Listen on Spotify" style="font-size: 1.25rem; margin-left: 0.35rem;"><i class="fa-brands fa-spotify"></i></a>

## Research demonstrations

- National Science Foundation site visit, Louisville Automation and Robotics Research Institute (LARRI), University of Louisville (2023)
- Doss High School visit, LARRI, University of Louisville, NSF outreach (2023)
- LARRI Summer Open House, University of Louisville (2023)
- U.S. Navy site visit, LARRI, University of Louisville (2022)
- NAO and MILO robot demonstration, St. Aloysius Catholic School, NSF outreach (2022)

## Conference presentations

<!-- Entries come from _data/conference_presentations.yml. Photos live in assets/img/presentations/. -->
<style>
  .conf-list { list-style: none; padding: 0; margin: 0; }
  .conf-item { display: flex; gap: 1rem; align-items: flex-start; padding: 0.9rem 0; border-top: 1px solid var(--global-divider-color); }
  .conf-item:first-child { border-top: 0; padding-top: 0.25rem; }
  .conf-photo { flex: 0 0 9.5rem; width: 9.5rem; height: 7rem; object-fit: cover; object-position: center 25%; border-radius: 0.375rem; cursor: zoom-in; }
  .conf-title { font-weight: 600; line-height: 1.35; }
  .conf-meta { color: var(--global-text-color-light); font-size: 0.925rem; margin-top: 0.2rem; }
  .conf-type { display: inline-block; font-size: 0.75rem; font-weight: 600; padding: 0.1rem 0.45rem; border-radius: 0.25rem; background: #efe6d2; color: #5c4a2e; margin-right: 0.35rem; }
  @media (max-width: 576px) { .conf-photo { flex-basis: 6.5rem; width: 6.5rem; height: 5rem; } }
</style>
<ul class="conf-list">
{% for item in site.data.conference_presentations %}
<li class="conf-item">
<img class="conf-photo" {% if item.position %}style="object-position: {{ item.position }};" {% endif %}src="{{ item.image | prepend: '/assets/img/presentations/' | relative_url }}" alt="{{ item.type }} at {{ item.venue }}, {{ item.year }}" loading="lazy" data-zoomable>
<div>
<div class="conf-title">{{ item.title }}</div>
<div class="conf-meta"><span class="conf-type">{{ item.type }}</span>{{ item.venue }}{% if item.location %}, {{ item.location }}{% endif %}, {{ item.year }}{% if item.award %}. <strong>{{ item.award }}</strong>{% endif %}</div>
</div>
</li>
{% endfor %}
</ul>
