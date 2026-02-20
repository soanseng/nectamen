# nectamen.com Landing Page Implementation Plan

> **For Claude:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task.

**Goal:** Build a single-page memorial-hall-style landing page at nectamen.com that links to four Taiwan White Terror interactive documentary sites.

**Architecture:** Pure HTML + CSS + minimal JS. No build step, no framework. Static files served directly via GitHub Pages with custom domain. The page has three sections: hero, timeline cards, footer.

**Tech Stack:** HTML5, CSS3 (custom properties, grid, flexbox), vanilla JS (optional hover effects), GitHub Pages, Google Fonts (Noto Serif TC, Noto Sans TC, Playfair Display).

---

### Task 1: Project Scaffolding

**Files:**
- Create: `CNAME`
- Create: `.gitignore`
- Create: `LICENSE`
- Create: `README.md`
- Create: `CLAUDE.md`

**Step 1: Create CNAME**

```
nectamen.com
```

**Step 2: Create .gitignore**

```
.DS_Store
*.swp
*~
.vscode/
.idea/
```

**Step 3: Create LICENSE (MIT)**

Standard MIT license with copyright `2026 soanseng`.

**Step 4: Create README.md**

```markdown
# 焚而不燬 — Nec Tamen Consumebatur

台灣民主化關鍵十年 1980–1989

Landing page for four interactive historical documentaries:

- [林宅血案 (1980)](https://soanseng.github.io/the-lin/)
- [陳文成事件 (1981)](https://soanseng.github.io/Chen-Wen-chen/)
- [江南案 (1984)](https://soanseng.github.io/henry-liu-case/)
- [鄭南榕事件 (1989)](https://soanseng.github.io/nylon/)

## Development

Open `index.html` in a browser. No build step required.

## License

MIT
```

**Step 5: Create CLAUDE.md**

```markdown
# nectamen.com

Landing page for Taiwan White Terror documentary series.

## Tech

- Pure HTML + CSS + minimal JS
- No build step, no framework
- Deployed via GitHub Pages with custom domain nectamen.com

## Files

- `index.html` — single page, all content
- `style.css` — all styles
- `favicon.svg` — burning bush icon

## Design

See `docs/plans/2026-02-20-landing-page-design.md`
```

**Step 6: Commit**

```bash
git add CNAME .gitignore LICENSE README.md CLAUDE.md
git commit -m "chore: project scaffolding"
```

---

### Task 2: HTML Structure

**Files:**
- Create: `index.html`

**Step 1: Write index.html with full semantic structure**

