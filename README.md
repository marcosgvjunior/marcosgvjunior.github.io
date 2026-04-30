# Marcos Vieira Portfolio Site

Public GitHub Pages portfolio for end-to-end data and software systems:
applied AI/ML, analytics, automation, software engineering, data engineering,
and research engineering.

Live site: <https://marcosgvjunior.github.io>

## Summary

1.  [Site Contributions](#site-contributions)
2.  [Project Overview](#project-overview)
3.  [Project Structure](#project-structure)
4.  [Architecture](#architecture)
5.  [Setup And Execution](#setup-and-execution)
6.  [Detailed Documentation](#detailed-documentation)
7.  [Development Workflow](#development-workflow)
8.  [Validation](#validation)
9.  [References](#references)

## Site Contributions

- **Portfolio information architecture:** The site separates home, case
  studies, research, writing, and about/contact surfaces instead of rendering a
  single long README-style page.
- **Data-driven Jekyll content:** Navigation, case-study cards, writing lanes,
  and research records live in `_data/` so content can be maintained without
  rewriting layouts.
- **Reusable page components:** Shared header, footer, and case-study cards live
  in `_includes/`, with page templates under `_layouts/`.
- **Web-style asset and page structure:** Public pages live under `pages/`, CSS
  under `assets/css/`, JavaScript under `assets/js/`, and images under
  `assets/images/`, keeping the Jekyll-specific directories clearly separated
  from normal frontend assets.
- **Containerized local preview:** Docker provides the Ruby/Jekyll runtime so
  the site can be built without installing Ruby on the host.

## Project Overview

This repository publishes <https://marcosgvjunior.github.io>. The site is a
public portfolio surface for selected professional background, research
engineering, applied AI/data/software projects, and writing.

The portfolio emphasizes evidence that is useful for recruiters, technical
reviewers, collaborators, and potential clients: working software, reproducible
data and AI workflows, research outputs, technical writing, and clear links to
source material.

## Project Structure

```text
.
|-- _data/          # Navigation, case-study, research, and writing records
|-- _includes/      # Reusable Liquid components
|-- _layouts/       # Page templates
|-- assets/
|   |-- css/        # Stylesheets
|   |-- js/         # Client-side behavior
|   `-- images/     # Public visual assets
|-- docs/           # Public architecture and content documentation
|-- pages/          # Top-level site pages with stable permalinks
|-- index.md        # Home page
|-- _config.yml
|-- Dockerfile
|-- Gemfile
`-- docker-compose.yml
```

## Architecture

The site keeps content, presentation, and runtime concerns separate:

- `_data/*.yml` stores structured public content used by multiple pages.
- `_includes/*.html` renders reusable components such as cards and site chrome.
- `_layouts/*.html` defines page shells.
- `pages/*.md` defines public pages such as Case Studies, Research, Writing,
  and About / Contact.
- `assets/css/main.css` owns the visual system.
- `assets/js/main.js` owns small progressive-enhancement behavior.
- `Dockerfile` and `docker-compose.yml` own local Jekyll execution.

See [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) for details.

## Setup And Execution

Run the site locally:

```bash
docker compose up --build
```

Then open:

```text
http://localhost:4000
```

Stop the server with `Ctrl+C`.

Useful checks:

```bash
docker build -t marcosgvjunior-github-io .
docker run --rm marcosgvjunior-github-io bundle exec jekyll build --trace
git status --short --branch
```

## Detailed Documentation

- **[Documentation Index](docs/README.md):** Public documentation map.
- **[Architecture](docs/ARCHITECTURE.md):** Layout, data, assets, and
  runtime boundaries.
- **[Flow](docs/FLOW.md):** Browser, Jekyll, and Docker execution flow.
- **[Logic Flow](docs/LOGIC_FLOW.md):** Mermaid map of templates, data, and
  JavaScript behavior.
- **[Content Model](docs/CONTENT_MODEL.md):** How portfolio evidence is
  structured across pages.
- **[Design System](docs/DESIGN_SYSTEM.md):** Visual direction, image policy,
  and component rules.
- **[Local Development](docs/LOCAL_DEVELOPMENT.md):** Docker-first workflow.
- **[Release Checklist](docs/RELEASE_CHECKLIST.md):** Content and technical
  checks before updates are pushed.

## Development Workflow

1.  Update structured content in `_data/` when possible.
2.  Add reusable markup in `_includes/` only when more than one page needs it.
3.  Keep public explanatory docs in `docs/`.
4.  Validate with Docker before pushing.

## Validation

The current baseline check is a Jekyll build inside the Docker image:

```bash
docker build -t marcosgvjunior-github-io .
docker run --rm marcosgvjunior-github-io bundle exec jekyll build --trace
```

## References

- [GitHub Pages](https://docs.github.com/en/pages)
- [Jekyll](https://jekyllrb.com/)
