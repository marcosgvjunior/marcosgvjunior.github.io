---
layout: page
title: Case Studies
kicker: Portfolio Evidence
description: Public portfolio evidence across software delivery, data science, applied AI/ML, research engineering, and scientific computing.
permalink: /case-studies/
---

<div class="case-grid case-grid--wide">
  {%- for item in site.data.case_studies -%}
    {%- include case-card.html item=item -%}
  {%- endfor -%}
</div>

<section class="prose-card">
  <h2>Evidence Standard</h2>
  <p>
    Each case study is selected because it connects a concrete problem to a
    visible technical workflow, validation signal, limitation, and public source
    material. The goal is not to list every repository; it is to make the
    strongest evidence easy to evaluate.
  </p>
  <p>
    The current portfolio spans full-stack software, data science, applied
    AI/ML, research engineering, and scientific computing. The active AI/ML
    track will keep growing through case studies on calibration, text
    intelligence, retrieval evaluation, and operational decision workflows.
  </p>
</section>
