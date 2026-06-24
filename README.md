# Handoff: Gina Dallison Coaching — Marketing Website

## Overview
A multi-section marketing website for **Gina Dallison Coaching** — a coach helping people living with chronic illness move "from struggle into a brighter world." The site has 8 pages and a long-form **Map of Wellness** sales/landing page. Visual direction is adapted from the *Zelva* nature-cottage template: pale + white sections alternating with deep forest-green blocks, sunset-orange accents, the Raleway typeface, photo-rich storytelling, subtle scroll animations, and a faint nature/butterfly parallax.

Brand line: **"Have Hope, Feel Better."**

## About the Design Files
The file in this bundle — `Gina Dallison Coaching.dc.html` — is a **design reference created in HTML** (a streaming "Design Component" prototype using a small custom runtime). It demonstrates the intended look, layout, content and behaviour. **It is not production code to ship directly.**

Your task is to **recreate this design in the target codebase's environment** using its established patterns and libraries. If there is no existing codebase yet, build it as a small static multi-page site or a lightweight React/Next.js (or Astro) app — whatever best fits hosting on GitHub Pages / Vercel / Netlify. Each "page" is currently a client-side view toggled by state; in a production build these can be real routes/pages or remain a single-page app.

Everything is **inline-styled** in the prototype (no CSS framework). Treat the inline styles as the spec; in production, move them into your styling system (CSS modules, Tailwind, styled-components, etc.).

## Fidelity
**High-fidelity (hifi).** Final colours, typography, spacing, imagery, copy and interactions are all intended as shown. Recreate pixel-closely, then adapt to your styling system. Real client copy and real photography are used throughout.

## Tech facts of the prototype (for reference)
- **Single root component** with a `page` state string controlling which view renders: `home | about | coaching | map | podcast | blog | community | contact`.
- A persistent fixed **top nav** and a shared **footer** wrap every page.
- **Font:** Raleway (Google Fonts), weights 300–800.
- **No images are hot-linked** — all assets are local in `/images` (see Assets).
- Booking CTAs link to **TidyCal**: `https://tidycal.com/ginadallisoncoaching/free-quick-chat` (open in new tab).

---

## Screens / Views

### Global — Navigation (fixed top bar)
- Full-width fixed bar, translucent dark-green (`rgba(15,40,28,0.32)`) with `backdrop-filter: blur(10px)`. On scroll past 40px it becomes solid `rgba(15,40,28,0.96)` with shadow `0 8px 30px rgba(0,0,0,0.25)`.
- Left: **white logo** image (`images/logo-white.png`), height ~`clamp(40px,4.2vw,50px)`, links home.
- Center/right: nav links (Home, About, Coaching, Map of Wellness, Podcast, Blog, Community, Contact) — white 14px/600, hover `#ffb877`; active link has a 2px orange underline.
- Right: **"Book a Call"** pill — orange `#ef7a1c`, white text, with a white circular `↗` badge. Links to TidyCal.

### Global — Footer
- Background deep green `#16382a`.
- Top: a 5-image gallery strip (rounded 12px) of nature/portrait photos.
- Columns: white logo + tagline paragraph · "Ways I Help" list · "Quick Links" (the nav labels) · "Newsletter" (email input + orange Subscribe button).
- List markers use an orange `»`.
- Bottom bar: `© 2026 Gina Dallison Coaching. All Rights Reserved.` / `Have Hope, Feel Better`.

