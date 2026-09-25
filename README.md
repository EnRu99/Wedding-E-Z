# Enis & Zainab — Digital Wedding Invitation

An interactive, mobile-first wedding invitation for the Nikah of Enis & Zainab
(Freitag, 02.10.2026, 19:30 Uhr, Islamisches Zentrum Zürich).

The guest sees a sealed envelope, taps the E & Z wax seal to open it, and then
scrolls through the invitation: welcome, scratch-to-reveal date, Bismillah and
Qur'an verses, invitation text with the fingerprint union, timeline, live
countdown, location, dresscode and RSVP.

## It is a static site

- `index.html`: the whole invitation (HTML, CSS and JavaScript in one file)
- `assets/fonts/`: self-hosted fonts (Great Vibes, Cormorant Garamond, Amiri Quran; all SIL Open Font License)
- `assets/README_AUDIO.txt`: how to add music later
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
`index.html`. It holds the names and monogram, the date and time (`event.start`
is the countdown target, `2026-10-02T19:30:00+02:00`), the venue, the scratch
fields, the timeline, the dresscode colours, the RSVP contact and the music.
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

## Music (intentionally absent)

No music file is included yet, and none is loaded. The music button stays
hidden. To add music later, put the file at `./assets/music.mp3` and set
`music.src: './assets/music.mp3'` in the `WEDDING` config. Playback then starts
with the seal tap, and a play/pause button appears. See
`assets/README_AUDIO.txt` for details.

## Still to be configured

- **RSVP**: no contact was supplied, so the reply buttons are hidden and a
  dashed "Vorschau-Hinweis" box marks the gap. Fill in `rsvp.whatsapp`
  (international digits, e.g. `41791234567`) and/or `rsvp.email` to show the
  buttons. They open a pre-filled WhatsApp message or e-mail. There is no
  backend and no fake form.
- **Location**: the Maps button searches "Islamisches Zentrum Zürich". For
  certainty, paste the exact Google Maps share link into `location.mapsUrl`.

## Publishing (later, only after approval)

Nothing is deployed. GitHub Pages is not configured, and there is no deployment
workflow. When the design is approved, the plan is to serve these static files
with GitHub Pages so guests get one HTTPS link to share on WhatsApp.
