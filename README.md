# Julie Training — Website

Personal training landing page for Julie — NASM CPT, IFBB competitor, Seattle.

**Live site:** https://julie-training.netlify.app *(update after first deploy)*

---

## Stack
- Pure HTML/CSS/JS — single file, zero dependencies, no build step
- Photo embedded as base64 (no external image hosting needed)
- Hosted on Netlify (free tier)

## Local Preview
Just open `index.html` in any browser. No server needed.

## How to Update

### Update prices, text, or any content:
Edit `index.html` directly. Search for the section you want:
- `<!-- ══ HERO ══ -->` — name, tagline, credentials
- `<!-- ══ ABOUT ══ -->` — bio, stats
- `<!-- ══ PRICING ══ -->` — all prices and packages
- `<!-- ══ TESTIMONIALS ══ -->` — client quotes
- `<!-- ══ FOOTER ══ -->` — contact info, Instagram handle

### Update the photo:
1. Convert new photo to base64: `base64 -i photo.png | tr -d '\n'`
2. In `index.html`, find `<img src="data:image/png;base64,...`
3. Replace the base64 string with the new one

### Deploy to Netlify:
**Option A — Drag & Drop (easiest):**
1. Go to https://netlify.com → Log in
2. Drag the `index.html` file onto the deploy zone
3. Done — live in ~30 seconds

**Option B — Auto-deploy from GitHub (recommended for ongoing updates):**
1. Push this repo to GitHub
2. In Netlify → "New site from Git" → connect repo
3. Build command: *(leave blank)*
4. Publish directory: `.` (or leave blank)
5. Every `git push` auto-deploys

## Customization Checklist
- [ ] Update Instagram handle `@Julie_fit` with real handle (search `Julie_fit` in file)
- [ ] Add real booking link to "Book a Session" button (search `#contact`)
- [ ] Update testimonials with real client quotes when available
- [ ] Update stats (years training, clients coached) in About section
- [ ] Confirm certification name (currently listed as NASM — update if different)
- [ ] Update copyright year if needed

## File Structure
```
julie-training-site/
├── index.html      ← entire site (single file)
├── README.md       ← this file
└── .gitignore
```