```html
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Primary Meta Tags -->
  <title>焚而不燬 — 台灣民主化關鍵十年 1980–1989</title>
  <meta name="description" content="四個改變台灣的案件：林宅血案、陳文成事件、江南案、鄭南榕事件。以政府解密檔案為基礎的互動式歷史紀錄。">
  <meta name="keywords" content="台灣歷史, 白色恐怖, 轉型正義, 林宅血案, 陳文成, 江南案, 鄭南榕, 民主化, 戒嚴">
  <meta name="author" content="soanseng">

  <!-- Open Graph -->
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://nectamen.com/">
  <meta property="og:title" content="焚而不燬 — 台灣民主化關鍵十年">
  <meta property="og:description" content="四個改變台灣的案件：林宅血案、陳文成事件、江南案、鄭南榕事件。以政府解密檔案為基礎的互動式歷史紀錄。">
  <meta property="og:image" content="https://nectamen.com/og-image.png">
  <meta property="og:locale" content="zh_TW">

  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="焚而不燬 — 台灣民主化關鍵十年">
  <meta name="twitter:description" content="四個改變台灣的案件：林宅血案、陳文成事件、江南案、鄭南榕事件。以政府解密檔案為基礎的互動式歷史紀錄。">
  <meta name="twitter:image" content="https://nectamen.com/og-image.png">

  <!-- Favicon -->
  <link rel="icon" type="image/svg+xml" href="favicon.svg">

  <!-- Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Noto+Serif+TC:wght@400;700&family=Noto+Sans+TC:wght@400;500&family=Playfair+Display:ital,wght@0,700;1,700&display=swap">

  <!-- Styles -->
  <link rel="stylesheet" href="style.css">

  <!-- Structured Data -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "WebSite",
    "name": "焚而不燬",
    "alternateName": "Nec Tamen Consumebatur",
    "url": "https://nectamen.com",
    "description": "台灣民主化關鍵十年 1980–1989 互動式歷史紀錄"
  }
  </script>
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "ItemList",
    "name": "台灣民主化關鍵案件",
    "itemListElement": [
      {
        "@type": "ListItem",
        "position": 1,
        "name": "林宅血案",
        "url": "https://soanseng.github.io/the-lin/"
      },
      {
        "@type": "ListItem",
        "position": 2,
        "name": "陳文成事件",
        "url": "https://soanseng.github.io/Chen-Wen-chen/"
      },
      {
        "@type": "ListItem",
        "position": 3,
        "name": "江南案",
        "url": "https://soanseng.github.io/henry-liu-case/"
      },
      {
        "@type": "ListItem",
        "position": 4,
        "name": "鄭南榕事件",
        "url": "https://soanseng.github.io/nylon/"
      }
    ]
  }
  </script>
</head>
<body>

  <!-- Hero Section -->
  <header class="hero">
    <div class="hero__glow" aria-hidden="true"></div>
    <div class="hero__content">
      <h1 class="hero__title">焚而不燬</h1>
      <p class="hero__subtitle"><em>Nec Tamen Consumebatur</em></p>
      <p class="hero__tagline">台灣民主化關鍵十年 1980–1989</p>
    </div>
  </header>

  <!-- Introduction -->
  <section class="intro">
    <p>1980到1989，四條生命、四個案件，<br>燒出了台灣通往自由的路。</p>
  </section>

  <!-- Timeline -->
  <main class="timeline">

    <a href="https://soanseng.github.io/the-lin/" class="case" target="_blank" rel="noopener">
      <span class="case__year">1980</span>
      <div class="case__body">
        <h2 class="case__title">林宅血案</h2>
        <p class="case__name">林義雄</p>
        <p class="case__desc">二月二十八日，一個家庭的毀滅</p>
      </div>
      <span class="case__arrow" aria-hidden="true">&#8594;</span>
    </a>

    <a href="https://soanseng.github.io/Chen-Wen-chen/" class="case" target="_blank" rel="noopener">
      <span class="case__year">1981</span>
      <div class="case__body">
        <h2 class="case__title">陳文成事件</h2>
        <p class="case__name">陳文成</p>
        <p class="case__desc">一位學者的最後一夜</p>
      </div>
      <span class="case__arrow" aria-hidden="true">&#8594;</span>
    </a>

    <a href="https://soanseng.github.io/henry-liu-case/" class="case" target="_blank" rel="noopener">
      <span class="case__year">1984</span>
      <div class="case__body">
        <h2 class="case__title">江南案</h2>
        <p class="case__name">劉宜良</p>
        <p class="case__desc">從美國車庫到台灣解嚴</p>
      </div>
      <span class="case__arrow" aria-hidden="true">&#8594;</span>
    </a>

    <a href="https://soanseng.github.io/nylon/" class="case" target="_blank" rel="noopener">
      <span class="case__year">1989</span>
      <div class="case__body">
        <h2 class="case__title">鄭南榕事件</h2>
        <p class="case__name">鄭南榕</p>
        <p class="case__desc">用火焰守護言論自由</p>
      </div>
      <span class="case__arrow" aria-hidden="true">&#8594;</span>
    </a>

  </main>

  <!-- Footer -->
  <footer class="footer">
    <p class="footer__source">本系列以政府解密檔案為基礎，不做政治評論，只呈現歷史。</p>
    <p class="footer__meta">
      <a href="https://github.com/soanseng" target="_blank" rel="noopener">GitHub</a>
      <span aria-hidden="true">&middot;</span>
      MIT License
    </p>
  </footer>

</body>
</html>
```

