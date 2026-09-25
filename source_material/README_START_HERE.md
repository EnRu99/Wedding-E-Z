# Enis & Zainab — Claude Code Pack

This ZIP contains the source brief, the master prompt, the wedding data, and the visual references needed to build the interactive digital wedding invitation in Claude Code.

## Goal
Build a **mobile-first, premium interactive wedding invitation** that captures the luxury feel of the reference reel while preserving the **content and intent** of Zainab's custom design.

## What Claude Code should build
A **single self-contained HTML invitation** (or as close as practical), with CSS and JavaScript, optimized for iPhone Safari.

### Core experience
1. Envelope intro with wax seal `E & Z`
2. Tap seal to open envelope
3. Smooth transition to main invitation
4. Scratch cards to reveal `02 | Oktober | 2026`
5. Invitation content with Arabic and German text
6. Fingerprint concept section (stylized, not real biometric prints)
7. Wedding timeline
8. Live countdown
9. Location section with map/open in Google Maps
10. Dresscode section with pastel palette
11. Optional RSVP section
12. Floating audio control

## Important product decision
The first deliverable should work as a **portable static experience**:
- no backend required
- no framework required
- opening locally should work
- later it can be uploaded anywhere as a normal link

## Suggested order inside Claude Code
1. Read `PROJECT_BRIEF.md`
2. Read `WEDDING_DATA.json`
3. Read `CLAUDE_CODE_MASTER_PROMPT.md`
4. Inspect the images in `reference_images/`
5. Build the invitation
6. Run it locally and iterate visually until it feels premium

## Files in this pack
- `CLAUDE_CODE_MASTER_PROMPT.md` → the main prompt to paste into Claude Code
- `PROJECT_BRIEF.md` → clarified requirements and constraints
- `WEDDING_DATA.json` → structured editable data
- `CONTENT_COPY.md` → copy/text content for the invitation
- `IMPLEMENTATION_NOTES.md` → technical guidance
- `reference_images/` → reel references + Zainab's design
