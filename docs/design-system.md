# Portfolio Design System

Three layers: **primitives** (the only place hex values live) → **semantic tokens** (re-mapped per theme under `html[data-theme="dark"]`) → components (semantic tokens only). Dark is the default theme. Light lives in `:root`.

## Color (semantic)
| Token | Light | Dark | Use |
|---|---|---|---|
| --color-bg | gray-25 #f7f8fb | night-950 #0c0f15 | page |
| --color-surface | #fff | #141923 | panels |
| --color-surface-raised | #fff | #19202d | cards, resume btn |
| --color-surface-subtle / -hover | #f1f3f8 / #e6ebf3 | #1c2331 / #273246 | chips, btn hover |
| --color-border / -subtle | #d5d9e2 / #e4e7ef | #283142 / #202838 | decorative dividers |
| --color-border-control | #8790a2 (3.2:1) | #6b778c (3.9:1) | edges of interactive controls |
| --color-text / -muted | #12151c / #464e5e | #f2f4f8 / #b0b8c8 | copy |
| --color-accent / -hover / -contrast | #1a478c / #12366e / #fff | #7eb2ff / #a3c8ff / #0c0f15 | **interactive only**: links, active filter, highlighted pill, primary CTA, chevron, hover borders |
| --color-metric-bg / -text | #f8efe0 / #734509 | #3a2a14 / #f5c984 | data: experience metrics, context badges |
| --color-success | #15803d | #16a34a | status dot |
| --color-tag-* | neutral | neutral | non-interactive tech pills |
| --color-focus | #1a5fd0 | #7eb2ff | focus ring |

Rule: blue means you can click it. Amber means data. Everything else is neutral.

## Type
Scale: --fs-xs 12 · sm 13 · md 14 · base 16 · lg 18 · xl 20 · 2xl 28 · 3xl 36 · 4xl 48.
Weights: --fw-regular 400 · medium 500 · semibold 600 · bold 700.
Line heights: --lh-tight 1.2 · snug 1.35 · normal 1.55 · relaxed 1.65.
Fonts: --font-display (Kantumruy Pro) for headings, --font-body (Inter).

## Spacing (4px grid)
--space-1 4 · 2 8 · 3 12 · 4 16 · 5 20 · 6 24 · 7 28 · 8 32 · 10 40 · 12 48 · 18 72 · --space-section 84 · --touch 44 (minimum touch target).

## Radius
--radius-xs 4 (focus) · sm 8 (buttons) · md 12 (media) · lg 16 (cards/panels) · pill 999 · round 50%.

## Shadow
--shadow-sm (resting) · --shadow-md (headshot) · --shadow-lg (card hover) · --shadow-glow (brand dot). Dark theme swaps in deeper versions.

## Motion
--dur-fast .15s · --dur-base .2s · --dur-slow .3s · --ease · --ease-out cubic-bezier(.22,1,.36,1). `prefers-reduced-motion` disables transforms and transitions.

## Components
.contact-chip(.is-primary), .filter-chip(.is-active)+.chip-count, .card (+ .thumb-wrap/.thumb-video/.play-hint/.is-playing), .pills li(.is-extra/.is-highlighted)+.pills-more, .repo-btn, .btn/.btn-disabled, .status-note, details.reflection, .exp-band/.exp-metric, .theme-toggle, .btn-resume.
