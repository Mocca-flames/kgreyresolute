# PLAN.md — K Grey Resolute Website

## Project Overview
**Client:** K Grey Resolute Security  
**Goal:** Build a professional, conversion-focused multi-page website for a new South African security company.  
**Stack:** React (single-file JSX per page) or HTML/CSS/JS — self-contained files, no backend required.  
**Status:** Planning phase

---

## Chosen Pages (Essential Only)

> Reasoning: New company with limited content. Focus on trust-building, lead generation, and service clarity. No gallery or portfolio until real assets are available.

| # | Page | Priority | Purpose |
|---|------|----------|---------|
| 1 | **Home** | Critical | First impression, overview, credibility, CTA |
| 2 | **Services** | Critical | Full list of offerings with descriptions |
| 3 | **About** | High | Company story, values, compliance badges |
| 4 | **Contact / Quote** | Critical | Lead capture — primary conversion goal |
| 5 | **Careers** | Medium | Recruitment — they have 20+ open positions |

**Excluded for now:**
- ~~Gallery~~ — No real photos yet; placeholder images look unprofessional
- ~~Portfolio/Case Studies~~ — New company, no track record to show
- ~~Fleet~~ — Can be merged into the About or Services page as a section

---

## Page-by-Page Content Plan

### Page 1: Home (`index`)
**Goal:** Hook the visitor in 3 seconds and funnel them to a quote.

| Section | Content Source | Notes |
|---------|---------------|-------|
| Hero | Headline + subheadline + CTA buttons | "K Grey Resolute — Security You Can Trust" |
| Stats Bar | 4 quick numbers | 24/7 Ops, 12-min response, 10 services, PSIRA certified |
| Services Overview | 6 top services (icons + 1-line desc) | Link to full Services page |
| Why Choose Us | 6 key differentiators (from content) | Checkmark list style |
| Testimonials | 3 of 5 quotes from CONTENT.md | Carousel or cards |
| Call to Action | "Get a Free Quote" banner | Links to Contact page |
| Footer | Full footer with all contact info | As per CONTENT.md |

---

### Page 2: Services (`services`)
**Goal:** Make every service clear, credible, and findable.

| Section | Content Source | Notes |
|---------|---------------|-------|
| Hero Banner | Services headline | "Comprehensive Protection for Every Situation" |
| Service Cards (10) | All 10 from CONTENT.md | Icon + name + description + CTA per card |
| Service Areas | Coverage map/list | Primary 5 areas + extended 4 |
| CTA Strip | Quote prompt | "Not sure what you need? Request a free consultation" |

---

### Page 3: About (`about`)
**Goal:** Build trust for a new company with no track record.

| Section | Content Source | Notes |
|---------|---------------|-------|
| Company Intro | Overview + founding story | Focus on experience of founders |
| Mission & Vision | From CONTENT.md | Two-column layout |
| Core Values | 5 values from CONTENT.md | Icon cards |
| Compliance Badges | PSIRA, BBBEE, COIDA, SASETA | Critical for B2B trust |
| Fleet Overview | Vehicle table from CONTENT.md | Shows operational capability |
| Technology Stack | 5 items from CONTENT.md | Drone, ANPR, body cams, etc. |

---

### Page 4: Contact / Quote (`contact`)
**Goal:** Capture leads. This is the most important conversion page.

| Section | Content Source | Notes |
|---------|---------------|-------|
| Contact Details | All phones + emails | Prominent display |
| Quote Request Form | Full form fields from CONTENT.md | Primary focus |
| Map / Address | Brand Road, Midrand | Embedded Google Map |
| Emergency CTA | Panic line copy | Red/urgent styling |
| Business Hours | From CONTENT.md | Office vs 24/7 control room |

---

### Page 5: Careers (`careers`)
**Goal:** Attract qualified PSIRA-registered security professionals.

| Section | Content Source | Notes |
|---------|---------------|-------|
| Intro | Why work here | Culture + professionalism |
| Open Positions | 5 role categories (20+ positions) | Job cards with requirements |
| Requirements | From CONTENT.md | PSIRA, firearm comp, driver's license, etc. |
| Benefits | 6 benefits from CONTENT.md | Icon list |
| Apply CTA | careers@kgreyresolute.co.za | Simple mailto link |

---

## Shared Components (Used Across All Pages)

| Component | Notes |
|-----------|-------|
| **Navbar** | Logo + 5 nav links + "Get Quote" button (sticky) |
| **Footer** | Full footer with nav, contact, legal, social media |
| **WhatsApp Float Button** | Bottom-right, links to +27 61 582 6087 |
| **Emergency Banner** | Optional: thin red bar at very top for panic line |

---

## File Structure

```
/
├── index.html          ← Home
├── services.html       ← Services
├── about.html          ← About
├── contact.html        ← Contact + Quote
├── careers.html        ← Careers
├── css/
│   ├── variables.css   ← CSS custom properties (from DESIGN.md)
│   ├── reset.css       ← Normalize/reset
│   ├── layout.css      ← Grid, container, spacing utilities
│   ├── components.css  ← Buttons, cards, forms, navbar, footer
│   ├── animations.css  ← Keyframes, transitions, IntersectionObserver styles
│   └── utilities.css   ← Helper classes (text, borders, shadows)
└── assets/
    ├── logo.svg
    └── images/         ← Placeholder images only until real photos
```

> **Styling Rule:** All CSS must reside in external `.css` files within the `/css` directory. No inline styles or `<style>` blocks in HTML. Use class-based styling exclusively.

---

## Content Gaps (Things to Collect)

- [ ] Real photography (guards, vehicles, control room)
- [ ] Company logo (final vector file)
- [ ] Real registration document scans (for compliance downloads)
- [ ] Google Maps embed API key or iframe link
- [ ] WhatsApp Business verification
- [ ] Actual founding team photos and bios (optional but builds trust)