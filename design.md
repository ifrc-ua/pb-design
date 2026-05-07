---
version: 1.2.0
name: Participatory Budgeting Ivano-Frankivsk
description: Design system for the Participatory Budget (PB) of Ivano-Frankivsk. Optimized for AI-driven analytics, UI generation, and municipal infographics.
colors:
  # Brand — purple
  primary-900: "#4E3C84"
  primary-500: "#654EA3"
  primary-300: "#7B66B8"
  primary-200: "#9C8BCC"
  primary-100: "#EEEAF7"
  primary-50: "#F6F4FB"
  # Brand — yellow
  secondary-700: "#E6D307"
  secondary-500: "#FFEC08"
  secondary-300: "#FFF266"
  secondary-100: "#FFF9B3"
  # Surface aliases (canvas == neutral-0; ink == neutral-900 — kept for semantic clarity)
  canvas: "#FDFDFD"
  ink: "#1A1A1A"
  # Neutrals — 10-step scale
  neutral-0: "#FDFDFD"
  neutral-50: "#F7F7F8"
  neutral-100: "#EFEFF1"
  neutral-200: "#E2E2E6"
  neutral-300: "#CACAD1"
  neutral-400: "#9FA0A9"
  neutral-500: "#71737E"
  neutral-700: "#3F4049"
  neutral-900: "#1A1A1A"
  neutral-950: "#0D0D12"
  # Semantic
  success: "#2F8F4E"
  success-tint: "#E8F3EC"
  success-ink: "#1E6B39"
  info: "#2563EB"
  warning: "#D97706"
  error: "#DC2626"
typography:
  # fontSize values below are DESKTOP defaults (1024px+).
  # For mobile/tablet scaling, see §3 "Responsive Type Scale" — never apply 96px hero on a 375px screen.
  display-hero:
    fontFamily: "Phenomena"
    fontSize: 96px
    fontWeight: 900
    lineHeight: 1.0
    letterSpacing: -2px
  title-h1:
    fontFamily: "Phenomena"
    fontSize: 64px
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: -0.8px
  title-h2:
    fontFamily: "Phenomena"
    fontSize: 40px
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: -0.4px
  title-h3:
    fontFamily: "Phenomena"
    fontSize: 28px
    fontWeight: 400
    lineHeight: 1.25
    letterSpacing: -0.2px
  body-lg:
    fontFamily: "Proxima Nova"
    fontSize: 20px
    fontWeight: 400
    lineHeight: 1.55
  body-md:
    fontFamily: "Proxima Nova"
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.55
  body-sm:
    fontFamily: "Proxima Nova"
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  label-bold:
    fontFamily: "Proxima Nova"
    fontSize: 12px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: 1px
  data-stat:
    fontFamily: "Phenomena"
    fontSize: 72px
    fontWeight: 900
    lineHeight: 1.0
  title-feature:
    fontFamily: "Proxima Nova"
    fontSize: 20px
    fontWeight: 600
    lineHeight: 1.30
  caption:
    fontFamily: "Proxima Nova"
    fontSize: 12px
    fontWeight: 500
    lineHeight: 1.40
  data-label:
    fontFamily: "Proxima Nova"
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.30
rounded:
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 24px
  pill: 999px
spacing:
  xxs: 4px
  xs: 8px
  sm: 12px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  section: 96px
components:
  button-primary:
    backgroundColor: "{colors.primary-500}"
    textColor: "{colors.canvas}"
    typography: "{typography.body-md}"
    fontWeight: 600
    rounded: "{rounded.sm}"
    padding: 12px 24px
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.primary-500}"
    border: "1.5px solid {colors.primary-500}"
    rounded: "{rounded.sm}"
    padding: 12px 24px
  button-accent:
    backgroundColor: "{colors.secondary-500}"
    textColor: "{colors.ink}"
    border: "1px solid {colors.ink}"
    rounded: "{rounded.sm}"
    padding: 12px 24px
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.neutral-700}"
    typography: "{typography.body-md}"
    fontWeight: 500
    rounded: "{rounded.sm}"
    padding: 12px 24px
    hoverBackgroundColor: "{colors.neutral-100}"
  checkbox:
    backgroundColorUnchecked: "{colors.canvas}"
    backgroundColorChecked: "{colors.primary-500}"
    border: "1.5px solid {colors.neutral-300}"
    checkmarkColor: "{colors.canvas}"
    rounded: "{rounded.xs}"
  toggle:
    trackInactive: "{colors.neutral-300}"
    trackActive: "{colors.primary-500}"
    thumb: "{colors.canvas}"
    rounded: "{rounded.pill}"
  focus-ring:
    outline: "2px solid {colors.primary-500}"
    outlineOffset: 2px
  card-project:
    backgroundColor: "{colors.canvas}"
    border: "1px solid {colors.neutral-100}"
    rounded: "{rounded.md}"
    padding: 20px
  card-stat:
    backgroundColor: "{colors.primary-50}"
    rounded: "{rounded.lg}"
    padding: 24px
  badge-winner:
    backgroundColor: "{colors.secondary-500}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: 4px 10px
  progress-bar-fill:
    backgroundColor: "{colors.primary-500}"
    rounded: "{rounded.pill}"
    height: 8px
  dropdown-filter:
    backgroundColor: "{colors.canvas}"
    border: "1px solid {colors.neutral-200}"
    rounded: "{rounded.sm}"
    padding: 10px 14px
  year-slider:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-sm}"
  top-nav:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-md}"
  badge-implemented:
    backgroundColor: "{colors.success-tint}"
    textColor: "{colors.success-ink}"
    rounded: "{rounded.pill}"
    padding: 4px 10px
  section-standard:
    backgroundColor: "{colors.canvas}"
    padding: "{spacing.section}"
  section-hero:
    backgroundColor: "{colors.primary-50}"
    padding: "{spacing.section}"
    rounded: "{rounded.xl}"
