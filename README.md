# Kamari Flanagan — The Feature (portfolio)

Cinematic one-page portfolio. Academy countdown leader → click to lift the screen →
three "scenes" (your live sites) → end credits. Standalone static site (no runtime),
just `index.html` + Google Fonts. Drops onto GitHub Pages at the repo root.

## Boot sequence
- Film **countdown leader** (4→1) with sweeping hand + rolling sprockets.
- Then **"Click anywhere to roll the film"** — a click (or Enter/Space) lifts the
  screen up and reveals the hero.
- **Runtime timer** (bottom-left, `RUNTIME 00:00:00`) counts how long the page has
  been open. Reduced-motion users skip straight to the click prompt.

## Deploy (your usual flow)
1. Drop this folder's contents into the repo root (GitHub Desktop / VS Code).
2. Push → Settings → Pages → deploy from branch → root.
3. Hard-refresh (Ctrl/Cmd + F5) if an old version is cached.

## Add / edit a project (one place)
In `index.html`, edit the `SCENES` array near the bottom:

```js
{ name:"New Project", href:"https://url/", meta:"Service site · live · 2026",
  stack:"HTML · CSS · JS", frame:true }   // frame:false = film-slate only
```

Order = scene number (first = SCENE 01).

## Notes
- Previews iframe the live site (desktop only, loads on scroll). If a site blocks
  framing (`X-Frame-Options`), the striped film-slate shows instead and the panel
  still links out. Set `frame:false` to force slate-only.
- Mobile skips iframes (slate + "OPEN THE SITE", tap opens the real site).
- Colors/fonts live in the `:root` block at the top of `index.html`.
- Credits link the résumé + AWS cert PDFs in this folder — swap files to update.

## Files
- `index.html` — the whole site
- `Kamari-Flanagan-Resume.pdf`
- `AWS-Cloud-Practitioner.pdf`
