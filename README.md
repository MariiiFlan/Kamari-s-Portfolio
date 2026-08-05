# Kamari Flanagan — The Feature (portfolio)

Cinematic one-page portfolio. Film-reel intro → three "scenes" (your live sites) → end credits.
Ported from the Claude Design bundle into a **standalone static site** — no React/runtime, just
`index.html` + Google Fonts. Drops straight onto GitHub Pages.

## Deploy (your usual flow)
1. Drop this folder's contents into the repo root (GitHub Desktop / VS Code).
2. Push. Settings → Pages → deploy from branch → root.
3. Hard-refresh (Ctrl/Cmd + F5) if an old version is cached.

Root `index.html` = it loads at the repo root URL. No build step.

## Add / edit a project (one place)
Open `index.html`, find the `SCENES` array near the bottom, add an object:

```js
{
  name: "New Project",
  href: "https://your-live-url/",
  meta: "Service site · live · 2026",   // right-side caption
  stack: "HTML · CSS · JS",             // bottom-right label
  frame: true                            // true = live iframe preview; false = slate only
}
```

Order = scene number (first object is SCENE 01). That's the whole edit.

## Notes
- **Previews:** each panel iframes the live site (desktop only, loads when scrolled into view).
  If a site blocks framing (custom domain w/ `X-Frame-Options`), the striped "film slate"
  shows instead — the panel still links out. Set `frame:false` to force slate-only.
- **Mobile:** no iframes (saves data) — slate + "OPEN THE SITE", tap opens the real site.
- **Assets:** `Kamari-Flanagan-Resume.pdf` and `AWS-Cloud-Practitioner.pdf` are linked in the
  end credits. Swap the files to update.
- **Colors/fonts:** the `:root` block at the top of `index.html` is the single source of truth.

## Files
- `index.html` — the whole site
- `Kamari-Flanagan-Resume.pdf` — linked in credits
- `AWS-Cloud-Practitioner.pdf` — linked in credits
