# Foyle International — Agent Briefing & Design System

This file is your first read on every session. Follow these rules exactly.
Do not deviate from the design system below without being explicitly asked to.

---

## Project Overview

**Client:** Foyle International — private English language school, Derry, Northern Ireland  
**Founded:** 1990 by Director Paul Murray  
**Site type:** Single-page marketing website  
**Goal:** Present courses clearly to international students and drive enquiries  

---

## File Structure

```
files/
  index.html        ← The entire site. One file. Do not split this.
  images/
    foyle-logo.png  ← The real Foyle logo. Celtic green lettering on black.
CLAUDE.md           ← This file
```

**Critical rules on structure:**
- This is intentionally a single `index.html` file. Do NOT suggest splitting into components, pages, or partials.
- Do NOT introduce React, Vue, Next.js, Tailwind, Node, PostCSS, or any build tools.
- Do NOT create `package.json`, `node_modules`, or any config files.
- Plain HTML + CSS + vanilla JS only. That is a feature, not a limitation.

---

## Design System

### Colour Palette

```css
--foyle-green: #3FA535;       /* Primary brand green — matches the logo exactly */
--foyle-green-dark: #2d7a25;  /* Darker green for text on light backgrounds */
--foyle-green-deep: #1a4f18;  /* Deepest green for headings/emphasis */
--foyle-green-pale: #f0f9ee;  /* Very light green tint for backgrounds */
--foyle-green-mid: #d9eed4;   /* Mid green for borders and chips */
--black: #0a0a0a;             /* Near-black for footer, dark sections */
--cream: #faf8f3;             /* Main page background — warm off-white */
--paper: #f5f2ea;             /* Slightly warmer than cream, used for Derry section */
--ink: #1a1a18;               /* Primary text colour */
--ink-soft: #545450;          /* Secondary/muted text */
--rule: #e2ddd0;              /* Border and divider colour */
--accent: #c89a3e;            /* Gold — use sparingly, currently unused */
```

### Typography

| Role | Font | Notes |
|---|---|---|
| Display headings (h1, h2) | Fraunces | Serif, italic for emphasis, weight 400–500 |
| Body copy / descriptions | Newsreader | Serif, warm and editorial |
| UI / labels / nav / buttons | Instrument Sans | Clean, uppercase for labels |
| Handwritten accents | Caveat | Used only for the founder signature |

**Font import is already in the `<head>`. Do not change it.**

All fonts loaded from Google Fonts:
```
Fraunces, Newsreader, Inter Tight, Instrument Sans, Caveat
```

### Spacing & Layout

- Max content width: `1400px` centred with `margin: 0 auto`
- Section padding: `8rem 2rem` desktop, `5rem 2rem` mobile
- Responsive breakpoint: `960px` — below this, everything collapses to single column
- The nav is fixed at `72px` height — all hero sections have `padding-top: 9rem` to compensate

---

## Site Sections (in order)

| # | Section | ID | Background |
|---|---|---|---|
| Nav | Fixed navigation | — | White (`rgba(255,255,255,0.95)`) |
| 1 | Hero | `#home` | Cream (`--cream`) |
| — | Stats strip | — | Foyle green (`--foyle-green`) |
| 2 | About | `#about` | Cream |
| 3 | Courses | `#courses` | Black (`--black`) |
| 4 | Derry | `#derry` | Paper (`--paper`) |
| 5 | Testimonials | `#testimonials` | Cream |
| 6 | Host a Student | `#host` | Foyle green |
| 7 | Contact + Form | `#contact` | Cream |
| — | Footer | — | Black |

---

## Navigation

- White background (`rgba(255,255,255,0.95)`) with blur backdrop
- Logo sits directly on the white nav — no background container. The PNG has a transparent background so the Celtic green lettering sits cleanly on white.
- Nav links are dark ink coloured, hover to `--foyle-green-dark`
- CTA button: green background, black text, pill shape (`border-radius: 100px`)
- Below 960px: hamburger menu, full-screen black overlay mobile menu

---

## Courses Currently Offered

Only these four. Do NOT add OET or CELTA — they are no longer offered.

1. **Erasmus+ Programmes** — Staff & student mobilities, Derry/Dublin/Donegal, EU funded
2. **Junior Summer Schools** — Ages 13–17, groups & individuals, summer only
3. **Vocational & Educational Training (VET)** — Professional + language skills, EU framework
4. **General English & Exam Prep** — All levels, small classes

---

## Key Business Facts

- **Address:** 72 Great James Street, Derry, BT48 7DE, Northern Ireland
- **Phone:** +44 28 71 371 535
- **Email:** info@foyle.eu
- **Domain:** foyle.eu
- **Locations:** Derry/Londonderry, Dublin, Donegal, Sligo
- **Accreditation:** British Council (first school in Northern Ireland to receive it)
- **Erasmus+:** Official partner
- **Founded:** 1990, Director Paul Murray

---

## Contact Form

- Simple fields: First name, Last name, Email, Country, Area of interest (dropdown), Message
- On submit: hides the form, shows a success message with the user's email confirmed
- No backend — this is a frontend-only form. It does not actually send emails yet.
- **Do not add a backend or external form service unless explicitly asked.**

---

## Image Placeholders

The site has placeholder divs where photos will go. These are intentional.
Do NOT replace them with stock photos or external image URLs.
When the client provides real photos, they will be added to `images/` and swapped in.

Current placeholder locations:
- About section: school/classroom photo (aspect ratio 3:4)
- Derry section: city photos (currently not rendered on mobile)

---

## Tone & Copy Rules

- Warm, confident, not corporate
- Irish hospitality is the key brand feeling
- Short sentences in body copy
- Headers use Fraunces italic for emotional emphasis: e.g. `Learn English <em>in the</em>`
- Section numbers follow pattern: `01 — Our story`, `02 — Our courses`, etc.

---

## What Good Looks Like

Before making any change, ask yourself:
- Does this maintain the editorial serif aesthetic?
- Does it work at 375px mobile width?
- Does it stay within the colour palette?
- Does it avoid adding new dependencies?

If yes to all four — proceed. If no to any — flag it before making the change.

---

*Last updated by Claude · April 2026*