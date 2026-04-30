# Logic Flow

## Summary

1.  [Purpose](#purpose)
2.  [Template Map](#template-map)
3.  [Client-Side Behavior](#client-side-behavior)

## Purpose

This document maps the small amount of site logic so the Jekyll structure feels
closer to a conventional web frontend project.

## Template Map

```mermaid
graph TD
    Navigation["_data/navigation.yml"] --> Header["_includes/header.html"]
    Cases["_data/case_studies.yml"] --> CaseCard["_includes/case-card.html"]
    Research["_data/research.yml"] --> ResearchPage["pages/research.md"]
    Writing["_data/writing.yml"] --> WritingPage["pages/writing.md"]
    CaseCard --> Home["index.md"]
    CaseCard --> CaseStudies["pages/case-studies.md"]
    Header --> Default["_layouts/default.html"]
    Home --> HomeLayout["_layouts/home.html"]
    HomeLayout --> Default
    CaseStudies --> PageLayout["_layouts/page.html"]
    ResearchPage --> PageLayout
    WritingPage --> PageLayout
    PageLayout --> Default
```

## Client-Side Behavior

```mermaid
graph TD
    Toggle[".nav-toggle click"] --> Class["Toggle .site-nav.is-open"]
    Class --> Aria["Update aria-expanded"]
    NavLink["Navigation link click"] --> Close["Close mobile menu"]
    Close --> AriaFalse["Set aria-expanded false"]
```

The site intentionally avoids heavy JavaScript until there is a specific
portfolio feature that benefits from it.
