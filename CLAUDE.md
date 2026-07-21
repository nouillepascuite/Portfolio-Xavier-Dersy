# Portfolio Mosaic

Early-web / Web 1.0 style single-page portfolio built in Claude Design (`Portfolio Mosaic.dc.html`).

## Concept
- "Beginning of the internet" aesthetic: minimalistic, white background.
- One screen, **no scrolling ever** — everything must fit the viewport.
- Title text: "Portfolio and current projects".

## Layout
- 10x10 mosaic grid (100 tiles), one per project.
- Tiles are perfect **squares** (1:1), not rectangles, with a small 6px gap between them.
- Grid stays centered on screen.
- No divider line between the title and the mosaic.

## Tile content
- Each tile holds an image or GIF for a project.
- Animated GIFs must stay animated (not frozen to a static frame).

## Click interaction
- Clicking a tile opens a **centered framed lightbox** (not fullscreen, not a side panel).
- Lightbox contains:
  - Editable title
  - Editable description
  - A thumbnail gallery — main image plus up to 5 additional gallery shots
  - Add images via click-to-upload or drag-and-drop
  - Arrow navigation to move between projects without closing the lightbox

## Data & persistence
- All content (images, titles, descriptions) is edited in place and **persists locally in the browser** (no backend).
- A tweak panel exists to change the accent color and toggle visibility of tile numbers.

## Revision history (from design chat)
1. Initial build: 10x10 mosaic, framed lightbox, local persistence, GIF support.
2. Changed tiles from rectangles to squares, added 6px gap.
3. Removed the straight divider line between the name and the mosaic.
