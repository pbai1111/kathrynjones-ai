# KathrynJones.AI — Workflow

## Site Map

| Page | File | Category | Status |
|------|------|----------|--------|
| Landing | `index.html` | — | Content complete, timeline + skills live |
| Experiential & Interactive Media | `theater.html` | Leading Cross-Functional Teams... | Content complete, videos embedded, Featured In added |
| Full-Service Agency Leadership | `agency.html` | Leading Cross-Functional Teams... | Content complete, client logos live |
| Live Production & Audience Engagement | `interactive.html` | Leading Cross-Functional Teams... | Content complete, video embedded |
| AI Workflow Systems & Creative Operations | `ai-systems.html` | Applied AI. Operationalized. | Content complete, flip cards live |
| Experiential Knowledge Design | `experiential-knowledge.html` | — | Separate design system (InsatiableMind) — do not touch styling |

---

## Content Positioning

This is the **corporate version** of the site, repositioned from projectbased.ai (arts/culture audience) to kathrynjones.ai (C-suite/enterprise audience).

### Key Framing Shifts
- "Technology and creativity" → "Technology, media, and enterprise operations"
- "Bootstrapped" narrative → "Built from the ground up" with direct leadership framing
- "Arts & culture" emphasis → "Fortune 500, nonprofit, and brand" emphasis
- Hero tagline: "Technology and creativity, engineered into experiences that resonate."
- "Applied AI. Early and all-in." → "Applied AI. Operationalized."
- Poetic/editorial tone → Confident, direct, executive tone
- "Seeing around corners" → "Identifying what's next and operationalizing it"
- Skills reordered: AI and strategy capabilities lead; creative execution follows
- Every page leads with business outcomes, operational scale, or measurable results

### Content Reference
- `corporate-site-text.md` — Full approved copy for all pages
- `site-copy.md` — Legacy text from the arts/culture version (for reference only)

---

## Architecture

### Shared Styles
- **`styles.css`** — Single shared stylesheet containing CSS variables, reset, nav, layout, typography, impact sections, throughline, video/work items, contact bar, responsive breakpoints
- Each page links `styles.css` and uses a small inline `<style>` block for page-specific overrides only
- **Exception:** `experiential-knowledge.html` has its own complete dark-theme `<style>` block (different fonts, colors, variables) that overrides `styles.css`

### Navigation
- **Index page:** Static chapter list in hero right column; hamburger nav slides in on scroll past hero
- **Inner pages (theater, agency, interactive, ai-systems):** Hamburger menu (☰) with semi-transparent plum overlay, current page highlighted
- **experiential-knowledge.html:** Has its own dark-theme nav — do not modify
- **Chapter names across all navs:**
  - 15+ years leading cross-functional teams through media, technology, and organizational change
    - Experiential & Interactive Media → `theater.html`
    - Full-Service Agency Leadership → `agency.html`
    - Live Production & Audience Engagement → `interactive.html`
  - Applied AI. Operationalized.
    - AI Workflow Systems & Creative Operations → `ai-systems.html`
    - AI-Powered Knowledge Systems → `experiential-knowledge.html` (Current Focus)

### Page Layout Pattern (inner pages)
- Page header with category label, title (left), and tagline (right) in a 2-column grid
- Two-column content area (sticky left, scrollable right)
- Impact/stats section with optional "Featured In" press row
- Throughline + "Next" link

### Index Page Layout
- Hero: name + gradient differentiator (left), chapter navigation (right), bouncing chevron scroll hint
- Timeline: alternating left/right entries (2007–2026) with milestone markers, staggered fade-in animations
- Skills block: hover-to-plum skill tags (AI & strategy skills lead)
- Contact bar

### Fonts
- **Light theme (all pages except experiential-knowledge):** Plus Jakarta Sans (200–800)
- **Dark theme (experiential-knowledge only):** Cormorant Garamond (serif) + DM Sans (sans)