**Step 2: Verify in browser**

Run: `python3 -m http.server 8000 -d /home/scipio/projects/nectamen` (or open index.html directly)
Expected: Unstyled but structurally complete page with all content visible and links working.

**Step 3: Commit**

```bash
git add index.html
git commit -m "feat: add HTML structure with SEO meta tags and structured data"
```

---

### Task 3: CSS — Core Layout & Typography

**Files:**
- Create: `style.css`

**Step 1: Write style.css with custom properties, reset, typography, and layout**

```css
/* ============================================
   焚而不燬 — nectamen.com
   Memorial Hall Landing Page
   ============================================ */

/* --- Custom Properties --- */
:root {
  --bg-dark: #1a1a1a;
  --bg-card: #2d2d2d;
  --text-primary: #e8e4df;
  --text-muted: #a09a92;
  --accent-amber: #c4721a;
  --accent-gold: #8b7355;
  --accent-glow: rgba(196, 114, 26, 0.15);
  --font-serif: 'Noto Serif TC', 'Georgia', serif;
  --font-sans: 'Noto Sans TC', 'Helvetica Neue', sans-serif;
  --font-latin: 'Playfair Display', 'Georgia', serif;
}

/* --- Reset --- */
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 16px;
  scroll-behavior: smooth;
}

body {
  font-family: var(--font-serif);
  background-color: var(--bg-dark);
  color: var(--text-primary);
  line-height: 1.8;
  min-height: 100vh;
  -webkit-font-smoothing: antialiased;
}

a {
  color: inherit;
  text-decoration: none;
}

/* --- Hero Section --- */
.hero {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 80vh;
  padding: 4rem 2rem;
  text-align: center;
  overflow: hidden;
}

.hero__glow {
  position: absolute;
  bottom: 10%;
  left: 50%;
  transform: translateX(-50%);
  width: 300px;
  height: 400px;
  background: radial-gradient(
    ellipse at center,
    rgba(196, 114, 26, 0.12) 0%,
    rgba(196, 114, 26, 0.05) 40%,
    transparent 70%
  );
  pointer-events: none;
}

.hero__content {
  position: relative;
  z-index: 1;
}

.hero__title {
  font-family: var(--font-serif);
  font-size: clamp(3rem, 8vw, 6rem);
  font-weight: 700;
  letter-spacing: 0.15em;
  margin-bottom: 1rem;
  color: var(--text-primary);
}

.hero__subtitle {
  font-family: var(--font-latin);
  font-size: clamp(1rem, 2.5vw, 1.5rem);
  font-weight: 700;
  color: var(--accent-gold);
  letter-spacing: 0.08em;
  margin-bottom: 1.5rem;
}

.hero__tagline {
  font-family: var(--font-sans);
  font-size: clamp(0.9rem, 2vw, 1.1rem);
  color: var(--text-muted);
  font-weight: 400;
}

/* --- Introduction --- */
.intro {
  max-width: 600px;
  margin: 0 auto;
  padding: 2rem 2rem 4rem;
  text-align: center;
  font-size: 1.1rem;
  color: var(--text-muted);
  line-height: 2;
}

/* --- Timeline --- */
.timeline {
  max-width: 720px;
  margin: 0 auto;
  padding: 0 2rem 4rem;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

/* --- Case Card --- */
.case {
  display: grid;
  grid-template-columns: 80px 1fr 40px;
  align-items: center;
  gap: 1.5rem;
  padding: 1.5rem 2rem;
  background: var(--bg-card);
  border: 1px solid rgba(139, 115, 85, 0.2);
  border-radius: 2px;
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
}

.case:hover,
.case:focus-visible {
  border-color: var(--accent-gold);
  box-shadow: 0 0 30px var(--accent-glow);
  outline: none;
}

.case__year {
  font-family: var(--font-latin);
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--accent-amber);
  text-align: center;
}

.case__body {
  min-width: 0;
}

.case__title {
  font-family: var(--font-serif);
  font-size: 1.3rem;
  font-weight: 700;
  margin-bottom: 0.15rem;
}

.case__name {
  font-family: var(--font-sans);
  font-size: 0.85rem;
  color: var(--accent-gold);
  margin-bottom: 0.3rem;
}

.case__desc {
  font-family: var(--font-sans);
  font-size: 0.9rem;
  color: var(--text-muted);
}

.case__arrow {
  font-size: 1.5rem;
  color: var(--accent-gold);
  opacity: 0.4;
  transition: opacity 0.3s ease, transform 0.3s ease;
  text-align: center;
}

.case:hover .case__arrow {
  opacity: 1;
  transform: translateX(4px);
}

/* --- Footer --- */
.footer {
  max-width: 720px;
  margin: 0 auto;
  padding: 3rem 2rem;
  text-align: center;
  border-top: 1px solid rgba(139, 115, 85, 0.15);
}

.footer__source {
  font-size: 0.85rem;
  color: var(--text-muted);
  margin-bottom: 1rem;
  line-height: 1.8;
}

.footer__meta {
  font-family: var(--font-sans);
  font-size: 0.8rem;
  color: var(--accent-gold);
}

.footer__meta a {
  text-decoration: underline;
  text-underline-offset: 2px;
}

.footer__meta a:hover {
  color: var(--text-primary);
}

/* --- Responsive --- */
@media (max-width: 480px) {
  .case {
    grid-template-columns: 60px 1fr 30px;
    padding: 1.2rem 1rem;
    gap: 1rem;
  }

  .case__year {
    font-size: 1.2rem;
  }

  .case__title {
    font-size: 1.1rem;
  }
}

/* --- Accessibility --- */
@media (prefers-reduced-motion: reduce) {
  * {
    transition: none !important;
  }
}

:focus-visible {
  outline: 2px solid var(--accent-amber);
  outline-offset: 2px;
}
```