shadows:
  level-0: "none"
  level-1: "0 1px 2px rgba(26, 26, 26, 0.04)"
  level-2: "0 4px 12px rgba(26, 26, 26, 0.06)"
  level-3: "0 12px 32px rgba(26, 26, 26, 0.10)"
  level-4: "0 24px 64px rgba(26, 26, 26, 0.14)"
---

# Design System Overview — Participatory Budgeting IF

> *[🇺🇦 Читати українською (Read in Ukrainian)](design.ua.md)*

## TL;DR (for AI agents and impatient readers)

- **Brand colors**: purple `#654EA3` + yellow `#FFEC08` on near-white `#FDFDFD`, text `#1A1A1A`.
- **Fonts**: `Phenomena` for display/headings/big numbers; `Proxima Nova` for everything else. Fallbacks (when commercial fonts unavailable): `Inter Tight` + `Inter` via Google Fonts CDN.
- **Numbers**: always use `tabular-nums`; thousands separator is a non-breaking space (`14 832`, never `14,832`); decimal separator is comma (`3,7%`).
- **Yellow rule**: yellow is an accent, never a large fill. In charts, yellow segments always carry a `#1A1A1A` 1.5px outline.
- **Layout**: mobile-first (test at 375px first); `8/12px` radii for buttons/cards; `96px` between sections; `tabular-nums` everywhere there are digits.
- **Scope**: 10 years of historical PB data across the 2016–2026 timeframe (no PB held in 2022). Not active voting cycles, no dark mode, no admin UI, no submission forms.
- **YAML > prose**: when YAML frontmatter and prose disagree, YAML is the source of truth.

The full document below explains the *why* behind each rule — read it once, then come back for reference.

---

This document defines the visual standards, tokens, and interface guidelines for the Participatory Budgeting ecosystem of Ivano-Frankivsk. The system is optimized for AI agents, analytical infographics, and municipal reporting.

---

## 1. Visual Theme & Atmosphere

Participatory Budgeting is a municipal tool that exists at the intersection of two energies: **civic trust** (calmness, transparency, order) and **active participation** (movement, voice, choice). The design system is built around this duality. Phenomena — a condensed, broad, almost architectural sans-serif — acts as the hero voice: used in display headings, sections, and record-breaking numbers. Its geometric nature and clean outlines evoke public spaces, feeling official yet approachable. Proxima Nova — a versatile workhorse typeface — handles dense interface layers, analytical labels, long project descriptions, and data tables.

The palette relies on two core logo colors: **Purple `{colors.primary-500}`** (`#654EA3` - seriousness, authority, creativity) and **Yellow `{colors.secondary-500}`** (`#FFEC08` - energy, voice, visibility). Purple acts as the document's ink, while yellow serves as a highlighter for what's most important. The background is an off-white (`{colors.canvas}`), and text is deep graphite (`{colors.ink}`) — pairing perfectly for maximum readability and data focus. We practice strict color discipline: the core relies only on the two brand colors plus neutral grays. An extended data-viz palette (for charts needing 5+ categories) lives in a separate `design-data.md` file, which is created only when genuinely needed.

The aesthetic is restrained infographics: abundant white space, clear grids, large numbers acting as composition heroes, crisp 1.5px icons, soft (8–12px) border radii on cards, and barely visible shadows. No neon gradients, no decorative animations — everything serves data readability and trust.

**Key Characteristics:**
- Two typefaces: Phenomena (`{typography.display-hero}`) for display/headings & Proxima Nova (`{typography.body-md}`) for UI, text, data.
- Two-color brand identity: Purple `{colors.primary-500}` & Yellow `{colors.secondary-500}`.
- Core Data-viz: Primary shades + yellow. The full categorical palette (11 canonical categories) lives in [design-data.md](./design-data.md).
- Historical, analytical focus: The system is designed to visualize **10 years of PB data across the 2016–2026 timeframe** (PB was not held in 2022), not to run the current voting cycle.
- Yellow `{colors.secondary-500}` is always a marker of IMPORTANCE (winner `{components.badge-winner}`, accent, CTA), never a background for large areas.
- Subtle shadows, `{spacing.xs}` (8px) grid, wide gutters — municipal trust equals "room to breathe."
- Mobile-first: The website and social media content are primarily consumed on mobile devices.

---

## 2. Color Palette & Roles

### Brand Core (from the logo)
| Role | HEX | RGB | Application |
|---|---|---|---|
| **Primary** — Purple | `#654EA3` | 101, 78, 163 | Display headings, primary CTAs, active states, brand surfaces |
| **Secondary** — Yellow | `#FFEC08` | 255, 236, 8 | "This is important" accent, winner badge, highlights, CTA underlines |
| **Background** — Off-white | `#FDFDFD` | 253, 253, 253 | Main page and card background |
| **Text** — Graphite | `#1A1A1A` | 26, 26, 26 | Body text, numbers, data |

### Primary Shades (Purple)
| Role | HEX | Application |
|---|---|---|
| Primary-900 (dark) | `#4E3C84` | Hover/active, pressed button, dark accents |
| Primary-500 (base) | `#654EA3` | Base primary (from brandbook) |
| Primary-300 (tint) | `#7B66B8` | Secondary buttons, border emphasis |
| Primary-200 (light) | `#9C8BCC` | Underlays, disabled states |
| Primary-100 (bg-tint) | `#EEEAF7` | Section card backgrounds, hover backgrounds |
| Primary-50 (surface) | `#F6F4FB` | Lightest purple — smooth sections |

### Secondary Shades (Yellow)
| Role | HEX | Application |
|---|---|---|
| Secondary-700 (dark) | `#E6D307` | Hover for yellow CTAs, dark accent |
| Secondary-500 (base) | `#FFEC08` | Base secondary (from brandbook) |
| Secondary-300 (tint) | `#FFF266` | Soft accent |
| Secondary-100 (bg-tint) | `#FFF9B3` | Text highlighter, winner badge background |

