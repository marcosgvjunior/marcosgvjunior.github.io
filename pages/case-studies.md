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

## Evidence Standard

Each case study is selected because it connects a concrete problem to a visible
technical workflow, validation signal, limitation, and public source material.
The goal is not to list every repository; it is to make the strongest evidence
easy to evaluate.

The current portfolio spans full-stack software, data science, applied AI/ML,
research engineering, and scientific computing. The active AI/ML track will keep
growing through case studies on calibration, text intelligence, retrieval
evaluation, and operational decision workflows.