**Step 2: Verify in browser**

Open index.html in browser.
Expected: Dark memorial hall aesthetic, readable typography, cards with hover glow effect, responsive on mobile.

**Step 3: Commit**

```bash
git add style.css
git commit -m "feat: add memorial hall CSS with dark theme, timeline cards, responsive layout"
```

---

### Task 4: Favicon SVG

**Files:**
- Create: `favicon.svg`

**Step 1: Create burning bush SVG favicon**

A minimalist burning bush silhouette — bare branches with a warm glow. Keep it simple so it reads at 32x32.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32">
  <!-- Glow -->
  <circle cx="16" cy="14" r="10" fill="#c4721a" opacity="0.2"/>
  <!-- Bush/branches -->
  <g fill="none" stroke="#c4721a" stroke-width="1.5" stroke-linecap="round">
    <!-- Trunk -->
    <line x1="16" y1="28" x2="16" y2="18"/>
    <!-- Main branches -->
    <line x1="16" y1="18" x2="10" y2="10"/>
    <line x1="16" y1="18" x2="22" y2="10"/>
    <line x1="16" y1="16" x2="12" y2="8"/>
    <line x1="16" y1="16" x2="20" y2="8"/>
    <!-- Small branches -->
    <line x1="13" y1="12" x2="9" y2="6"/>
    <line x1="19" y1="12" x2="23" y2="6"/>
    <line x1="16" y1="14" x2="16" y2="6"/>
  </g>
