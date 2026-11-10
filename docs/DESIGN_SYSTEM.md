# Design System

## Summary

1.  [Direction](#direction)
2.  [Visual Language](#visual-language)
3.  [Images](#images)
4.  [Components](#components)
5.  [Next Improvements](#next-improvements)

## Direction

The site is designed as a technical portfolio, not a generic personal blog. The
visual system supports scanning, comparison, and evidence review for recruiters,
technical readers, and potential collaborators.

## Visual Language

- quiet neutral background;
- strong typography;
- restrained card borders;
- teal, amber, and red accents for system, evidence, and risk signals;
- dense but readable sections;
- no decorative blobs or unrelated illustration.

## Images

Images reveal the work or the portfolio signal:

- project screenshots;
- generated visuals tied to already published posts;
- diagrams or generated visuals tied to a specific case study;
- research visuals with clear source rights and context.

The home hero uses `assets/images/formless-echo-hero.webp`, a purpose-made
illustration connecting the portfolio to Formless Solutions. T-echo Wings and
F-echo Solutions appear with voice, data, and security symbols. It is a brand
illustration, not a product screenshot or evidence of deployed capabilities.

The composition is open, centered, and visually balanced: the studio's central
axis and holographic table sit between T-echo Wings and F-echo Solutions.
The existing page layout, centered image crop, and text overlay are preserved.
The image is decorative (`alt=""`), has explicit intrinsic dimensions, and is
prioritized as an above-the-fold asset. The original background asset is
retained for an easy rollback.

The Tavern's Ledger card uses `assets/images/case-studies/taverns-ledger.webp`,
a thematic illustration of a tavern inventory ledger. It reflects the RPG
cataloging concept, rather than pretending to show the application interface.

## Components

- Hero: positioning and primary actions.
- Proof strip: three quick professional signals.
- Case cards: track, status, summary, evidence bullets, and links.
- Record lists: publications, awards, and education.
- Writing cards: public writing lanes.

## Next Improvements

- Keep the hero composition and text contrast checked at desktop and mobile widths.
- Add screenshots for The Tavern's Ledger backend/frontend.
- Add case-study pages with diagrams for computer vision calibration, complaint
  intelligence, and RAG evaluation.
- Add a small visual asset checklist before any new public page is added.
