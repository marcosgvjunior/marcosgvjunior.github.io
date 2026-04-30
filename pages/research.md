---
layout: page
title: Research
kicker: Research Engineering
description: Peer-reviewed work, academic training, and scientific computing foundations that support the applied AI and data portfolio.
permalink: /research/
---

## Selected Publications

<div class="record-list">
  {%- for item in site.data.research.publications -%}
    <article class="record">
      <p class="eyebrow">{{ item.venue }} | {{ item.year }}</p>
      <h2><a href="{{ item.url }}">{{ item.title }}</a></h2>
    </article>
  {%- endfor -%}
</div>

## Awards

<div class="record-list record-list--compact">
  {%- for item in site.data.research.awards -%}
    <article class="record">
      <h2>{{ item.title }}</h2>
      <p>{{ item.detail }}</p>
    </article>
  {%- endfor -%}
</div>

## Education

<div class="timeline">
  {%- for item in site.data.research.education -%}
    <article class="timeline__item">
      <p class="eyebrow">{{ item.period }}</p>
      <h2>{{ item.title }}</h2>
      <p>{{ item.institution }}</p>
    </article>
  {%- endfor -%}
</div>
