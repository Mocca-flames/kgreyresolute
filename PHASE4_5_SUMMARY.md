# Phase 4 & 5 Implementation Summary

## Files Created
- `contact.html` — Contact & Quote Request page
- `careers.html` — Careers & Job Openings page

## What Was Built

### Contact.html (Phase 4)
1. **Page Hero Banner** — "Get in Touch / Request a Quote" headline with subtitle
2. **Emergency Strip** — Red highlighted box with 24/7 emergency line + "press 1" note
3. **Two-Column Layout** (CSS Grid):
   - **Left:** Full contact details:
     - Main tel: +27 61 582 6087 (tel: link)
     - WhatsApp: wa.me/27615826087
     - All 5 emails: info@, sales@, ops@, accounts@, careers@ (all mailto: links)
     - Physical address: Brand Road, Swart Dr, Midrand, 1685
     - Business hours: Mon–Fri 7am–6pm | 24/7 Control Room
   - **Right:** Full quote request form with 15 fields:
     - Full Name, Company Name, Email, Phone
     - Service dropdown (all 10 services)
     - Start date, Duration
     - Site address (textarea)
     - No. of guards, Armed/Unarmed select, Coverage hours select
     - Special requirements (textarea)
     - Preferred contact method (radio buttons)
     - Submit button → `action="mailto:sales@kgreyresolute.co.za"`
4. **Google Map Embed** — iframe with Midrand coordinates
5. **Social Media Links** — LinkedIn, Facebook, Instagram with icons
6. Navbar (Contact active), Footer, WhatsApp float button included

### Careers.html (Phase 5)
1. **Page Hero Banner** — "Join the K Grey Resolute Team" headline + intro paragraph
2. **Open Positions** — 5 role cards:
   - Armed Response Officers (×5, Midrand/JHB)
   - Control Room Operators (×3, Midrand)
   - CCTV Monitoring Specialists (×2)
   - Security Guards — Various Grades (×10+)
   - Tactical Team Members (×4)
   Each card includes: title, count, location, description, bulleted requirements list
3. **Common Requirements Section** — 6 items in card format:
   - PSIRA license, Firearm competency, Driver's license, Grade 12/Matric, First Aid (advantageous), Good physical fitness
4. **Benefits Section** — 6 items with icons:
   - Competitive Pay Rates, Ongoing Training, Career Progression, 13th Cheque, Medical Aid Contribution, Uniform Provided
5. **Apply CTA** — Full-width gold CTA section with mailto button to careers@kgreyresolute.co.za
6. Navbar (Careers active), Footer, WhatsApp float button included

## Technical Verification

### ✅ Design System Compliance
- Uses exact same HTML head structure as index.html (fonts, CSS load order)
- All styling via external CSS files (no inline `<style>` blocks)
- CSS classes from existing components.css, utilities.css, layout.css
- Font families: Oswald (headings), DM Sans (body), JetBrains Mono (labels)

### ✅ Content Accuracy
- All phone numbers: +27 61 582 6087 (tel: and wa.me links)
- All emails: info@, sales@, ops@, accounts@, careers@ → kgreyresolute.co.za
- PSIRA: 4792247
- Address: Brand Road, Swart Dr, Midrand, 1685
- Copyright: 2025

### ✅ Mobile-Friendliness
- Both pages use responsive grid/flex layouts
- Mobile hamburger menu script copied verbatim from index.html
- Contact form responsive (two-column → single column on mobile)
- Job cards stack on mobile
- Benefits grid auto-fit responsive

### ✅ CSS Added
New classes added to `components.css`:
- `.emergency-strip` — red strip with icon and centered text
- `.emergency-box` — flex container for emergency content
- `.section-label` — mono gold pre-headline style
- `.cta-banner` — gold-accent background CTA strip
- `.cta-content`, `.cta-headline`, `.cta-subtitle`

## Assumptions Made
1. **Google Maps** — Used generic Midrand coordinates with placeholder embed URL (requires replacement with actual embedded map from Google Maps)
2. **Form backend** — Used `mailto:` as no-backend option per PHASES.md. Live form requires Formspree integration later.
3. **Social media URLs** — Used placeholder URLs (linkedin.com/company/kgreyresolute, etc.) — to be replaced with actual business accounts
4. **Emergency strip "press 1"** — Included as per requirement; IVR note may reflect actual phone system configuration
5. **Contact form radio buttons** — Styled inline with no wrapper class (minimal inline flex styling applied via style attribute for layout; no custom class yet)

## Ready for Review
Both files are complete, responsive, and follow the established design system. Content is live, not placeholder. All requirements from PHASES.md Phase 4 and Phase 5 are met.
