# DESIGN.md — K Grey Resolute Visual Design System

## Design Philosophy

**Aesthetic Direction:** Tactical Refinement  
Dark, authoritative, and precise. The design communicates strength and professionalism without aggression. Think military-grade discipline expressed through clean typography, controlled negative space, and sharp gold accents — not flashy, but impossible to ignore.

**One Thing Visitors Should Remember:** "This company is serious, professional, and ready."

---

## Color Palette

```css
:root {
  /* Backgrounds */
  --bg-primary:     #0A0A0A;   /* Near black — main background */
  --bg-secondary:   #111111;   /* Slightly lighter — card backgrounds */
  --bg-tertiary:    #1A1A1A;   /* Section alternates */
  --bg-surface:     #222222;   /* Input fields, elevated cards */

  /* Accent — Gold / Amber */
  --accent:         #C9A84C;   /* Primary brand gold */
  --accent-light:   #E8C46A;   /* Hover states, highlights */
  --accent-dark:    #A07830;   /* Pressed states */
  --accent-subtle:  rgba(201, 168, 76, 0.12); /* Ghost/tinted backgrounds */

  /* Text */
  --text-primary:   #F5F5F0;   /* Main body text (warm white) */
  --text-secondary: #A8A8A0;   /* Subtext, captions */
  --text-muted:     #666660;   /* Disabled, placeholders */
  --text-inverse:   #0A0A0A;   /* Text on gold backgrounds */

  /* Status */
  --success:        #3A8C5C;
  --danger:         #C0392B;   /* Emergency/panic elements */
  --danger-light:   #E74C3C;

  /* Borders */
  --border:         rgba(255, 255, 255, 0.08);
  --border-accent:  rgba(201, 168, 76, 0.30);
}
```

---

## Typography

### Font Pairing
```css
/* Display / Headings */
@import url('https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;600;700&display=swap');
--font-display: 'Oswald', sans-serif;

/* Body / UI */
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&display=swap');
--font-body: 'DM Sans', sans-serif;

/* Mono / Labels */
@import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500&display=swap');
--font-mono: 'JetBrains Mono', monospace;
```

**Rationale:**
- **Oswald** — Condensed, authoritative. Military/security feel without being cliché. Great for big headlines.
- **DM Sans** — Clean, modern, highly legible for body text and forms.
- **JetBrains Mono** — Used sparingly for labels, PSIRA numbers, registration codes — adds a technical edge.

### Type Scale
```css
--text-xs:    0.75rem;   /* 12px — legal, footnotes */
--text-sm:    0.875rem;  /* 14px — captions, labels */
--text-base:  1rem;      /* 16px — body */
--text-lg:    1.125rem;  /* 18px — lead paragraphs */
--text-xl:    1.25rem;   /* 20px — card titles */
--text-2xl:   1.5rem;    /* 24px — section subtitles */
--text-3xl:   1.875rem;  /* 30px — section headings */
--text-4xl:   2.25rem;   /* 36px — page headings */
--text-5xl:   3rem;      /* 48px — hero headings */
--text-6xl:   3.75rem;   /* 60px — hero on desktop */
```

---

## Layout & Spacing

### Grid
- **Max container width:** 1280px
- **Content padding:** 24px (mobile), 48px (tablet), 80px (desktop)
- **Section vertical padding:** 80px (mobile), 120px (desktop)
- **Column system:** 12-column CSS Grid

### Spacing Scale
```css
--space-1:  4px
--space-2:  8px
--space-3:  12px
--space-4:  16px
--space-5:  20px
--space-6:  24px
--space-8:  32px
--space-10: 40px
--space-12: 48px
--space-16: 64px
--space-20: 80px
--space-24: 96px
```

---

## Component Design Specs

### Navbar
- **Height:** 72px (desktop), 64px (mobile)
- **Background:** `var(--bg-primary)` with `backdrop-filter: blur(12px)` when scrolled
- **Border-bottom:** `1px solid var(--border)` when scrolled
- **Logo:** Left-aligned, white + gold accent
- **Nav links:** DM Sans 500, 14px, `var(--text-secondary)` → `var(--accent)` on hover
- **CTA Button:** Gold filled, "Get a Quote"
- **Sticky:** Yes, `position: sticky; top: 0; z-index: 100`

### Hero Section
- **Height:** 100vh (home), 50vh (inner pages)
- **Background:** Dark image overlay (`rgba(0,0,0,0.65)`) over security-related imagery
- **Layout:** Left-aligned text (60%), image/visual right (40%)
- **Pre-headline:** Mono font, gold color, uppercase tracked — e.g., `— PSIRA REGISTERED —`
- **Headline:** Oswald 700, 56-72px, white, letter-spacing: -0.02em
- **Body:** DM Sans 300, 18px, `var(--text-secondary)`, max-width 480px
- **CTAs:** Primary gold button + ghost white button

