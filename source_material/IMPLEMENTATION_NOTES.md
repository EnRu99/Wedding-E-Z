# Implementation Notes

## Strong recommendation
Build this as a **static mobile web invitation** with:
- `index.html`
- `styles.css`
- `app.js`

Or, if desired, as a single-file self-contained `index.html`.

## Core interactions

### 1) Envelope open
- full-screen envelope intro
- embossed floral details
- centered wax seal with `E & Z`
- tap gesture opens top flap
- subtle glow and scale animation
- after open: smooth transition to main content

### 2) Scratch cards
- use HTML5 canvas per field or one canvas per card
- support touch + mouse
- use high DPI scaling for crisp rendering
- reveal values:
  - 02
  - Oktober
  - 2026
- once a threshold is scratched, auto-clear remaining overlay for delight

### 3) Countdown
- target `2026-10-02T19:30:00+02:00`
- show days / hours / minutes / seconds
- update every second

### 4) Audio button
- floating circular button bottom-right
- music must start only from a user action (e.g. seal tap) due to iPhone browser restrictions
- button toggles mute/play

### 5) Location
- if a live iframe is inconvenient in local-file mode, provide at minimum:
  - location name
  - open in Google Maps button
- hosted version can optionally show an embedded map

## Recommended fonts
- elegant serif for body / headings
- calligraphic/script font for names
- Arabic font such as Amiri or Noto Naskh Arabic

## Performance / UX
- keep animations elegant and light
- no heavy 3D libraries
- prefer CSS and SVG ornaments
- use white space generously
- make all section spacing feel premium and calm

## Visual caution
Avoid over-decorating. The reel is rich, but Enis wants a more refined and slightly simpler luxury feel.
