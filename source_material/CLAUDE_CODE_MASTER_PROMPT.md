# Claude Code Master Prompt

You are implementing a real production-quality interactive digital wedding invitation for **Enis & Zainab**.

This is **not** a generic template demo. It must feel like a bespoke, premium, luxury invitation designed primarily for **smartphone viewing**, especially **iPhone Safari**.

## Inputs available in this folder
- `PROJECT_BRIEF.md`
- `WEDDING_DATA.json`
- `CONTENT_COPY.md`
- `IMPLEMENTATION_NOTES.md`
- `reference_images/`

## What the reference images mean
- `01` to `09` show the **luxury reference reel** and define the **interaction flow, quality bar, layout mood, and premium design language**.
- `10_custom_design_from_zainab.jpg` is the **content and conceptual base** created by the bride. It must be respected and translated into the interactive experience, not merely displayed as a static image.

## Main task
Build the complete invitation as a **static mobile-first web experience** using plain HTML, CSS, and JavaScript unless a dependency provides clear value.

### Strong constraints
- Prefer a **single portable self-contained HTML** or a tiny static bundle.
- No backend required.
- No framework required.
- No Three.js.
- No over-engineering.
- The invitation should work when opened locally and also be easy to host later as a normal link.
- Keep Arabic text as real HTML text, not baked into raster images.
- Use tasteful CSS/SVG ornamentation rather than overcomplicated graphics.
- Animations must feel slow, elegant, soft, and physical.

## Desired user experience
1. Full-screen **cream-colored embossed envelope** appears.
2. A **gold wax seal** with `E & Z` is centered.
3. User taps the seal.
4. Envelope opens with subtle glow/light effect.
5. Background music can begin from this user interaction.
6. Main invitation experience appears.
7. A premium hero/welcome section introduces Enis & Zainab.
8. A **scratch-to-reveal date** section lets the user rub away gold fields to reveal:
   - `02`
   - `Oktober`
   - `2026`
9. An elegant invitation content section presents:
   - Bismillah
   - Qur'an verse from Ar-Rum 30:21
   - Qur'an verse from An-Naba 78:8
   - German translation `„Und Wir haben euch als Paare erschaffen.“`
   - Event keyfacts
   - Enis & Zainab names
10. Include a **fingerprint concept section** inspired by the bride's design:
   - Groom fingerprint + Bride fingerprint = union / heart motif
   - Use stylized decorative fingerprints, not real biometric prints
11. Add a **wedding timeline** section.
12. Add a **live countdown** section.
13. Add a **location** section with button to open Google Maps.
14. Add a **dresscode** section with pastel swatches.
15. Add a simple **RSVP** area.
16. Add a floating **audio button** at the bottom-right.

## Design direction
- Background: off-white / cream paper
- Accents: champagne gold
- Text: deep espresso
- Style: refined luxury, not tacky
- Use subtle embossed paper textures and floral/oriental decorative motifs
- Use arches, soft floral corners, lantern hints, and tiny shimmering particles sparingly
- More white space than the reference reel if it improves elegance
- Premium typography is crucial

## Technical requirements
- Mobile-first responsive layout
- Smooth scrolling
- Touch support everywhere needed
- Scratch cards must support touch and mouse
- Use proper high-DPI canvas handling
- Countdown target must be based on `2026-10-02T19:30:00+02:00`
- Make key text/data editable from one central config/data object

## RSVP requirement
For version 1, keep RSVP lightweight.
A simple CTA that opens WhatsApp or an email draft is acceptable if a full backend form is unnecessary.

## Critical instruction about quality
Do not stop after writing code.
You must:
1. Build the invitation.
2. Run it locally.
3. Inspect the result visually.
4. Compare it against the reference reel images and the bride's design.
5. Identify what still feels cheap, generic, too cluttered, or insufficiently premium.
6. Iterate until the result feels polished and bespoke.

## Output expectation
Produce the implementation files and iterate until the invitation is visually strong.
If you create assets, keep the project simple and portable.
