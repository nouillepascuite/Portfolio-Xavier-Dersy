# Portfolio (redesign, in progress)

Full rebuild from scratch, inspired by nick.computer (Nick McMillan's freelance
developer portfolio: https://nick.computer). This **replaces** the earlier "Web 1.0
mosaic" concept — see "What this replaces" below for what's being dropped.

## Concept
- Editorial, illustrated developer portfolio — playful and personal rather than
  minimal/grid-based.
- Light content sits on a dark (charcoal, `#333`) page background. Supports
  automatic light/dark mode via `prefers-color-scheme`.
- A small, curated set of projects (nick.computer shows ~5-8), each with a
  custom illustration, not a dense wall of tiles.

## Layout
- **Home**: name in large display type, a short one-line intro/bio, a row of
  circular social icon links, then a horizontal row of project cards (scrolls
  sideways if it overflows, rather than wrapping into a grid).
- **Card**: custom illustration/icon at top, project title below. On hover the
  card lifts with a layered drop-shadow (a soft blurred "upper" shadow plus a
  tighter "lower" shadow — not a single flat box-shadow) for a subtle
  parallax/tilt feel.
- **Detail page** (click a card): its own view, not a modal/lightbox — large
  project icon, title, a row of small tool/tech icons used on the project, one
  or two paragraphs of case-study copy, and a circular "Back" button (fixed
  position) to return home.

## Typography
- Display font: "Rammetto One" (Google Font) — used for the name, section
  sub-headings, and detail-page titles. Chunky, rounded, high personality.
- Body font: system UI sans-serif stack — `-apple-system, BlinkMacSystemFont,
  "Segoe UI", Roboto, Helvetica, Arial, sans-serif`.
- Tight letter-spacing (~`-0.4px`) throughout.

## Interaction details worth matching
- Card hover: shadow opacity/scale transitions in (not just appears instantly).
- Links get a decorative underline (thicker, offset below the baseline) rather
  than the browser default.
- Custom text-selection color: dark background, white text (inverted from body).
- Responsive: card size shrinks below the ~768px breakpoint; layout still needs
  to work on mobile.

## Content needed per project (the big lift)
- **A custom illustration or icon** — not a screenshot or photo. This is the
  single biggest content gap versus the current site: every project needs
  original artwork, which has to be sourced or commissioned per project
  (illustration style TBD — nick.computer's are flat, colorful, hand-drawn).
- Project title.
- Short one-line teaser (shown on the card).
- Case-study body copy for the detail page.
- Small tech/tool icon set per project (e.g. React, Figma, etc. logos).

## Open questions to resolve before/while building
- **Illustration source**: hand-drawn commissioned art, AI-generated, or a
  simplified icon-based placeholder system to start?
- **Self-publish system**: the previous mosaic had a password + GitHub-token
  gated in-browser editor that committed uploads straight to the repo via
  GitHub's API. Does that get carried over for editing card art/copy, or does
  this version go back to plain hand-authored content (simpler, since the
  project count is now small and curated rather than dozens of tiles)?
- **Number of projects** to feature at launch.
- **Case-study copy** — needs actual project write-ups, not placeholder text.

## What this replaces
Dropping entirely: the 10-tile square mosaic grid, the framed lightbox
editor, drag-and-drop image upload UI, and (pending the question above) the
password/GitHub-token self-publishing flow. The GitHub Pages hosting setup
(`nouillepascuite/Portfolio-Xavier-Dersy`, deployed via GitHub Pages from
`main`) stays — only the page's design and content model change.