### 1. Home
Sections top→bottom:
1. **Hero** — full-bleed photo (`journey-steps.jpg`) under a left-to-right dark-green gradient. Left column: orange "leaf" eyebrow, H1 *"Walk from struggle into a **brighter world**."* (the last two words `#ff9a44`), supporting paragraph, an orange "Start your journey" pill, and an avatar cluster ("Many souls already on the journey"). Right column: portrait (`gina-hero.jpg`) in an **arched frame** (`border-radius: 230px 230px 24px 24px`) with a **spinning circular badge** ("HAVE HOPE · FEEL BETTER ·" rotating, center orange `↗`, `@keyframes spin` 16s linear).
2. **Stat bar (overlapping)** — two white rounded cards (`100%` / Whole-person approach + a Free-discovery-call card). This bar **straddles the seam** between the dark hero and the white section below using a negative top margin (`margin-top: clamp(-104px,-7.5vw,-68px)`, `z-index:6`). Reproduce this overlap.
3. **Intro trio** — three cards: a pale-green stat card, a photo, and a dark-green message card.
4. **About** — image with an overlapping "Discover Gina" orange pill + heading + 4 "specialties" with `»` markers.
5. **Services** — 4 photo cards ("Ways I can help"). **A faint pale pine-forest silhouette sits behind these cards and drifts on scroll (parallax).**
6. **Programmes** — 2 wide image cards (Map of Wellness, Healing Vibrations) with left dark gradient + "Read more" pill.
7. **Video CTA band** — dark photo band, heading + "Get in touch" + a circular "Play film" button.
8. **Why work with me** — feature list (2 items) + overlapping images. **A faint large butterfly silhouette sits behind this section and drifts on scroll (parallax).**
9. **Roles** — 4 round-photo cards: Speaker · Author · Coach · Broadcaster.
10. **Pricing** — 3 plans (Free Discovery Call / Map of Wellness / 1:1 Coaching). Middle plan is **highlighted** (orange tab, raised `translateY(-14px)`, dark body).
11. **FAQ** — accordion (one open at a time); open item is dark green with a white `–`, closed items white with an orange `+`. Plus an arched photo with a small "You-led / always at your pace" badge.
12. **Blog** — 3 post cards.
13. **Contact** — headshot + intro card, and a photo-backed form (First/Last name, Email, Number, Send Message).

### 2. About
Dark photo banner with centered title + breadcrumb (`Home » About`). Then: story (overlapping images + 2 paragraphs of core copy + specialties), a dark-green pull-quote band, the 4 Roles cards, a "Kind words" reviews section (2 cards, orange stars), and a closing CTA band.

### 3. Coaching ("Work With Me")
Banner → intro → 4 service photo cards → 3-plan pricing (same as Home) → closing CTA band.

### 4. Map of Wellness — **long-form sales page** (most important)
Order, all from the client's wireframe:
1. **Hero** over `journey-steps.jpg` — a white pin-logo chip ("A 12-WEEK 1:1 PROGRAMME"), H1 **"Map to Wellness"**, orange sub-headline ("Create your personalised route to health, clarity and a life you actually want to live."), supporting line, an italic emotional hook with an orange left border, and the booking CTA.
2. **"Does this feel familiar?"** (pale) — 5 list items + a dark-green bridge card: *"You're not broken. **You're just stuck without a clear path.**"*
3. **"The Shift"** (white) — heading + 4 check items.
4. **ABC Framework** (dark green) — the **green ABC map graphic** (`images/m2w-map.png`) full-width + 3 cards: A Acceptance & Awareness · B Beliefs & Breathwork · C Courage & Consistent Change (orange letter badges).
5. **What you get** (white) — 6 items, each with a leaf badge.
6. **The result** (pale) — 5 green-check items.
7. **For you / Not for you** (white) — two columns (green ✓ / red ✕).
8. **Testimonials** (pale) — 4 cards (Michael Villines, Irina Ramirez, Harriet Connides, Andrew Bradshaw). **Use initial-monogram avatars, not stock faces** (these are real people).
9. **Why me** (white) — headshot in an arched frame + the "I'm Gina… living with Multiple Sclerosis… This isn't theory. This is lived." copy.
10. **Investment** (pale) — big **£997** card, "Payment plan available on request", a reframe note, and the booking CTA.
11. **FAQ** (white) — 6 static Q&A cards (incl. payment plan).
12. **Closing** (dark photo) — *"Time will pass anyway. The question is… Will you still be in the same place in 3 months?"* + strong booking CTA.
13. **Trust bar** (dark green) — 4 items (1:1 Personalised Support · Proven ABC Framework · Real Transformation · Compassionate Guidance).

> Note: client's wireframe text said `$997`; the client's own one-pager shows **£997**, which is used here. Confirm the currency.

### 5. Podcast ("Healing Vibrations")
Banner → intro (square image + platform chips: Spotify, Apple Podcasts, Amazon Music) → episode list (5 rows, orange play buttons) → CTA band.

### 6. Blog
Banner → filter chips → 6 post cards → CTA band.

### 7. Community
Banner → 2 large image cards (TikTok Live, The Healing Vibrations Network Facebook group) → CTA band.

