# Higgsfield — Premium Art Themes (10 backgrounds)

Goal: 10 "premium art" themes on top of the 24 flat themes → ~34 total, curated
(decision: NOT 50 — choice paralysis kills conversion; every theme must look
premium or it hurts trust).

## Two ways to run this

- **Option A (Claude drives):** Mario opens higgsfield.ai in the Claude browser
  panel, logs in himself, says "logged in". Claude generates everything.
- **Option B (Mario pastes):** generate one image per prompt below, download
  the highest resolution, drop files into `~/makewelcomebook/art/` named
  `01-botanical.png`, `02-boho-arch.png`, … Claude integrates them.

## Global rules — append to EVERY prompt

> vertical portrait 3:4, soft muted colors, large calm empty area in the center
> for text overlay, edges decorated only, flat matte illustration, high
> resolution, no text, no letters, no words, no watermark, no people

(If Higgsfield offers aspect ratio settings, use 3:4 portrait, largest size.)

## The 10 prompts

1. **01-botanical** — delicate watercolor eucalyptus branches and soft green
   leaves framing the corners of a cream paper background, airy, minimal
2. **02-boho-arch** — terracotta boho arches and hand-drawn sun, warm beige
   background, abstract shapes in corners only, earthy tones
3. **03-coastal** — soft watercolor ocean waves and sandy beach tones along the
   bottom edge, pale blue sky, breezy and calm
4. **04-wildflowers** — pressed wildflower meadow illustration along bottom and
   top edges, muted pastel colors, vintage botanical style
5. **05-citrus** — Mediterranean lemon branches with leaves in two corners,
   white-cream background, Amalfi tile accent along bottom edge
6. **06-mountain** — minimal line-art mountain range and pine trees along the
   bottom edge, misty sage green and grey tones
7. **07-tropical** — watercolor palm leaves and monstera framing top corners,
   soft sandy background, relaxed resort feeling
8. **08-desert** — desert sunset with cactus silhouettes along bottom edge,
   dusty rose and clay gradient sky, minimal
9. **09-vineyard** — watercolor grapevine and olive branches along the side
   edges, Tuscan cream background, rustic elegant
10. **10-toile** — vintage French garden toile pattern as a light border frame,
    single accent color on cream, classic and refined

## Integration (Claude's job once images exist)

- Each art theme = new THEMES entry with `art:"art/01-botanical.png"` +
  matching palette; cover renders image as background layer, inner pages get a
  subtle strip/corner of the same art.
- Compress to ~200-400KB each (target: whole site under 5MB).
- Landing page gets an "art themes" showcase row + count update.
