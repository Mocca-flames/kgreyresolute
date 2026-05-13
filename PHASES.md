# PHASES.md — K Grey Resolute Website Build Phases

## How to Use This Document
Work through each phase in order. Each phase has a clear goal, a checklist, and a "done when" condition. Do not move to the next phase until the current one is complete. Mark items with ✅ as you finish them.

---

## Phase 0 — Foundation Setup
**Goal:** Get shared components and design system ready before building any page.  
**Time estimate:** 1–2 sessions

### Checklist
- [ ] Finalize color palette (from DESIGN.md) as CSS variables in `style.css`
- [ ] Import Google Fonts: Oswald, DM Sans, JetBrains Mono
- [ ] Build the **Navbar** component (logo + nav links + "Get Quote" CTA + mobile hamburger)
- [ ] Build the **Footer** component (all 4 columns + legal strip)
- [ ] Add **WhatsApp floating button** (bottom-right, all pages)
- [ ] Define button styles: `.btn-primary`, `.btn-ghost`, `.btn-danger`
- [ ] Define shared input/form styles
- [ ] Set up the `assets/` folder structure

### Done When
Navbar and Footer render correctly on desktop and mobile. CSS variables are all defined. You can copy-paste the navbar/footer into any new page and it works instantly.

---

## Phase 1 — Home Page
**Goal:** Build the most impactful page first. This is the face of the company.  
**File:** `index.html`  
**Time estimate:** 2–3 sessions

### Sections (in order)
- [ ] **Hero** — Full-screen, dark background image, headline, sub-headline, 2 CTA buttons
- [ ] **Stats Bar** — 4 numbers: 24/7 Ops | 12–15 min Response | 10 Services | PSIRA Certified
- [ ] **Services Overview** — 6 service cards (icons, titles, 1-line description) + "View All Services" link
- [ ] **Why Choose Us** — 6 differentiators with check icons (from CONTENT.md)
- [ ] **Testimonials** — 3 quotes in cards (carousel optional, static grid is fine)
- [ ] **Quote CTA Banner** — Full-width gold/dark section: "Ready to secure your business?" + button
- [ ] **Navbar + Footer** from Phase 0

