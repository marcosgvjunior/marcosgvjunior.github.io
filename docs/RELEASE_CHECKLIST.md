# Release Checklist

## Summary

1.  [Purpose](#purpose)
2.  [Content Checks](#content-checks)
3.  [Visual Checks](#visual-checks)
4.  [Technical Checks](#technical-checks)
5.  [Release Notes](#release-notes)

## Purpose

This checklist keeps the portfolio useful for recruiters, technical reviewers,
collaborators, and potential clients. Site updates improve clarity, evidence,
navigation, or visual polish.

## Content Checks

- The page explains the professional signal clearly.
- Project descriptions connect problem, workflow, evidence, and limitation.
- Links point to stable repositories, papers, posts, websites, or demos.
- Role language is broad enough for software, data science, applied AI/ML,
  analytics, and data engineering opportunities.
- Business-facing text is written for readers outside the development process.

## Visual Checks

- Images support the project or case-study signal.
- Hero and card images are not generic decoration.
- Text remains readable on desktop and mobile.
- Cards, buttons, and navigation remain visually consistent.

## Technical Checks

```bash
docker build -t marcosgvjunior-github-io .
docker run --rm marcosgvjunior-github-io bundle exec jekyll build --trace
git diff --check
```

## Release Notes

Before pushing, summarize:

- what changed for site visitors;
- which pages or data files changed;
- which build checks passed;
- any remaining visual or content follow-up.
