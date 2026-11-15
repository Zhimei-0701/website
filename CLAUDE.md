# Portfolio site — project brief

Personal-brand portfolio for Zhimei. English only. Content: resume (experience, projects) + life section.

## Status
- Decided: purpose, style, motion level, language, stack, hosting.
- Next: content skeleton (About / Experience / Projects / Life / Contact) → static style sample for sign-off → asset prompts → build → QA & launch.
- Done: repo `zhimei-0701/website` created; folder + content skeleton in `content/*.md` (TODO placeholders).
- Open: Life section contents; fill in content TODOs; deploy target — repo is named `website`, not `<username>.github.io`, so either rename it or serve as a project site under `/website/` (set Vite `base`).

## Visual direction
East-Asian editorial magazine collage, warm "candle-flame" feel.
- Oversized high-contrast serif titles (Bodoni Moda / Playfair Display) layered with the subject (subject overlaps letters).
- Vertical CJK text strips as texture; issue numbers, barcodes, crosshair "+" marks, dot grids, wide-tracked small caps.
- Cut-out photo frames + line-drawn botanicals + ink-wash + gold rules, all on a strict hidden grid.
- Beige paper texture background, never pure white.

### Palette (draft — confirm in style sample)
| token | hex | use |
|---|---|---|
| --aubergine | #3B2352 | primary |
| --violet | #6B4A8A | secondary |
| --gold | #B08D57 | accent, rules, seal |
| --paper | #EFE6D2 | background |
| --ink | #1F1A24 | body text |

## Motion (close to thibaultguignand.com)
- Homepage: full-screen video carousel; hovering a project swaps video via noise block-reveal + warp + chromatic aberration peaking mid-transition.
- Cursor flowmap distortion on titles/hero images; directional RGB split; idle guard stops rAF after ~90 frames.
- Text reveal everywhere: SplitText + scramble + left-to-right clip-path wipe, one shared utility.
- Project page footer: "Next project" scroll morph (unclip + scale + 0→100 ring), auto-navigate with guards; also clickable.
- Page transitions: staged GSAP fade + View Transition API (wrap navigate in flushSync); preload next chunk + hero on click.
- Grid overlay toggle (Cmd/Ctrl+G). Full `prefers-reduced-motion` alternate design.
- Pattern: every WebGL effect driven by one GSAP-tweened `progress` uniform; per-frame work via direct DOM writes, not React state.

## Stack
Vite + React 18 + TypeScript, GSAP (SplitText, ScrollTrigger, ScrambleText), OGL, Lenis (synced to GSAP ticker), SCSS + BEM.

## Hosting
GitHub Pages only (no Vercel). Repo `<username>.github.io`, deploy via GitHub Actions (Settings → Pages → Source: GitHub Actions). Copy `index.html` → `404.html` for SPA route fallback. Keep videos short, compressed (a few MB each); no file over 100 MB.

## Folders
```
assets/hero/            hero portrait collage
assets/texture/         paper, grain
assets/decor/           seals, line botanicals, ink wash, gold lines (transparent PNG)
assets/projects/<name>/ covers, screenshots, loop videos
assets/life/            life photos
content/                resume + life copy (md)
```
