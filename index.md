---
layout: home
title: Home
body_class: home-page
---

<section class="hero">
  <img class="hero__image" src="{{ "/assets/images/background.png" | relative_url }}" alt="">
  <div class="hero__shade"></div>
  <div class="hero__content">
    <p class="eyebrow">Data Science | Applied AI/ML | Software Engineering</p>
    <h1>Marcos Vieira</h1>
    <p class="hero__lede">
      I build reproducible data, applied AI/ML, and software systems that turn
      experiments into validated, documented, and decision-ready workflows.
    </p>
    <div class="hero__actions">
      <a class="button button--primary" href="{{ "/case-studies/" | relative_url }}">View Case Studies</a>
      <a class="button button--secondary" href="{{ "/research/" | relative_url }}">Research Background</a>
    </div>
  </div>
</section>

<section class="proof-strip" aria-label="Portfolio signals">
  <div class="proof-strip__item">
    <strong>Software</strong>
    <span>Full-stack MVPs, APIs, frontend interfaces, Docker, CI/CD, tests, documentation</span>
  </div>
  <div class="proof-strip__item">
    <strong>Data Science And Applied AI/ML</strong>
    <span>Classical ML, computer vision, NLP, LLM/RAG, metrics, and model evaluation</span>
  </div>
  <div class="proof-strip__item">
    <strong>Research Engineering</strong>
    <span>scRNA-seq, stochastic modeling, sensor data, scientific computing, statistical validation</span>
  </div>
</section>

<section class="section">
  <div class="section__header">
    <p class="eyebrow">Selected Evidence</p>
    <h2>Portfolio Work</h2>
    <p>
      The portfolio is organized around evidence: shipped software, reproducible
      data and ML workflows, peer-reviewed research engineering, scientific
      computing, and technical writing that explains decisions and limitations.
    </p>
  </div>

  <div class="case-grid">
    {%- assign featured_cases = site.data.case_studies | where: "featured", true -%}
    {%- for item in featured_cases -%}
      {%- include case-card.html item=item -%}
    {%- endfor -%}
  </div>
</section>

<section class="section section--split">
  <div>
    <p class="eyebrow">Positioning</p>
    <h2>From Research To Delivery</h2>
  </div>
  <div class="split-copy">
    <p>
      My background connects applied physics, computational biology, scientific
      software, and practical data/AI workflows. The portfolio is designed for
      software, applied AI/ML, data science, analytics, and data engineering
      roles where evaluation, reproducibility, technical communication, and
      handoff-ready code matter.
    </p>
    <p>
      Formless Solutions extends this work into an emerging consulting studio
      focused on applied AI, data and software systems, strategy, and decision
      workflows for complex problems.
    </p>
  </div>
</section>

<section class="section section--contrast">
  <div class="section__header">
    <p class="eyebrow">Applied AI/ML Focus</p>
    <h2>Current Case Study Directions</h2>
    <p>
      The active AI/ML portfolio track focuses on practical workflows that make
      model behavior visible: calibration, text intelligence, retrieval quality,
      evidence grounding, and business-facing interpretation.
    </p>
  </div>
  <div class="pipeline-grid">
    <article>
      <span>Computer Vision</span>
      <h3>Face Recognition Calibration</h3>
      <p>Thresholds, FAR/FRR, open-set limits, and why calibration is not liveness detection.</p>
    </article>
    <article>
      <span>NLP And Analytics</span>
      <h3>Complaint Intelligence</h3>
      <p>Text signals, sentiment limits, aspect cues, and operational triage over public complaint data.</p>
    </article>
    <article>
      <span>LLM/RAG</span>
      <h3>Contract RAG Evaluation</h3>
      <p>Citations, abstention, retrieval quality, and auditable document intelligence.</p>
    </article>
  </div>
</section>