### Neutrals (10 steps)
| Token | HEX | Application |
|---|---|---|
| neutral-0 | `#FDFDFD` | Background |
| neutral-50 | `#F7F7F8` | Page subtle, striped rows |
| neutral-100 | `#EFEFF1` | Dividers, light borders |
| neutral-200 | `#E2E2E6` | Borders, input-rest |
| neutral-300 | `#CACAD1` | Disabled border, subtle emphasis |
| neutral-400 | `#9FA0A9` | Placeholder, muted text |
| neutral-500 | `#71737E` | Secondary text |
| neutral-700 | `#3F4049` | Body on light, subtitle |
| neutral-900 | `#1A1A1A` | Text primary |
| neutral-950 | `#0D0D12` | Overlay, max-contrast display |

### Semantic
| Role | HEX | Application |
|---|---|---|
| Success | `#2F8F4E` | "Implemented", positive delta in stats |
| Info | `#2563EB` | Informational messages, neutral states |
| Warning | `#D97706` | Admin warnings, "data attention" alerts |
| Error | `#DC2626` | Form errors, "not implemented" (for nuances — neutral is preferred) |

### Status Badges (Core)

Two universal badges needed by any user of the system — including an individual author designing a poster or presentation for their winning project.

| Label | Background | Text | Usage |
|---|---|---|---|
| Переможець року (Winner) | `#FFEC08` (Secondary-500) | `#1A1A1A` | Winning project of the year's vote |
| Реалізовано (Implemented) | `#E8F3EC` (tint Success) | `#1E6B39` | Project completed after winning |

> The full set of **6 real statuses** from the PB data (Implemented, In Progress, Participated, Rejected, Permanently Rejected, Impossible to Implement) lives in [design-data.md](./design-data.md) §6 for analytic dashboards. We keep this section minimal because these two badges are the only ones needed for promo, pitch, and project-specific materials.

### Core Data-viz

For most charts, the brand colors are sufficient:
- **Primary shades** (6 shades of purple) — gradation for 2-4 series; also functions as a sequential scale for heatmaps / choropleths (Primary-50 → Primary-900).
- **Yellow `#FFEC08`** — accent for the most critical data point/line/bar. On a white background, always pair with a dark `#1A1A1A` 1–1.5px outline.
- **Neutrals 100–500** — for auxiliary series, comparative "plan/actual" bars.

> The full categorical palette (11 canonical categories with stable colors and Lucide icons) and the year-by-year mapping of real PB categories 2016–2026 — live in [design-data.md](./design-data.md) §4 and §3. Pull category fills from `{data.canonical-categories.<key>.color}` rather than inventing HEX values.

### Contrast (WCAG AA)
Verified pairs:
- `#1A1A1A` on `#FDFDFD` — 19.3:1 ✓ AAA
- `#FDFDFD` on `#654EA3` — 6.7:1 ✓ AA
- `#1A1A1A` on `#FFEC08` — 16.1:1 ✓ AAA
- `#654EA3` on `#FDFDFD` — 7.0:1 ✓ AA
- `#71737E` (neutral-500) on `#FDFDFD` — 4.7:1 ✓ AA (for muted text)

> **DO NOT use:** white text on yellow, or purple on yellow (both fail AA accessibility).

---

## 3. Typography Rules

### Font Families
- **Display/Headings**: `Phenomena` (commercial license, not bundled), fallback: `'Inter Tight', system-ui, sans-serif`
- **Body/UI**: `Proxima Nova` (commercial license, not bundled), fallback: `'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`
- **Numerics/Data**: `Proxima Nova` with `font-variant-numeric: tabular-nums` — mandatory for tables, dashboards, and charts.

### Font Substitutes (when commercial fonts are unavailable)

External AI tools (Lovable, v0, Stitch, Canva) and third-party presentations do not bundle Phenomena or Proxima Nova. Use these substitutes — and apply the listed corrections, otherwise the typographic rhythm collapses.

| Original | Substitute | Correction |
|---|---|---|
| Phenomena (display, headings) | `Inter Tight` 900 | Inter Tight has slightly wider counters; reduce letter-spacing by an additional `-0.5px` at sizes 64px+. |
| Proxima Nova (UI, body) | `Inter` (regular/semibold/bold) | Inter line-height runs 2–3% taller; tighten `body-md` line-height from 1.55 → 1.50, `body-lg` from 1.55 → 1.45. |
| Proxima Nova `tabular-nums` | `Inter` with `font-variant-numeric: tabular-nums` | Mandatory — Inter's default proportional digits will misalign tables. |

> Geist Sans/Geist Mono are acceptable secondary fallbacks if Inter is also unavailable.
> Never substitute Phenomena with a serif, slab, or display script — the system loses its architectural calm.

### Available Weights
- **Phenomena**: Thin (100), ExtraLight (200), Light (300), Regular (400), Bold (700), ExtraBold (800), Black (900)
- **Proxima Nova**: Thin (100), Light (300), Regular (400), Semibold (600), Bold (700), Extrabold (800), Black (900) — all with Italics.

### Hierarchy