### Color System
- **Light theme:** Background `#FAFAF8`, text `#1a1a1a`, accent plum `#5A2650`
- **Dark theme (experiential-knowledge):** Background `#070707`, text `#e8e4df`, accents gold `#c9a96e` + blue `#7a9bb5`
- **Key styling patterns:** Client names in plum, section headers bold plum

---

## What's Done

- [x] Shared `styles.css` extracted from inline styles
- [x] Hamburger nav with plum overlay on all inner pages
- [x] Scroll-triggered hamburger nav on index page
- [x] Client logos on agency page (16 logos in `assets/CA Client logos/`)
- [x] Client names filled in on theater, interactive pages
- [x] Video embeds updated to new Vimeo account (theater page — 3 videos)
- [x] Video embed on interactive page (Vimeo)
- [x] AI systems page redesigned — full-width flip cards, plum front/light back
- [x] Page taglines added to theater, agency, interactive, ai-systems headers
- [x] Chapter numbers removed across all pages and menus
- [x] Front page: gray-to-plum gradient on differentiator, timeline (2007–2026), skills block
- [x] Section headers restyled (plum, bold, optically balanced)
- [x] "Featured In" press rows on theater (ABC, CNN, Streaming Media, The Verge, New York Times, Wall Street Journal) and agency (Fast Company, AdWeek, LA Times, Boston Globe)
- [x] Client names and capabilities styled in plum for quick scanning
- [x] Scroll hint: bouncing chevron, hero at 88vh for timeline peek
- [x] `corporate-site-text.md` — all approved corporate copy documented
- [x] Git repo on GitHub, pushed to main
- [x] Full copy repositioning from arts/culture to corporate audience
- [x] All nav overlays updated with corporate chapter names across every page
- [x] Timeline entries rewritten with operational/enterprise framing
- [x] Skills list reordered — AI & strategy capabilities lead
- [x] Theater page reframed as "Experiential & Interactive Media" with enterprise clients elevated
- [x] Agency page reframed as "Full-Service Agency Leadership" with P&L and scale emphasis
- [x] Interactive page reframed as "Live Production & Audience Engagement" with operational design framing
- [x] AI systems page reframed as "AI Workflow Systems & Creative Operations"

---

## Development Checklist

### Still To Do
- [ ] Add `<meta name="description">` tags to each page for SEO
- [ ] Add Open Graph / social meta tags
- [ ] Add favicon
- [ ] Audit accessibility (alt text on logos, ARIA labels, semantic HTML)
- [ ] Test all inter-page navigation links
- [ ] Test responsive layouts on mobile / tablet breakpoints
- [ ] Verify contact email link on index.html works
- [ ] Add responsive handling for page-header tagline grids (mobile stacking)
- [ ] Add responsive handling for timeline on mobile

### Performance
- [ ] Optimize Google Fonts loading (preconnect, font-display)
- [ ] Consider self-hosting Plus Jakarta Sans
- [ ] Optimize logo image sizes (some are large originals)

---

## Deployment

### Current Setup
- Git repo: kathrynjones-ai
- Branch: `main`
- Static HTML — no build step, no framework

### Vercel Deployment
- Go to [vercel.com](https://vercel.com) → New Project → Import Git Repository
- Select the repo
- Framework preset: **Other** (static HTML, no build step)
- Output directory: `.` (root)
- Deploy

### Custom Domain
- Add `kathrynjones.ai` in Vercel project settings → Domains
- Update DNS records as Vercel instructs

---

## Notes

- **experiential-knowledge.html** has its own design system — dark theme, different fonts, different color palette. Never modify its styling from shared CSS work.
- Page 5 has scroll-triggered reveal animations (JavaScript at bottom of file).
- Index page has scroll-triggered nav (JavaScript at bottom of file).
- Site is fully static — no server, no framework, no dependencies beyond Google Fonts.
- `corporate-site-text.md` contains all approved corporate copy for all pages.
- `site-copy.md` contains legacy arts/culture copy for reference only.
- **Essence Festival entries** credit Wide Angle Productions — Kathryn facilitated, not led, these productions.
