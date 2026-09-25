# Project Brief — Interactive Digital Wedding Invitation

## Context
There are two sources of truth:

1. **Luxury reference reel**
   - defines interaction style, visual quality, flow, and overall premium feel
   - includes envelope opening, scratch-to-reveal date, timeline, countdown, map, dress code, and floating audio button

2. **Zainab's custom design**
   - defines the actual invitation content direction
   - should be used as the conceptual/content base for the custom invitation
   - should not just be shown as a static image; it should be rebuilt beautifully as part of the digital experience

## Main objective
Create a **smartphone-first interactive invitation** that feels like a bespoke luxury wedding web app while remaining technically simple.

## Technical constraints
- Prefer **one portable self-contained HTML file** or a tiny static bundle
- No framework required
- No build step required if possible
- No backend required
- Invitation must run locally in browser and also be easy to host later if desired
- Optimize for **iPhone Safari**

## Design direction
- Cream / off-white background
- Champagne gold accents
- Dark espresso text
- Elegant Arabic calligraphy sections
- Soft embossed paper feeling
- Oriental arch motifs
- Hanging lantern details
- Soft glitter / gold particle atmosphere (subtle, not cheesy)
- Premium typography and spacing
- High white-space usage
- Slow, elegant, physical-feeling animations

## Non-goals
- Do not build a generic wedding template
- Do not over-engineer with React/Next.js/Three.js
- Do not make it look like SaaS UI
- Do not copy the reel literally; reinterpret it for Enis & Zainab

## UX flow
1. Intro envelope screen fills viewport
2. User taps wax seal
3. Envelope opens with glow/light animation
4. Hero section / welcome section appears
5. Scroll reveals scratch date section
6. Scroll reveals core invitation card with Arabic/German content
7. Fingerprint concept section
8. Timeline section
9. Countdown section
10. Location section
11. Dresscode section
12. RSVP / contact section
13. Floating audio player persists

## Fingerprint concept
Keep the idea from Zainab's design:
- Groom print + Bride print = joined symbol / heart / union motif
- Use **stylized vector fingerprints**, not real biometric fingerprints

## Hosting / portability
The output should be deliverable as:
- a single portable HTML for local opening
- or the same static project uploaded later for a normal web link