| Token | Font | Size | Weight | Line Height | Letter Spacing | Use |
|---|---|---|---|---|---|---|
| `{typography.display-hero}` | Phenomena | 72–96px | 900 (Black) | 1.00 | -1.5px to -2px | Hero numbers, landing title, "10 years of PB" |
| `{typography.title-h1}` | Phenomena | 48–64px | 700 (Bold) | 1.05 | -0.8px | Main screen heading |
| `{typography.title-h2}` | Phenomena | 32–40px | 700 (Bold) | 1.15 | -0.4px | Page sections |
| `{typography.title-h3}` | Phenomena | 24–28px | 400 (Regular) | 1.25 | -0.2px | Section subheading |
| `{typography.title-feature}` | Proxima Nova | 20–24px | 600 (Semibold) | 1.30 | normal | Project card name, widget title |
| `{typography.body-lg}` | Proxima Nova | 18–20px | 400 (Regular) | 1.55 | normal | Intro paragraphs, descriptions |
| `{typography.body-md}` | Proxima Nova | 16px | 400 (Regular) | 1.55 | normal | Main text |
| `{typography.body-sm}` | Proxima Nova | 14px | 400 (Regular) | 1.50 | normal | Auxiliary text, metadata |
| `{typography.caption}` | Proxima Nova | 12–13px | 500 (Medium) | 1.40 | normal | Chart/image captions |
| `{typography.label-bold}` | Proxima Nova | 11–12px | 600 (Semibold) | 1.20 | +1px (uppercase) | Section labels, tags |
| `{typography.data-stat}` | Phenomena | 48–72px | 900 (Black) | 1.00 | -1px, tabular-nums | "14 832 голоси", "₴5.2 млн" |
| `{typography.data-label}` | Proxima Nova | 11–13px | 400 (Regular) | 1.30 | normal, tabular-nums | Chart axes, tooltip values |

### Responsive Type Scale

Values in the YAML frontmatter are **desktop defaults**. AI agents must scale them down on smaller breakpoints — otherwise headings break the viewport on mobile (a 96px hero on a 375px screen wraps mid-letter).

| Token | Mobile (≤599px) | Tablet (600–1023px) | Desktop (1024–1439px) | Wide (1440px+) |
|---|---|---|---|---|
| `display-hero` | 56px | 72px | 96px | 96px |
| `data-stat` | 48px | 56px | 64px | 72px |
| `title-h1` | 36px | 48px | 56px | 64px |
| `title-h2` | 28px | 32px | 36px | 40px |
| `title-h3` | 22px | 24px | 26px | 28px |
| `title-feature` | 18px | 20px | 20px | 22px |
| `body-lg` | 17px | 18px | 19px | 20px |
| `body-md` | 16px | 16px | 16px | 16px |
| `body-sm` | 14px | 14px | 14px | 14px |
| `caption` | 12px | 12px | 13px | 13px |
| `label-bold` | 11px | 11px | 12px | 12px |
| `data-label` | 12px | 12px | 13px | 13px |

**Rules:**
- Body text (`body-md`/`body-sm`) does not scale — readability is the same on every device.
- Letter-spacing scales with size: at mobile (≤599px), reduce display/title `letter-spacing` toward 0 (e.g. `display-hero` -2px → -1.2px on mobile) — tight tracking looks awful on small text.
- Line-height stays as defined in YAML across all breakpoints.
- For arbitrary widths between breakpoints, use `clamp()` rather than fixed steps: `font-size: clamp(56px, 8vw, 96px)` for hero.

### Principles
- **Phenomena — strictly for headings and large numbers.** Never use Phenomena for long paragraphs; its wide footprint ruins readability.
- **Proxima Nova — for anything longer than 5 words.** All UI, descriptions, lists, tables, data.
- **Tabular numerals are mandatory** for all numbers in tables, dashboards, and charts, ensuring digits align vertically.
- **Uppercase with +1px letter-spacing** — strictly for Overlines/Labels. Do not use uppercase for H1–H3 headings.
- **Weight contrast matters:** use 900 Black for maximum emphasis in large numbers; use 400 Regular for body text.
- **Use Italics sparingly:** only for quotes, "note:" callouts, or external source titles.

### Number & Currency Formatting (UA locale)

All numbers must be formatted according to Ukrainian standards. This is **mandatory** — English-speaking agents (Stitch, Lovable, v0) default to using commas for thousands, and without this rule, "14 832 голоси" turns into "14,832".

- **Thousands separator**: non-breaking space (` `). `14 832`, `127 456`, `1 412`. NOT `14,832`, NOT `14.832`.
- **Decimal separator**: comma. `3,7%`, `5,2 млн`. NOT `3.7%`.
- **Currency**: `₴` before the number with a non-breaking space — `₴5,2 млн`. For exact sums — as a postfix: `62 437 ₴`.
- **Abbreviations**: `тис.`, `млн`, `млрд` with a non-breaking space. `127 тис.`, `5,2 млн`.
- **Percentages**: tight, no space. `47,3%`.
- **Year ranges**: en-dash without spaces. `2016–2026`, NOT `2016-2026`, NOT `2016 - 2026`.
- **Years**: full digits. `2019`, NOT `'19`.
- `tabular-nums` — mandatory on all UI, table, and chart numbers (see Hierarchy above).

---

## 4. Component Stylings

### Buttons

**Primary (Solid Purple)**
- Background: `#654EA3` (Primary-500)
- Text: `#FDFDFD`
- Padding: 12px 24px
- Radius: 8px
- Hover: Background `#4E3C84` (Primary-900)
- Disabled: Background `#9C8BCC` (Primary-200), cursor not-allowed
- Font: Proxima Nova 16px 600

**Secondary (Outline)**
- Background: transparent
- Text: `#654EA3`
- Border: 1.5px solid `#654EA3`
- Padding: 12px 24px (-1.5px for border)
- Radius: 8px
- Hover: Background `#EEEAF7` (Primary-100)

**Ghost / Tertiary**
- Background: transparent
- Text: `#3F4049` (neutral-700)
- Hover: Background `#EFEFF1` (neutral-100)
- Use for navigation, toolbars, link-buttons

**Accent (Yellow CTA)**
- Background: `#FFEC08` (Secondary-500)
- Text: `#1A1A1A`
- Border: 1px solid `#1A1A1A` *(mandatory for contrast on light surfaces)*
- Padding: 12px 24px
- Radius: 8px
- Hover: Background `#E6D307` (Secondary-700)
- Use case: exceptional CTAs (e.g., "Explore 10 years of PB")

