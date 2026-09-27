# Enis & Zainab — Digital Wedding Invitation

An interactive, mobile-first wedding invitation for the Nikah of Enis & Zainab
(Freitag, 02.10.2026 · 20. Rabīʿ ath-Thānī 1448, 19:30 Uhr): Trauung im Islamischen
Zentrum Zürich, anschliessend Apéro am Kurt-Früh-Weg 4, 8050 Zürich.

The guest sees a sealed envelope, taps the E & Z wax seal to open it, and then
scrolls through the invitation: a framed floral welcome page with their childhood photo,
scratch-to-reveal date, Bismillah and Qur'an verses, invitation text with the
fingerprint union, timeline, live countdown, location and a short Rückmeldung
note. Soft background music starts with the seal tap.

## It is a static site

- `index.html`: the whole invitation (HTML, CSS and JavaScript in one file)
- `assets/fonts/`: self-hosted fonts (Great Vibes with a Petit Formal Script "Z", Cormorant Garamond, Amiri Quran; all SIL Open Font License)
- `assets/images/enis-zainab-kindheit.jpg`: the childhood photo on the welcome page
- `assets/images/og-einladung.jpg`: link preview image (WhatsApp etc.)
- `assets/music.mp3`: background music (see `assets/README_AUDIO.txt`)
- `source_material/`: the original brief, content copy and reference images (not used by the page)

There is no framework, no build step, no backend and no `npm install`. All paths
are relative (`./assets/...`), so the same files work locally and under a
GitHub Pages project path such as `/Wedding-E-Z/`.

## Preview locally

Either double-click `index.html`, or (recommended, closer to real hosting) run a
tiny static server in the repository folder:

```bash
python3 -m http.server 8080
```

Then open <http://localhost:8080/>. To try it on your phone, open
`http://<your-computer's-LAN-IP>:8080/` while both devices are on the same Wi-Fi.
Use the browser's device toolbar at 390 × 844 for an iPhone-like view on a desktop.

The envelope appears on every fresh load. Reload the page to see it again.

## Where to edit the event data

All wedding data lives in one object, `window.WEDDING`, at the top of
`index.html`. It holds the names and monogram, the date, Hijri date and time
(`event.start` is the countdown target, `2026-10-02T19:30:00+02:00`), the scratch
fields, the timeline, both locations (`location.ceremony`, `location.apero` with the
parking note), the Rückmeldung sentence and the music settings. The E & Z seal
monogram is fixed SVG artwork (`#mono-glyphs`).
The Qur'an text itself is kept verbatim in the HTML, taken from
`source_material/CONTENT_COPY.md`.

## How the scratch cards work

Each of the three date cards has a `<canvas>` painted with a brushed
champagne-gold coating (high-DPI aware). Pointer Events (touch, mouse and pen)
erase the coating under the finger with a soft round brush
(`destination-out`). Only the cards themselves capture touches, so scrolling
anywhere else stays normal. Every ~140 ms, and when the finger lifts, a
sampled pixel check measures how much is cleared. At about 55 % the remaining
foil fades away. When all three are revealed, a single soft gold shimmer runs
across the date. **Datum vollständig anzeigen** reveals everything without
dragging, for accessibility.

## Music

`assets/music.mp3` never plays on page load. It starts when the guest taps the
wax seal (browsers, especially iPhone Safari, only allow sound after a tap),
fades in softly and loops. A small play/pause button then appears in the
bottom-right corner. If a browser blocks playback, the invitation still opens
and the button lets the guest start the music. Settings are in `WEDDING.music`
(`src: ''` switches the music off). See `assets/README_AUDIO.txt`.

## Still to be configured

- **Maps**: the two Maps buttons search for "Islamisches Zentrum Zürich" and
  "Kurt-Früh-Weg 4, 8050 Zürich". To point at an exact place, paste a Google
  Maps share link into `location.ceremony.mapsUrl` / `location.apero.mapsUrl`.

## Publishing with GitHub Pages

The repository is ready. `.github/workflows/pages.yml` publishes only
`index.html` and `assets/` (never `source_material/`), and `.nojekyll` makes
GitHub serve the files unchanged. The page has `noindex`, so search engines
leave it alone.

One step in GitHub has to be done by the repository owner:

1. GitHub Pages needs either a **public** repository or a paid plan (GitHub Pro).
   This repository is currently private.
2. Open **Settings → Pages** and under *Build and deployment → Source* choose
   **GitHub Actions**.
3. Open **Actions → Publish invitation → Run workflow** once. After that, every
   push to the branch updates the site automatically.

The invitation is then at **https://enru99.github.io/Wedding-E-Z/**. The link
preview image in `index.html` (`og:image`) points to that address; if the site
ends up somewhere else, update the two `og:` URLs.