### 8. Contact
Banner → contact section (headshot/intro + photo-backed form) → a dashed "Free resource — Diet Comparison Chart" download strip.

---

## Interactions & Behavior
- **Page routing:** state string toggles which view renders; nav + footer persist. On page change, scroll to top.
- **Nav scroll state:** translucent → solid green after 40px scroll (see hex above).
- **Scroll-reveal:** elements marked `data-reveal` start at `opacity:0; translateY(30px)` and animate to visible (`transition: opacity .7s, transform .7s`) via IntersectionObserver, with a ~1.6s fallback that reveals everything (so content is never stuck hidden). **Important:** set the hidden state from JS, not CSS, so content stays visible if JS fails.
- **Parallax silhouettes:** the forest (Services) and butterfly (Why-choose) shapes translate vertically based on their live viewport position, driven by a `requestAnimationFrame` loop (not scroll events — more robust), bounded to a small amplitude (forest ±~69px, butterfly ±~108px).
- **FAQ accordion (Home):** single-open; `faqOpen` index in state.
- **Testimonial slider (Home hero band):** prev/next cycle a `tIndex`.
- **Pricing:** middle plan visually raised + highlighted.
- **Hover:** buttons lift (`translateY(-2/3px)`) + deeper shadow; cards lift `translateY(-6/7px)` + shadow; images in cards can zoom subtly.
- **Spinning badge:** `@keyframes spin` 16s linear infinite on the hero circular-text SVG.
- **CTAs:** all "Book a call / Check if this is right" buttons link to the TidyCal URL (new tab).
- **Responsive:** layouts use `grid` with `repeat(auto-fit, minmax(...,1fr))` and `clamp()` for fluid type/padding — they reflow to single column on mobile without media queries. Reproduce the fluid behaviour.

## State Management
- `page: string` — current view.
- `faqOpen: number` — open FAQ index (Home).
- `tIndex: number` — active testimonial (Home hero band).
- No data fetching; all content is static. Newsletter/contact/booking forms are non-functional placeholders (wire to your provider; booking already points to TidyCal).

## Design Tokens

### Colours
| Token | Hex | Use |
|---|---|---|
| Forest green (deep) | `#16382a` | dark sections, footer, dark pricing body, nav (solid) |
| Forest green (darker) | `#0f2c20` | hero base, ABC section |
| Green (success/accent) | `#2f7d4a` | check icons, "for you", eyebrow text variants |
| Eyebrow green | `#2f5e3a` | small eyebrow labels |
| Sunset orange (primary) | `#ef7a1c` | buttons, accents, links, `»`/stars |
| Orange (gradient top) | `#f59a36` | button gradient start |
| Orange (light highlight) | `#ff9a44` | highlighted words on dark bg |
| Orange (deep, hover/text) | `#c0532b` / `#cf6a10` | "not for you" heading, link text |
| Warn red-orange | `#d9663f` | ✕ icons |
| Pale green A | `#eef6ea` | alternating light sections / chips |
| Pale green B | `#eaf4e6` | secondary light |
| White | `#ffffff` | white sections, cards |
| Text primary | `#2b3128` | body |
| Heading near-black | `#16281c` | headings on light |
| Text muted | `#5d685a` | secondary text |
| Text muted 2 | `#4a5548` | paragraph body |
| On-dark white | `rgba(255,255,255,0.66–0.92)` | text on green/photos |

### Typography
- Family: **Raleway** (`300, 400, 500, 600, 700, 800`).
- H1: `clamp(38px, 5–7vw, 68–86px)`, weight 800, `letter-spacing: -0.02em`, `line-height: ~1.0`.
- H2: `clamp(28px, 3.4–3.6vw, 44–46px)`, weight 800.
- Eyebrow: 13px, weight 700, often uppercase-ish, paired with a 16px orange "leaf" (`border-radius: 0 70% 0 70%`).
- Body: 14–17px, weight 400, `line-height: 1.5–1.7`.
- Buttons: 13–15px, weight 700.

### Spacing
- Section vertical padding: `clamp(56px–64px, 7–8vw, 100–110px)`.
- Page banner top padding: `clamp(140px, 20vh, 210px)` (clears fixed nav).
- Container max-widths: 1180px (content), 1080–1100px (tighter), 640–820px (text/forms).
- Card gaps: 16–24px.

