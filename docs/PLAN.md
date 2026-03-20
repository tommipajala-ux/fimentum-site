# Fimentum Site Implementation Plan

## Overview

Modern single-page landing site for Fimentum Oy - funding advisory for Finnish startups and growth companies.

**Tech Stack:** Astro 5 + Tailwind CSS v4 + TypeScript (strict)
**Deployment:** AWS Amplify
**Language:** English primary

---

## Current Status

### Completed
- [x] Astro + Tailwind v4 boilerplate setup
- [x] All section components built (Hero, Services, Stats, About, Process, Contact)
- [x] Header with sticky nav and mobile menu
- [x] Footer with social links and company info
- [x] Logo integration (dark + white versions)
- [x] Partner logos (Business Finland, EU, Finnvera, Elinvoimakeskus)
- [x] Partnerships section (Kasvu Open, Business Tampere)
- [x] Design system utilities in CSS
- [x] Tommi photo integration (LinkedIn)

### Pending
- [ ] Calendly integration (booking link)
- [ ] Contact form backend (Formspree/Netlify Forms)
- [ ] Google Analytics 4 setup (env var ready)
- [ ] AWS Amplify deployment
- [ ] Final copy review/polish

---

## Site Architecture

### Single-Page Sections

| Section | Component | Background | Status |
|---------|-----------|------------|--------|
| Hero | `Hero.astro` | Dark gradient | Done |
| Services | `Services.astro` | White | Done |
| Track Record | `Stats.astro` | Dark gradient | Done |
| Partnerships | (in Stats.astro) | White | Done |
| About | `About.astro` | Dark gradient | Done |
| Process | `Process.astro` | White | Done |
| Contact | `Contact.astro` | Dark gradient | Done |
| Footer | `Footer.astro` | Slate-900 | Done |

---

## Components

| Component | File | Description |
|-----------|------|-------------|
| Header | `src/components/Header.astro` | Sticky nav, scroll-aware, mobile menu |
| Hero | `src/components/Hero.astro` | Gradient bg, headline, stats bar, dual CTAs |
| Services | `src/components/Services.astro` | 4 service cards in responsive grid |
| Stats | `src/components/Stats.astro` | Partner logos + Kasvu Open/Business Tampere |
| About | `src/components/About.astro` | Tommi photo + bio + credentials |
| Process | `src/components/Process.astro` | 4-step visualization with CTA |
| Contact | `src/components/Contact.astro` | Contact form + details |
| Footer | `src/components/Footer.astro` | 4-column, social links, company info |

---

## Assets

### Logos (in `public/`)
- `logo.webp` - Original dark logo (for light backgrounds)
- `logo-white.webp` - White logo (for dark backgrounds)

### Partner Logos (in `public/logos/`)
- `business-finland.svg` - White version
- `eu.svg` - EU flag
- `finnvera.svg` - White version
- `ely.svg` - White version (converted from EPS)
- `kasvu-open.jpg` - Color logo
- `business-tampere.jpg` - Color logo

---

## Design System

See `/docs/DESIGN.md` for full specifications.

Key CSS utilities defined in `src/styles/global.css`:
- `.btn-primary` / `.btn-secondary` - Buttons
- `.card-service` - Service cards
- `.section-dark` / `.section-light` - Section backgrounds
- `.section-container` - Max-width wrapper
- `.form-input` / `.form-label` - Form elements
- `.gradient-badge` - Icon backgrounds
- `.blur-orb-indigo` / `.blur-orb-cyan` - Decorative elements

---

## Environment Variables

| Variable | Purpose | Required |
|----------|---------|----------|
| `PUBLIC_GA_ID` | Google Analytics 4 measurement ID | Production only |

---

## Future Expansion

- Finnish language version
- Blog/resources section
- Case studies page
- Funding calculator tool