### Buttons
```css
/* Primary */
.btn-primary {
  background: var(--accent);
  color: var(--text-inverse);
  font: 600 14px var(--font-body);
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 14px 32px;
  border: none;
  cursor: pointer;
  transition: background 0.2s;
}
.btn-primary:hover { background: var(--accent-light); }

/* Ghost */
.btn-ghost {
  background: transparent;
  color: var(--text-primary);
  border: 1px solid var(--border);
  /* same size as primary */
}
.btn-ghost:hover { border-color: var(--accent); color: var(--accent); }

/* Danger (Emergency) */
.btn-danger {
  background: var(--danger);
  color: white;
}
```

### Service Cards
- **Background:** `var(--bg-secondary)`
- **Border:** `1px solid var(--border)` → `var(--border-accent)` on hover
- **Border-left accent:** `3px solid var(--accent)` (signature detail)
- **Icon:** Gold, 32px
- **Title:** Oswald 600, 20px, white
- **Body:** DM Sans 400, 14px, `var(--text-secondary)`
- **Hover:** Slight lift `translateY(-4px)`, border color shift

### Stats Bar
- **Background:** `var(--accent)` (gold band)
- **Text:** `var(--text-inverse)` (black)
- **Numbers:** Oswald 700, 48px
- **Labels:** DM Sans 500, 12px uppercase

### Testimonial Cards
- **Opening quote mark:** Oswald 700, 80px, `var(--accent)`, opacity 0.3
- **Quote text:** DM Sans 300 italic, 16px
- **Author:** DM Sans 600, 14px, gold accent
- **Star rating:** Gold stars

### Form Inputs
```css
input, select, textarea {
  background: var(--bg-surface);
  border: 1px solid var(--border);
  color: var(--text-primary);
  font: 400 15px var(--font-body);
  padding: 14px 16px;
  border-radius: 2px; /* near-square — tactical feel */
}
input:focus {
  border-color: var(--accent);
  outline: none;
  box-shadow: 0 0 0 3px var(--accent-subtle);
}
```

### Compliance/Badge Section
- Display as a horizontal row of `badge cards`
- Each card: dark background, centered icon + name + registration number in mono font
- Border: thin gold

---

## Imagery Guidelines

> Until real photography is available, use high-quality stock imagery from Unsplash or Pexels.

**Recommended search terms:**
- "security guard professional dark"
- "armed response vehicle"
- "CCTV control room monitoring"
- "VIP protection bodyguard"
- "security team night patrol"

**Image treatment:**
- All hero images: dark overlay `rgba(0,0,0,0.6)` minimum
- Use `object-fit: cover` with consistent aspect ratios
- Avoid images with text or logos
- Prefer images with strong diagonal composition

---

## Motion & Animation

**Principle:** Intentional, fast, military-precise. No bouncing or playful easing.

```css
/* Standard easing */
--ease-standard: cubic-bezier(0.25, 0.1, 0.25, 1.0);
--ease-out:      cubic-bezier(0.0, 0.0, 0.2, 1.0);
--ease-sharp:    cubic-bezier(0.4, 0.0, 0.6, 1.0);

/* Durations */
--duration-fast:   150ms;
--duration-normal: 250ms;
--duration-slow:   400ms;
```

**Animations to implement:**
- Page load: staggered fade-up on hero elements (delay: 0ms, 150ms, 300ms, 450ms)
- Scroll reveal: `IntersectionObserver` → fade-up + opacity for sections
- Stat counters: Number count-up animation when stats section enters viewport
- Card hover: `transform: translateY(-4px)` with border color transition
- Nav: Background blur appears after 80px scroll

---

## Responsive Breakpoints

```css
/* Mobile first */
--bp-sm:  480px
--bp-md:  768px
--bp-lg:  1024px
--bp-xl:  1280px
--bp-2xl: 1536px
```

**Key responsive behaviors:**
- Hamburger menu below 1024px
- Hero text switches to centered on mobile
- Service cards: 1 col (mobile) → 2 col (tablet) → 3 col (desktop)
- Stats bar: 2×2 grid on mobile, 4-across on desktop
- Footer: stacked on mobile, 4-column on desktop

---

## Special Design Details (Signature Touches)

1. **Thin gold top bar** — 3px gold line at very top of every page (brand signature)
2. **Section label style** — Every section has a pre-label: `— Section Name —` in mono font, gold, centered above headings
3. **Left border accent on cards** — 3px gold left border on service/feature cards
4. **Number formatting** — Stats use mono font; PSIRA and reg numbers always in mono
5. **WhatsApp FAB** — Floating green WhatsApp button bottom-right, on every page
6. **Emergency strip** — Thin red banner option at top: "24/7 Emergency: +27 61 582 6087"
7. **Gold dividers** — Sections separated by `<hr>` styled as thin gold lines with decorative center diamond

---

## Favicon & Logo Notes

- Logo should be designed as: Shield icon (grey/silver) + "K GREY RESOLUTE" in Oswald
- Favicon: Shield icon on dark background, 32×32
- Use SVG for scalability
- Always display logo in white/gold on dark backgrounds

---

## Implementation Notes

- All CSS must be externalized into separate stylesheet files (see PLAN.md `css/` directory).
- Use the CSS custom properties defined above in `variables.css`.
- Organize component styles into logical CSS files: layout, components, utilities, animations.
- No inline styles or embedded `<style>` tags are permitted in HTML files.