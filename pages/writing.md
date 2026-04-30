---
layout: page
title: Writing
kicker: Public Technical Notes
description: Public writing lanes that connect technical work, research background, applied AI practice, and professional positioning.
permalink: /writing/
---

<div class="writing-grid">
  {%- for item in site.data.writing -%}
    <article class="writing-card">
      <p class="eyebrow">{{ item.status }}</p>
      <h2>{{ item.title }}</h2>
      <p>{{ item.summary }}</p>
      <ul class="signal-list">
        {%- for signal in item.evidence -%}
          <li>{{ signal }}</li>
        {%- endfor -%}
      </ul>
    </article>
  {%- endfor -%}
</div>

## Writing Focus

The writing track translates technical work into clear professional evidence:
what problem was addressed, what artifact was built, which metric or contract
matters, and what the result does or does not prove.

This supports recruiters, technical peers, collaborators, and potential clients
who need to understand both the engineering work and the decision logic behind
it.