### Done When
Home page is complete, responsive on mobile/tablet/desktop, all links point to correct pages (even if those pages don't exist yet — just use the correct `href`).

---

## Notes Before Phase 2

**Completed Phase 0 & 1:**
- CSS architecture established in `/css/` (7 modular files, no inline styles)
- Navbar, Footer, WhatsApp float button are reusable components already in `index.html`
- Design tokens mapped from DESIGN.md (colors, fonts, spacing)
- Home page live with all Phase 1 sections

**Phase 2–5 Pattern:**
- Each page begins with the same `<link>` tags for external CSS files
- Copy-paste the Navbar and Footer HTML from `index.html`
- Include the WhatsApp floating button anchor
- Keep all styles in external CSS; no `<style>` blocks allowed
- Mobile hamburger menu script is already in `index.html` — reuse verbatim
- All services link to IDs on `services.html` (e.g., `href="services.html#armed-guarding"`)

**Content Reference:**
- Service descriptions, compliance details, careers listings: pull from `CONTENT.md`
- Phone: +27 61 582 6087 (use `tel:` and `wa.me` links)
- PSIRA: 2998765
- Address: Brand Road, Swart Dr, Midrand, 1685
- Emails: info@, sales@, ops@, accounts@, careers@

---

## Phase 2 — Services Page
**Goal:** Give every visitor a clear picture of what K Grey Resolute offers.  
**File:** `services.html`  
**Time estimate:** 1–2 sessions

### Sections (in order)
- [x] **Page Hero Banner** — "Our Services" headline, short intro paragraph
- [x] **Services Grid** — All 10 service cards with full descriptions (3-column desktop, 1-column mobile)
  - Armed & Unarmed Guarding
  - VIP Protection
  - Tactical Response
  - CCTV Monitoring
  - Event Security
  - Access Control
  - Patrol Services
  - Escort Services
  - Control Room Monitoring
  - Risk Assessments
- [x] **Service Areas** — Two-column list: Primary 5 areas | Extended 4 areas
- [x] **Bottom CTA** — "Not sure what you need? Get a free consultation" → Contact link

### Done When
All 10 services are displayed with correct content. Page is responsive. Service area section is clear.

---

## Phase 3 — About Page
**Goal:** Build credibility for a brand-new company.  
**File:** `about.html`  
**Time estimate:** 1–2 sessions

### Sections (in order)
- [x] **Page Hero Banner** — "About K Grey Resolute" + company tagline
- [x] **Company Overview** — 2 paragraphs: who we are + founding story
- [x] **Mission & Vision** — Two-column layout, each with icon + title + paragraph
- [x] **Core Values** — 5 value cards with icons (Protection, Integrity, Excellence, Reliability, Innovation)
- [x] **Compliance Badges** — PSIRA | BBBEE Level 4 | COIDA | SASETA | Insured — displayed as a badge row with registration numbers in mono font
- [x] **Fleet Overview** — Table or card grid from CONTENT.md fleet section
- [x] **Technology Stack** — 5 items (cloud reporting, GPS tracking, ANPR, body cams, drone) with icons
- [x] **Bottom CTA** — Link to Contact / Quote page

### Done When
Compliance section is prominent and scannable. New visitor can verify legitimacy within 10 seconds of seeing the page.

---

## Phase 4 — Contact & Quote Page
**Goal:** Maximum conversion. Make it easy to get in touch or request a quote.  
**File:** `contact.html`  
**Time estimate:** 1–2 sessions

### Sections (in order)
- [x] **Page Hero Banner** — "Get in Touch / Request a Quote"
- [x] **Emergency Strip** — Red highlighted box: "24/7 Emergency Line: +27 61 582 6087" (press 1)
- [x] **Two-Column Layout:**
  - **Left:** Contact details (main number, WhatsApp, all email addresses, physical address, business hours)
  - **Right:** Full quote request form
- [x] **Quote Form Fields** (from CONTENT.md):
  - Full Name, Company Name, Email, Phone
  - Service dropdown (all 10 services)
  - Start date, Duration, Site address
  - No. of guards, Armed/Unarmed, Coverage hours
  - Special requirements (textarea)
  - Preferred contact method
  - Submit button
- [x] **Google Map Embed** — Brand Road, Swart Dr, Midrand (or static map image if no API key)
- [x] **Social Media Links** — LinkedIn, Facebook, Instagram

### Done When
Form is fully functional (can submit via `mailto:` or `formspree.io` as a no-backend option). All contact details are correct and clickable (tel:, mailto:, wa.me links). Map displays correctly.

> **No-Backend Form Option:** Use `action="https://formspree.io/f/YOUR_ID"` on the form for free email delivery without a server.

---

## Phase 5 — Careers Page
**Goal:** Attract quality security professionals to apply.  
**File:** `careers.html`  
**Time estimate:** 1 session

### Sections (in order)
- [x] **Page Hero Banner** — "Join the K Grey Resolute Team"
- [x] **Intro Paragraph** — Why work here, company culture
- [x] **Open Positions** — 5 role cards:
  - Armed Response Officers (×5, Midrand/JHB)
  - Control Room Operators (×3, Midrand)
  - CCTV Monitoring Specialists (×2)
  - Security Guards — Various Grades (×10+)
  - Tactical Team Members (×4)
- [x] **Requirements List** — PSIRA, firearm comp, driver's license, Grade 12, First Aid, fitness
- [x] **Benefits** — 6 benefit items with icons
- [x] **Apply CTA** — "Send your CV to careers@kgreyresolute.co.za" + mailto button

### Done When
All open positions are listed with requirements. Apply button opens email client. Page is mobile-friendly (many applicants will be on phones).

---

## Phase 6 — Polish & Cross-Page QA
**Goal:** Make everything feel cohesive and professional before launch.  
**Time estimate:** 1 session

### Checklist

**Visual Consistency**
- [ ] All pages use the same navbar, footer, and font imports
- [ ] Section spacing is consistent across all pages
- [ ] Gold accent used consistently — not over-used
- [ ] All headings use Oswald, all body text uses DM Sans

**Links & Navigation**
- [ ] All nav links work on every page
- [ ] "Get Quote" CTA always links to `contact.html`
- [ ] WhatsApp button on every page links to `wa.me/27615826087`
- [ ] Phone numbers are `tel:` links (clickable on mobile)
- [ ] Email addresses are `mailto:` links

**Responsive Check**
- [ ] Test at 375px (iPhone SE)
- [ ] Test at 768px (iPad)
- [ ] Test at 1280px (desktop)
- [ ] Hamburger menu works correctly

**Content Accuracy**
- [ ] All phone numbers correct: +27 61 582 6087
- [ ] PSIRA number correct: 2998765
- [ ] All email addresses correct (info@, sales@, ops@, accounts@, careers@)
- [ ] Physical address correct: Brand Road, Swart Dr, Midrand, 1685
- [ ] Copyright year: 2025

**Performance**
- [ ] Images have `loading="lazy"` attribute
- [ ] Fonts loaded with `display=swap`
- [ ] No broken image links

---

## Phase 7 — Launch Prep
**Goal:** Everything needed to go live.

### Checklist
- [ ] Add real photography when available (replace placeholder images)
- [ ] Set up domain: `www.kgreyresolute.co.za`
- [ ] Configure hosting (recommended: Netlify, Vercel, or shared hosting via cPanel)
- [ ] Add Google Analytics or similar tracking
- [ ] Submit sitemap to Google Search Console
- [ ] Set up WhatsApp Business account for the number
- [ ] Set up Formspree (or backend) for quote form emails
- [ ] Test contact form — confirm emails arrive at `sales@kgreyresolute.co.za`
- [ ] Test on real mobile devices
- [ ] Add SSL certificate (HTTPS) — free via Let's Encrypt / Netlify

---

## Future Phases (Post-Launch)

| Phase | Feature | When to Add |
|-------|---------|-------------|
| 8 | Real photo gallery | Once actual job photos exist |
| 9 | Blog / News section | After 3–6 months operation |
| 10 | Client portal login | When operational systems are in place |
| 11 | Live chat integration | When team can manage it |
| 12 | Online quote calculator | When pricing is standardized |

---

## Build Order Summary

```
Phase 0 → Shared Components (Navbar, Footer, CSS)
Phase 1 → Home Page          ← Most important, do first
Phase 2 → Services Page
Phase 3 → About Page
Phase 4 → Contact & Quote    ← Second most important
Phase 5 → Careers Page
Phase 6 → QA & Polish
Phase 7 → Launch
```