### Cards & Containers

**Project Card (historical)**
- Background: `#FDFDFD`
- Border: 1px solid `#EFEFF1` (neutral-100)
- Radius: 12px
- Padding: 20px
- Shadow (hover): `0 4px 12px rgba(26, 26, 26, 0.06)`
- Contains: photo (top, radius 8px), category tag (chip), project title (Proxima Nova 20px 600), author (Proxima Nova 14px, neutral-500), stats (votes, budget — Phenomena 28px 700), status badge (winner / implemented)

**Stat-card (large number)**
- Background: `#F6F4FB` (Primary-50) OR `#FDFDFD` with 1px border
- Radius: 16px
- Padding: 24px
- Large number: Phenomena 56px 900, tabular-nums
- Label: Proxima Nova 14px 400, neutral-500, uppercase with +1px letter-spacing

### Tags / Chips (PB Categories)

- Size: height 24–28px, padding 4px 10px
- Radius: 999px (pill)
- Font: Proxima Nova 12px 600
- Background: tint of Primary or Neutral (15–20% opacity) + full color text of the same hue
  - Example (Primary-tinted): bg `rgba(101, 78, 163, 0.15)`, text `#4E3C84`
- The full "category → color" map lives in [design-data.md](./design-data.md) §4 — 11 canonical categories with stable colors across all years they appear.
- A small 14px icon can be added on the left.

### Historical Badges (Status)

- Size and geometry mirror chips (pill, 24–28px)
- Solid fill (not outline) for immediate recognition:
  - Winner of the year: bg `#FFEC08`, text `#1A1A1A`, optional star icon
  - Implemented: bg `#E8F3EC`, text `#1E6B39`, optional checkmark icon

### Progress Bar (Budget / Votes)

- Height: 8px (standard), 12px (hero on project page)
- Background: `#EFEFF1` (neutral-100)
- Fill: `#654EA3` (Primary-500) for votes; `#FFEC08` with a dark outline for "budget realization"
- Radius: 999px (pill)
- Optional: ticks (markers) at 25/50/75/100% using thin `#CACAD1` (neutral-300) lines

### Filter Elements (for analytical screens)

**Year Range Slider**
- Track: 4px, `#EFEFF1`, active-range fill `#654EA3`
- Handle: 16px circle, `#FDFDFD`, border 2px `#654EA3`, subtle shadow
- Labels: Proxima Nova 13px 500, tabular-nums

**Dropdown (category, year, etc.)**
- Background: `#FDFDFD`
- Border: 1px `#E2E2E6` (neutral-200)
- Radius: 8px
- Padding: 10px 14px
- Focus: border `#654EA3`, shadow `0 0 0 3px rgba(101, 78, 163, 0.15)`

**Checkbox / Toggle**
- Unchecked: border 1.5px `#CACAD1`, bg `#FDFDFD`
- Checked: bg `#654EA3`, checkmark `#FDFDFD`
- Toggle (e.g., "only winners"): track `#CACAD1`/`#654EA3`, thumb `#FDFDFD`

### Navigation
- Horizontal nav, bg `#FDFDFD`, bottom border 1px `#EFEFF1`
- Links: Proxima Nova 16px 500, `#3F4049`, hover `#654EA3`
- Active state: 2px bottom underline `#654EA3`, text `#1A1A1A`
- Logo: 28–32px height, aligned left

---

## 5. Layout Principles

### Spacing System (8px base)
`4px, 8px, 12px, 16px, 20px, 24px, 32px, 40px, 48px, 64px, 80px, 96px`

### Grid & Container
- Max container width: **1280px**
- Side padding: 24px (mobile), 40px (tablet), 64px (desktop)
- Columns: 4 (mobile), 8 (tablet), 12 (desktop)
- Gutter: 16px (mobile), 24px (tablet+)

### Whitespace Philosophy
- **Municipal trust = room to breathe.** Sections are separated by `{spacing.section}` (96px) of vertical space on desktop (`{spacing.xxl}` on mobile). Allow the page to return to `{colors.canvas}` between every two sections so each block reads as deliberate.
- **Cards breathe:** internal card padding is `{spacing.lg}` (24px), spacing between cards in grids is `{spacing.lg}`.
- **Data needs air:** charts and tables maintain 24–32px padding from container edges.

### Section Surface Pattern (Color Blocks)

Long-form pages ("10 Years of PB", project deep-dives) need a vertical rhythm. The system uses surface alternation, not decoration, to break sections.

