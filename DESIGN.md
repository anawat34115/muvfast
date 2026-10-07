# DESIGN.md — MUVFAST Home (3 drafts, EN)

## 1. Visual Theme & Atmosphere
Clean, calm, search-first rental marketplace (ref: muvfast.com/en for content, zillow.com / apartments.com for header, photos and headline placement). White space and real room photos do the work. Client feedback: "too many colors, like candy" → **one accent colour only** (brand orange), everything else neutral.

| Draft | Concept | Hero | Feel |
|---|---|---|---|
| A — Open Search | Zillow-like | Full-bleed photo, centred headline, floating white search bar | Familiar, confident |
| B — Split Listing | Apartments.com-like | Text + stacked search left, photo pair right with "Min. 1 month" tag | Practical, listing-heavy |
| C — Quiet Type | Typography-first | Big headline on warm paper, one long search pill, photo strip below | Calm, editorial, most minimal |

## 2. Color Palette & Roles
Shared:
- brand #FC4A1A — logo, primary button, active states, min-stay tag. Never for large backgrounds.
- brand-dark #D63A0E — button hover, orange text under 18px (contrast)
- ink — headings/body: A #1B1D21, B #14171C, C #2A231E (warm)
- muted — secondary text: A #5E636B, B #5B6170, C #6E625A
- line — borders: A #E6E4E1, B #E4E6EA, C #E8E1D8
- surface-alt — alternate section: A #F6F5F3, B #F4F5F7, C #F3EEE7
- page — A/B #FFFFFF, C #FBF8F4

## 3. Typography
- A: Figtree 400/500/600/700 (H1 56/40, H2 36/28, body 16/1.6)
- B: Manrope 400/500/600/700 (H1 52/36, H2 34/26, body 16/1.6)
- C: Bricolage Grotesque 500/600 display (H1 88/44, tight −0.03em) + Onest 400/500 body
- Fallback stack adds Noto Sans Thai for the TH version. Client brand font CoStar Brown can replace A/B fonts once files arrive.

## 4. Component Stylings
- Header: 3-column grid — left: Landlord · Agent | centre: logo.svg (height 24–28) | right: EN/TH segmented toggle + "Sign in" (outline A, solid ink B, text+underline C). Mobile: menu button left, logo centre, Sign in right; drawer holds Landlord / Agent / language.
- Search: Location, Move-in, Duration (1–12 months), Budget / month, Search button (brand). Height 56 (desktop), fields stack on mobile.
- **Unit card (client spec)** — photo 4:3 with "Min. N mth" tag (brand) + photo count + heart; body lines: 1) price/mo + min stay, 2) BR · BA · sqm · Fl., 3) project name, 4) district, province.
- Benefit: icon 32 + title + one sentence. Lifestyle: 12 items (chip / tile / pill per draft).
- FAQ: native `<details>` accordion.
- Buttons: height 48 (56 hero), radius A 8 / B 8 / C 999 (pill), focus ring 2px brand offset 2px.

## 5. Layout Principles
8px grid: 8,16,24,32,40,48,56,64,80,96. Container 1200 + side padding 16 (mobile) / 32. Section padding 56 mobile / 80 desktop. Card gap 24.

## 6. Depth & Elevation
Flat. Borders over shadows. Only the floating search (A) and hover on cards use a soft shadow `0 8px 24px rgba(20,23,28,.08)`.

## 7. Do's and Don'ts
Do: one orange per view area, real photos, short copy from muvfast.com, min stay visible on every listing.
Don't: multiple accent colours, gradients, emoji icons, invented reviews/stats, copying the old menu, Material Icons.

## 8. Responsive Behavior
Breakpoints 768 / 1024. Cards 1 → 2 → 3 (A), carousel (B), 1 → 2 → 4 (C). Lifestyle grid 2 → 4 → 6. Touch targets ≥ 48.

## 9. Agent Prompt Guide
- "Read muvfast/DESIGN.md + chosen draft. Add the client's new section with the same header style (eyebrow + H2), 8px spacing, orange only for the primary action."
- "Unit card must keep the 4-line spec from REQUIREMENTS.md §4."

Motion: hero stagger 120ms + scroll reveal (IntersectionObserver), ease cubic-bezier(.16,1,.3,1), disabled by prefers-reduced-motion.
