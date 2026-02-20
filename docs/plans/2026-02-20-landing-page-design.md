# Landing Page Design: nectamen.com

**Date:** 2026-02-20
**Status:** Approved

---

## Overview

**Domain:** `nectamen.com`
**Title:** 焚而不燬
**Subtitle:** Nec Tamen Consumebatur — 台灣民主化關鍵十年 1980–1989
**Positioning:** A memorial hall entrance — a single landing page that guides visitors to four interactive historical documentary sites about Taiwan's journey from authoritarianism to democracy.

### Concept Origin

"Nec Tamen Consumebatur" (焚而不燬) comes from the Presbyterian Church of Taiwan's motto, drawn from Exodus 3:2 — the burning bush that was not consumed. It symbolizes:

- Nylon Deng's self-immolation for freedom of speech
- The democratic movement that survived authoritarian oppression
- The Presbyterian Church's role in Taiwan's democracy movement

---

## Target Audience

- Taiwanese general public
- Primary language: Traditional Chinese
- People interested in history but not necessarily familiar with White Terror details

---

## The Four Sites

| Project | Event | Year | URL |
|---------|-------|------|-----|
| the-lin | 林宅血案 | 1980 | soanseng.github.io/the-lin/ |
| Chen-Wen-chen | 陳文成事件 | 1981 | soanseng.github.io/Chen-Wen-chen/ |
| henry-liu-case | 江南案 | 1984 | soanseng.github.io/henry-liu-case/ |
| nylon | 鄭南榕事件 | 1989 | soanseng.github.io/nylon/ |

All four are React + TypeScript + Vite + Tailwind + PixiJS interactive scrollytelling documentaries, sourced from declassified government documents.

---

## Page Structure (Single Page, Top to Bottom)

### Hero Section

- Title: 焚而不燬
- Subtitle: Nec Tamen Consumebatur
- Tagline: 台灣民主化關鍵十年 1980–1989
- Visual: Burning bush silhouette with subtle warm glow on dark background

### Introduction

2-3 sentences:

> 1980到1989，四條生命、四個案件，燒出了台灣通往自由的路。
> 本系列以政府解密檔案為基礎，不做政治評論，只呈現歷史。

### Four Cases (Vertical Timeline)

Each case displayed as a memorial plaque:

1. **1980 — 林宅血案** (林義雄)
   - One-line description + link to site
2. **1981 — 陳文成事件** (陳文成)
   - One-line description + link to site
3. **1984 — 江南案** (劉宜良)
   - One-line description + link to site
4. **1989 — 鄭南榕事件** (鄭南榕)
   - One-line description + link to site

### Footer

- Source statement: government declassified archives
- License: MIT
- GitHub: soanseng

---

## Visual Design: Memorial Hall Entrance

### Color Palette

- Background: Dark stone texture (#1a1a1a ~ #2d2d2d) — black granite wall feel
- Text: Off-white (#e8e4df) — aged parchment tone
- Accent: Warm amber/orange (#c4721a) — subtle flame glow
- Timeline: Muted gold (#8b7355) — bronze-like
- Hover state: Soft warm glow around cards

### Typography

- Latin title: Serif font (e.g., Playfair Display or similar)
- Chinese body: Noto Serif TC
- UI elements: Noto Sans TC

### Imagery

- Hero: Burning bush silhouette — static, subtle gradient glow (no animation)
- Cards: Memorial plaque style — slightly raised, stone-like texture
- Hover: Cards glow faintly, as if lit by firelight
- Overall: Minimal decoration, whitespace = solemnity

---

## Technical Decisions

| Item | Choice | Rationale |
|------|--------|-----------|
| Framework | Pure HTML + CSS + minimal JS | Single navigation page, no React overhead. Best SEO, fastest load |
| Deployment | GitHub Pages | Consistent with all four sub-sites |
| Domain | nectamen.com → GitHub Pages CNAME | Custom domain with DNS configuration |
| Favicon | Burning bush simplified icon (SVG) | Matches theme |

---

## SEO Strategy

### Meta Tags

- `<title>`: 焚而不燬 — 台灣民主化關鍵十年 1980–1989
- `<meta name="description">`: 四個改變台灣的案件：林宅血案、陳文成事件、江南案、鄭南榕事件。以政府解密檔案為基礎的互動式歷史紀錄。
- `<meta name="keywords">`: 台灣歷史, 白色恐怖, 轉型正義, 林宅血案, 陳文成, 江南案, 鄭南榕, 民主化, 戒嚴

### Open Graph

- og:title: 焚而不燬 — 台灣民主化關鍵十年
- og:description: (same as meta description)
- og:image: 1200x630 sharing image (burning bush motif)
- og:type: website
- og:url: https://nectamen.com

### Structured Data

- `WebSite` schema for the landing page
- `ItemList` schema linking to the four sub-sites

### Files

- `sitemap.xml` with links to all four sub-sites
- `robots.txt` allowing full indexing

---

## File Structure

```
nectamen/
├── index.html
├── style.css
├── script.js              # minimal interactions (if needed)
├── CNAME                  # nectamen.com
├── favicon.svg            # burning bush icon
├── og-image.png           # Open Graph sharing image
├── sitemap.xml
├── robots.txt
├── .github/
│   └── workflows/
│       └── deploy.yml     # GitHub Pages auto-deploy
├── docs/
│   └── plans/
│       └── 2026-02-20-landing-page-design.md
├── CLAUDE.md
├── README.md
├── LICENSE                # MIT
└── .gitignore
```

---

## Out of Scope

- No React / Vite / build step
- No multi-page routing
- No comments system
- No analytics (unless user requests later)
- No English translation (Chinese-primary for now)