**Allowed surfaces:**
- `{colors.canvas}` (#FDFDFD) — default; the page returns here between every two color blocks.
- `{colors.primary-50}` (#F6F4FB) — calm purple block for stat sections, narrative recap, "the big picture" framings.
- `{colors.primary-100}` (#EEEAF7) — slightly stronger purple for emphasis blocks (e.g., "Top winner of the decade").
- `{colors.secondary-100}` (#FFF9B3) — yellow block, used **at most once per page**, reserved for the single most important moment (a hero stat, a CTA strip).

**Rules:**
- **One color block per visible viewport.** If two color blocks would appear simultaneously on a 1080px-tall screen, insert a canvas section between them.
- **Canvas always returns.** Never chain two non-canvas sections in a row.
- **Color blocks span full bleed** on mobile (no side margins, no rounded corners). On desktop they render as `rounded-xl` containers with `{spacing.section}` (96px) interior padding (component: `section-hero`).
- **Type stays the same.** Surface change does not allow new fonts or new color tokens — only the background varies.
- **Yellow blocks demand restraint.** A yellow section forces a dark border (`1px solid {colors.ink}`) on any contained `button-primary` to maintain contrast.

> This pattern is the system's pacing tool. A 6-section page should read roughly as: canvas → primary-50 → canvas → primary-100 → canvas → secondary-100 (closing CTA). Never: primary-50 → primary-100 → primary-50 in a row.

### Border Radius Scale
- `4px` — tiny elements (internal chip labels, progress ticks)
- `8px` — buttons, inputs, small cards
- `12px` — project cards, standard blocks
- `16px` — large stat-cards, modals
- `24px` — large hero sections, featured cards
- `999px` (pill) — chips, badges, thin tag-buttons

### Image & Photo Geometry

Real PB project photos vary wildly in quality — the system masks this with a uniform geometric frame.

- **Aspect ratio**: 3:2 in cards, 16:9 in heroes, 1:1 only for social media tiles. Never freeform.
- **Corner radius**: `{rounded.sm}` (8px) when nested inside a `card-project` (12px outer); `{rounded.md}` (12px) for stand-alone hero images; `{rounded.lg}` (16px) for full-bleed hero photos in `section-hero`.
- **No drop shadows on photos.** Photos sit flat on the card surface.
- **No rotation, no parallax.** Photos are static rectangles — this is municipal reportage, not editorial design.
- **No avatars.** Authors are referenced by name + neighborhood (Proxima Nova 14px, neutral-500), never by photo, to protect resident privacy.
- **Lazy-loading mandatory** for any image below the first viewport — `loading="lazy"` on every `<img>` outside the hero.
- **Object-fit: cover** with `object-position: center` is the default. Manual cropping is allowed only when a face or critical detail anchors the frame.
- **Placeholder when photo is missing**: `{colors.primary-50}` background with a 32px Lucide camera-off icon in `{colors.neutral-400}`, centered. Never use stock photography as a fallback.
- **Alt text mandatory** — describe the project subject ("courtyard with new playground on Halytska St."), not the photo composition.

---

## 6. Depth & Elevation

| Level | Shadow | Usage |
|---|---|---|
| 0 (Flat) | none | Base surfaces, text, backgrounds |
| 1 (Subtle) | `0 1px 2px rgba(26, 26, 26, 0.04)` | Static cards on a light background |
| 2 (Raised) | `0 4px 12px rgba(26, 26, 26, 0.06)` | Card hovers, elevated elements |
| 3 (Overlay) | `0 12px 32px rgba(26, 26, 26, 0.10)` | Dropdowns, tooltips, popovers |
| 4 (Modal) | `0 24px 64px rgba(26, 26, 26, 0.14)` | Modals, lightboxes |

**Philosophy:** Shadows are always neutral gray (based on `#1A1A1A` with opacity), never purple. Offsets strictly run downwards (y+), with zero lateral shift. This establishes a calm, timeless hierarchy free from "digital noise."

---

## 7. Do's and Don'ts

### Do
- Use Phenomena exclusively for headings and large numbers — that's where its magic lies.
- Use Proxima Nova for all UI components, body text, data, and captions.
- Apply `tabular-nums` to all digits in tables and dashboards.
- Treat yellow `#FFEC08` as an **accent**, not a background. Use it to mark winners, highlights, and exceptionally critical CTAs.
- In charts involving yellow, always outline it with a dark `#1A1A1A` 1–1.5px stroke.
- Core data-viz relies on Primary shades + yellow as an accent. The categorical palette for multi-segment charts (donuts, stacked bars, streamgraphs) lives in [design-data.md](./design-data.md) §4.
- For heatmaps / choropleths, rely on a single-color sequential gradation — naturally, Primary-50 → Primary-900.
- Give sections 80–96px of vertical breathing room.
- Stick to 8px radii for buttons, 12px for cards, and pill shapes for chips/badges.
- Verify text/background contrast against WCAG AA standards (min. 4.5:1 for body text, 3:1 for large text).

### Don't
- Do not use Phenomena for body text — readability will collapse.
- Do not put purple text on a yellow background, or white on yellow — both fail AA contrast.
- Do not use large yellow fills — it causes eye fatigue and creates an unintended "warning" vibe.
- Do not use neon or gradient colors — the brand is restrained.
- Do not roughly round large numbers in official stats — "14 832 голоси", not "~15 тис.".
- Do not confuse roles: "live" status chips like "Voting in progress" are **forbidden**. The site is a **historical analytics** platform, not an active PB voting cycle.
- Do not use lateral shadows (x-offset) — stick strictly to vertical drops.
- Do not design dark-mode variants — municipal transparency is rooted in a light interface; dark mode is **out of scope** for this system.
- Do not attempt inline text editing with Phenomena 300 or thinner — its Thin/Light weights are strictly for display applications at large sizes (48px+).

---

## 8. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|---|---|---|
| Mobile | 360–599px | 1 column stack, hero number 48px, padding 24px |
| Tablet | 600–1023px | 2 columns, hero number 64px, padding 40px |
| Desktop | 1024–1439px | 3–4 columns, hero number 80px, padding 64px |
| Wide | 1440px+ | Max container 1280px, center aligned |

### Touch Targets

Mobile-first means real fingers on real phones in real Marshrutkas. Every interactive element must satisfy these minimums.

| Element | Mobile (touch) | Desktop (mouse) |
|---|---|---|
| Pill buttons (primary, secondary, accent) | min height **44px** | 40px acceptable |
| Form inputs (dropdown, text, select) | min height **48px** | 40px acceptable |
| Checkbox / toggle hit area | **44×44px** (visual can be 20px, hit area larger via padding) | 24×24 acceptable |
| Year-range slider handle | **24px diameter** (visible) with **44×44px hit area** | 16px diameter, 32×32 hit area |
| Icon-only button (e.g., filter chip close, map zoom) | **44×44px** | 32×32px |
| Inline link (within paragraph) | line-height ≥ 1.55 + 8px vertical padding on tap | n/a |
| Map markers | **32×32px** minimum tap target (visual icon can be 20px) | 20×20px |

**Spacing between adjacent targets**: ≥ 8px gutter to prevent thumb mis-taps.
**Bottom-sheet filter handles**: full-width tap zones, ≥ 56px tall.

> Test at 375px width with a fingertip overlay (44px circle) before declaring any screen mobile-ready.

### Collapsing Strategy
- Hero display: 96px → 72px → 56px → 48px
- H1: 64px → 48px → 36px
- Section H2: 40px → 32px → 28px
- Column Grid: 12 → 8 → 4
- Map: Collapses filters into a bottom-sheet on mobile.
- 10-year data tables: Convert into horizontal scroll or stacked-cards on mobile.
- Navigation: Collapses into a burger menu on mobile.

### Mobile-first Priority
The "10 Years of PB" site and all infographics are **designed for mobile first** — because the vast majority of citizens consume municipal content via phones. Maps, filters, and statistics must remain perfectly usable on a 375px screen.

---

## 9. Iconography

### Sets
- **Primary**: [Lucide](https://lucide.dev/) — thin, stroke-based, 1.5px weight, rounded corners.
- **Fallback for filled icons**: [Phosphor Icons](https://phosphoricons.com/) — Regular/Fill variants.

### Rules
- Stroke weight: **1.5px** (standard), **2px** (for display sizes 32px+).
- Sizes: 16px (inline), 20px (buttons), 24px (column nav), 32px+ (hero).
- Color: `currentColor` — icons always inherit the color of the adjacent text.
- Rounded corners only, absolutely no sharp edges.

### Map & Category Icons

> The fixed "category → icon → color" table, alongside map specifics (project markers, clusters, winner stars), lives in [design-data.md](./design-data.md) §4 and §7. We only dictate general icon rules here (weight, size, `currentColor`) because the category set shifts year to year.

---

## 10. Voice & Tone (Editorial Style)

### Principles
- **Formal-yet-warm.** Always use the polite "Ви" (You). Never use the informal "Ти", not even on social media.
- **Active verbs, concrete results.** "Residents of Pasichna chose 14 projects" is better than "Voting was conducted." "12 courtyards renovated for 5.2M UAH" is better than "A series of improvement measures were executed."
- **No bureaucratic jargon.** Words like "вищезазначений" (aforementioned), "в рамках" (within the framework), "з метою" (with the aim of), or "шляхом" (by means of) are banned. Write simply.
- **Don't hide hero numbers.** If 127 thousand people participated over 10 years, that should be a massive display number, not buried in a paragraph.
- **Focus on people and results, not processes.** "Maria from the Bus Station area submitted the city's first bike station project" beats "Applications were submitted via the electronic cabinet."

### Headings
- Short, specific, featuring a number or a name whenever possible.
- ✓ "10 years, 1,412 projects, 8 legendary winners"
- ✗ "Overview of participatory budgeting implementation over a ten-year period"

### Chart Captions
- Explain the **insight**, don't just describe the chart: "Educational projects swept 5 out of 6 top spots in 2018" is superior to "Distribution of winning projects by category in 2018."

### Social Media
- Brief facts with an emotional hook: "In 2019, a courtyard on Halytska gathered more votes than any educational project across all 10 years. See how it happened in the insights ↓"
- Always offer a clear call to action: a link to the site with a pre-applied filter.

---

## 11. Agent Prompt Guide

### Quick Reference
```
BRAND CORE
  Primary (purple):    #654EA3
  Secondary (yellow):  #FFEC08
  Background:          #FDFDFD
  Text:                #1A1A1A

FONTS
  Display/Headings:    Phenomena (900 Black for hero, 700 for H1-H2, 400 for H3)
  Body/UI:             Proxima Nova (600 for titles, 400 for body)
  All numbers:         tabular-nums

DATA-VIZ (in core)
  Primary shades + yellow as accent
  Sequential for heatmap/choropleth: Primary-50 → Primary-900
  Yellow in charts ALWAYS with dark outline #1A1A1A 1-1.5px
  Data-viz palette goes in a fixed order. Yellow in charts - ALWAYS with a dark outline.
  Extended categorical palette + map tokens → design-data.md (§4, §7)

RADII: 4, 8, 12, 16, 24, 999 (pill)
SPACING: 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96
```

### Example Prompts

**"10 Years of PB" Hero Card:**
> Create a hero card for "10 років Бюджету участі Івано-Франківська". Large display number "10" in Phenomena Black 96px, color #654EA3, tabular-nums. Subtitle "років змін" in Proxima Nova 20px 400, color #1A1A1A. Background #FDFDFD, padding 48px, border-radius 24px, subtle shadow level 2. Below: three stat chips (1 412 проєктів / 127К учасників / ₴62 млн) in Phenomena 28px 700.

**Historical Project Card:**
> Build a project card: photo on top (radius 12px, aspect-ratio 3:2), then a pill-tag «Освіта» (bg rgba(101, 78, 163, 0.15), text #4E3C84, font Proxima Nova 12px 600). Title in Proxima Nova 20px 600, color #1A1A1A. Below: author name in Proxima Nova 14px 400, color #71737E. Stats row: "2 847 голосів" (Phenomena 24px 700) and "₴1,2 млн" (Phenomena 24px 700). Bottom: yellow badge "Переможець 2019" bg #FFEC08, text #1A1A1A, pill, Proxima Nova 12px 600.

**Social Media Infographic (1:1):**
> Create a 1080×1080 infographic. Background #FDFDFD with subtle top-right corner detail in Primary-50 #F6F4FB. Big display number in center: "14 832" in Phenomena Black 180px, color #654EA3, tabular-nums. Below in Proxima Nova 28px 600: "голоси за двір на Галицькій, 2019". Footer: small yellow badge "переможець року" bg #FFEC08, dark border 1px. Logo bottom-left.

> **Examples for maps, heatmaps, and other analytical artifacts** — see [design-data.md](./design-data.md) §7 (map tokens) and §8 (visualization patterns). We only keep core promo/card examples here, which any consumer of the core system would need.

### Iteration Guide
1. Always start with the brand core (purple + yellow + graphite on off-white).
2. Phenomena — strictly for headings and huge numbers. Everything else is Proxima Nova.
3. `tabular-nums` — on all digits.
4. Data-viz palette runs in a fixed order. Yellow in charts ALWAYS gets a dark outline.
5. Shadows are strictly vertical, soft, and neutral-gray.
6. Absolutely no "live" status indicators — rely only on historical badges (Winner of the Year, Participant, Implemented, Not Implemented).
7. Mobile-first. Stress-test the design at 375px before scaling wider.

### Known Gaps

This system is intentionally minimal. The following areas are **out of scope** for the core `design.md`. If you need them, do not invent — defer or escalate.

**Provided by [design-data.md](./design-data.md)** (the data layer):
- Canonical categorical palette (11 categories, stable colors, Lucide icons) — §4
- Year-by-year category mapping with renamings/splits/merges — §2 and §3
- 6 real project statuses (Implemented, In Progress, Participated, Rejected, Permanently Rejected, Impossible to Implement) — §6. Only the 2 promotional badges (Winner, Implemented) live in core.
- Map tokens: project markers, clusters, winner stars, choropleth scale — §7
- Project size axis (Малий / Середній / Великий / Маленький) — §5

**Out of scope entirely** (do not design or generate):
- Dark mode — municipal transparency is rooted in a light interface
- Live voting states ("Voting in progress", "Submission open") — this is a historical analytics platform, not an active PB cycle
- Form error states & validation copy — current PB site does not collect submissions through this design system
- Admin / CMS UI — the system covers public-facing artifacts only
- Email templates, push notifications — different medium, different rules
- Multi-language switcher beyond UA/EN — system is bilingual, not multilingual

**If an agent encounters a gap**: leave a `<!-- TODO: design-data.md needs X -->` HTML comment in the generated artifact, never fabricate a token or color outside the documented set.

---

## 12. Motion & Interaction

Motion in this system serves **moments of emphasis** — the arrival of hero numbers, chart entries, and hover states. The baseline state of the UI is stillness. This section sets rigid boundaries to prevent AI agents from hallucinating arbitrary animations and ensures our signature "number count-up on scroll" is executed consistently.

### Core Rules
- **`prefers-reduced-motion` is non-negotiable.** All animations must feature a CSS fallback revealing the final state instantly.
- **Stillness is default.** Only animate during key moments: first appearance in the viewport, hover/focus, and state transitions (dropdowns, tabs, modals).
- **Motion serves the data.** No decorative floating or bouncing — animate only to draw focus to a number or a state change.

### Durations & Easing

| Context | Duration | Easing |
|---|---|---|
| Hover / focus (color, shadow) | 150ms | `ease-out` |
| Tooltip, dropdown, tab switch | 200–250ms | `cubic-bezier(0.22, 1, 0.36, 1)` |
| Card reveal on scroll | 400–500ms | `cubic-bezier(0.22, 1, 0.36, 1)` |
| **Count-up for hero numbers** | 900–1200ms | `cubic-bezier(0.25, 0.1, 0.25, 1)` |
| Chart entry (bars grow, lines draw) | 800–1000ms | `cubic-bezier(0.22, 1, 0.36, 1)` |
| Modal open | 200–250ms (fade + scale) | `ease-out` |

### Count-up for Hero Numbers (Signature Animation)

This is the system's signature flair. When a hero number (Phenomena Black 48px+) enters the viewport for the first time, it counts up from `0` to the target value.

- **Trigger**: `IntersectionObserver`, threshold 0.4 (when 40% of the element is visible).
- **Duration**: 900–1200ms (larger numbers skew closer to 1200ms).
- **Easing**: Natural deceleration — fast start, braking towards the end.
- **Intermediate formatting**: Interstitial numbers must retain the non-breaking space formatting (`8 421` → `14 832`), not unformatted "14832".
- **Minimum threshold**: Do not apply to numbers `< 100` — it looks erratic.
- **Adjacent stat cards**: Apply an 80–120ms stagger between cards; they should not count up in perfect unison.

### Chart Entry Animations

- **Bar**: Bars grow from the bottom to their final height, 800ms, with a 50ms stagger between bars.
- **Line / Area**: Lines draw from left to right using `stroke-dashoffset`, 1000ms. Area fills fade in *after* the line finishes drawing.
- **Donut / Pie**: Segments draw clockwise starting from 12 o'clock, 800ms total.
- **Heatmap**: Cells fade in diagonally from top-left to bottom-right, with a 15ms stagger per cell.
- **Trigger**: Exclusively upon entering the viewport, never merely on page load.

### Interactive States

- **Card hover**: `translateY(-2px)` + elevate shadow from level 1 to level 2, 150ms.
- **Chart bar/dot hover**: Fill becomes 10% lighter, tooltip fades in over 150ms.
- **Focus-ring**: `outline: 2px solid #654EA3; outline-offset: 2px` — **zero animation** (instant switch for accessibility).
- **Button click**: `scale(0.98)` for 100ms, then revert — providing light tactile feedback.

### Reduced Motion

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

Under this preference: count-ups instantly display the **final number** with zero scrolling, and charts render in their final state immediately.

### Don't

- Do not animate background colors (e.g., `white → purple` for a "swoosh" effect) — it's jarring.
- No parallax scrolling, no bounce or elastic easings — that's the tone of a gaming site, not a municipal tool.
- Do not let a count-up exceed 1.5s — the user has already moved on.
- Typewriter animations for headings (letters typing out one by one) are forbidden due to dyslexia concerns.