</svg>
```

**Step 2: Verify**

Open favicon.svg in browser — should show a simple amber-colored branching tree shape.

**Step 3: Commit**

```bash
git add favicon.svg
git commit -m "feat: add burning bush favicon SVG"
```

---

### Task 5: SEO Files (sitemap, robots)

**Files:**
- Create: `sitemap.xml`
- Create: `robots.txt`

**Step 1: Create sitemap.xml**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://nectamen.com/</loc>
    <lastmod>2026-02-20</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://soanseng.github.io/the-lin/</loc>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://soanseng.github.io/Chen-Wen-chen/</loc>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://soanseng.github.io/henry-liu-case/</loc>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://soanseng.github.io/nylon/</loc>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
</urlset>
```

**Step 2: Create robots.txt**

```
User-agent: *
Allow: /

Sitemap: https://nectamen.com/sitemap.xml
```

**Step 3: Commit**

```bash
git add sitemap.xml robots.txt
git commit -m "feat: add sitemap.xml and robots.txt for SEO"
```

---

### Task 6: GitHub Actions Deploy

**Files:**
- Create: `.github/workflows/deploy.yml`

**Step 1: Create deploy workflow**

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [main]

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: pages
  cancel-in-progress: true

jobs:
  deploy:
    runs-on: ubuntu-latest
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    steps:
      - uses: actions/checkout@v4

      - name: Setup Pages
        uses: actions/configure-pages@v5

      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: '.'

      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

**Step 2: Commit**

```bash
git add .github/workflows/deploy.yml
git commit -m "ci: add GitHub Pages deployment workflow"
```

---

### Task 7: Create GitHub Repo & Push

**Step 1: Create remote repo**

```bash
gh repo create nectamen --public --description "焚而不燬 — 台灣民主化關鍵十年 1980–1989" --source /home/scipio/projects/nectamen --push
```

**Step 2: Enable GitHub Pages**

Go to repo Settings > Pages > Source: GitHub Actions.
Or via CLI if available.

**Step 3: Verify deployment**

Wait for GitHub Actions to complete, then verify `https://soanseng.github.io/nectamen/` loads correctly.
(Custom domain `nectamen.com` will work after DNS is configured.)

---

### Task 8: Open Graph Image (Placeholder)

**Files:**
- Create: `og-image.png` (1200x630)

**Step 1: Generate a simple OG image**

Use the @frontend-design skill to create a 1200x630 PNG with:
- Dark background (#1a1a1a)
- 「焚而不燬」in large serif text, centered
- "Nec Tamen Consumebatur" below in gold
- "台灣民主化關鍵十年 1980–1989" at bottom
- Subtle amber glow behind text

Alternatively: Create a simple HTML-to-image version, or use a placeholder and iterate later.

**Step 2: Commit**

```bash
git add og-image.png
git commit -m "feat: add Open Graph sharing image"
```

---

## Summary of Commits

1. `chore: project scaffolding` — CNAME, .gitignore, LICENSE, README, CLAUDE.md
2. `feat: add HTML structure with SEO meta tags and structured data` — index.html
3. `feat: add memorial hall CSS with dark theme, timeline cards, responsive layout` — style.css
4. `feat: add burning bush favicon SVG` — favicon.svg
5. `feat: add sitemap.xml and robots.txt for SEO` — SEO files
6. `ci: add GitHub Pages deployment workflow` — .github/workflows/deploy.yml
7. `chore: create repo and push` — remote setup
8. `feat: add Open Graph sharing image` — og-image.png

## DNS Configuration (Manual, Post-Deploy)

After buying `nectamen.com`:

1. Add DNS records:
   - `A` record → `185.199.108.153` (GitHub Pages)
   - `A` record → `185.199.109.153`
   - `A` record → `185.199.110.153`
   - `A` record → `185.199.111.153`
   - `CNAME` `www` → `soanseng.github.io`

2. In GitHub repo Settings > Pages > Custom domain: enter `nectamen.com`

3. Enable "Enforce HTTPS"