### Radii
`14px` (small chips/cards) · `16–18px` · `20–24px` (cards/sections) · `999px` (pills) · arched frames `230px 230px 24px 24px` and `200–220px 200–220px 20px 20px`.

### Shadows
- Cards: `0 12px 30px rgba(20,40,25,0.06–0.08)`; hover `0 22px 48px rgba(20,40,25,0.16)`.
- Floating/hero: `0 24–30px 56–70px rgba(0,0,0,0.2–0.4)`.
- Buttons (orange): `0 10–12px 26–28px rgba(239,122,28,0.28–0.36)`.

### Button pattern (reuse everywhere)
Orange pill, white text, left-padded, with a trailing white circle (32–36px) containing an orange `↗`. Hover: lift + deeper shadow.

## Assets
All in `images/` (included in this bundle). Real photography of Gina + supplied brand graphics.

**Logo**
- `logo-full.png` — full-colour logo (green wordmark + orange "Have Hope, Feel Better" + orange heart mark), transparent bg, 800×400.
- `logo-white.png` — **white monochrome version** (generated from the full logo, recoloured + trimmed, 787×266) — used in nav + footer on dark green.

**Map of Wellness brand graphics**
- `m2w-map.png` — the green ABC "Map to Wellness" route graphic (1920×1080).
- `m2w-icon.jpg` — the yellow "Map to Wellness" pin icon (used as the hero chip mark).

**Photography** (Gina Dallison — supplied by client)
- `gina-hero.jpg`, `gina-orange-bridge.jpg`, `gina-flowers.jpg`, `gina-mug.jpg`, `gina-wisteria.jpg`, `gina-headshot.jpg`, `coaching-1to1.jpg`, `coaching-couple.jpg`, `speaking-life.jpg`, `speaking-podium.jpg`, `meditation.jpg`, `bench-estuary.jpg`, `journey-steps.jpg` (the "walking with sticks" image), `glider.jpg`.

**Fonts**
- Raleway via Google Fonts: `https://fonts.googleapis.com/css2?family=Raleway:wght@300;400;500;600;700;800&display=swap`.

**External links**
- Booking (all primary CTAs): `https://tidycal.com/ginadallisoncoaching/free-quick-chat`.

## Files
- `index.html` — **immediately hostable entry point** (a copy of the design). Together with `support.js` and `images/` it renders the full site as-is. Drop these on GitHub Pages / Netlify / Vercel and it works (loads React + Raleway from CDN). This is the quickest way to get the design live; the production rebuild (below) is the proper long-term path.
- `support.js` — the small runtime that powers `index.html` (keep it alongside `index.html`).
- `Gina Dallison Coaching.dc.html` — the design **source of truth** for layout, copy, colours and behaviour. Read it as a reference, not as code to ship verbatim.
- `images/` — all assets listed above.
- `screenshots/` — reference PNGs of each page (if included).

> A single fully-inlined offline HTML was not produced because inlining all the photography exceeds the 30 MB file limit — the multi-file `index.html` + `support.js` + `images/` above is the practical hostable artifact. If you specifically need one self-contained file, ask and I'll downscale the imagery and generate it.

---

## Getting this into your GitHub repo (`adamwatters03/ginadallisoncoaching`)

This bundle is a starting point. From a terminal (with Claude Code) in an empty folder:

```bash
# 1. Clone your (empty) repo, or init a new one
git clone https://github.com/adamwatters03/ginadallisoncoaching.git
cd ginadallisoncoaching

# 2. Copy the contents of this handoff bundle into the repo folder
#    (README.md, Gina Dallison Coaching.dc.html, images/)

# 3. Commit and push
git add .
git commit -m "Add Gina Dallison Coaching design handoff (reference + assets)"
git branch -M main
git push -u origin main
```

Then, in Claude Code, point it at this README and ask it to **build the production site** (e.g. a static multi-page site or an Astro/Next.js app) from the design reference, reusing the tokens and assets above. Recommended first prompt:

> "Read `design_handoff_gina_dallison_coaching/README.md` and the reference file `Gina Dallison Coaching.dc.html`. Build a production static website (mobile-first, accessible, no framework unless helpful) that recreates this design pixel-closely using the documented tokens and the assets in `images/`. Keep all real copy and the TidyCal booking links. Wire the contact + newsletter forms to placeholders I can connect later."
