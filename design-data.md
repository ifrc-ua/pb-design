---
version: 0.6.0
name: PB Ivano-Frankivsk Community — Real Data Reference
description: Real PB categories per year (2016–2026), canonical category palette and icons, project statuses, map tokens, author- and voter-gender axes. Companion to design.md.
parent: design.md
updated: 2026-05-25
status: beta
canonical-categories:
  # Education group (purple family — semantically grouped)
  education-general:
    label-en: "Education (umbrella)"
    label-uk: "Освіта"
    color: "#654EA3"             # = colors.primary-500 in design.md
    color-token: "primary-500"
    icon: graduation-cap
    active-years: [2019, 2020, 2021, 2023]
    notes: "Umbrella label used 2019–2023. In 2021, education projects ran under the size×theme matrix (Малий освітній / Великий освітній) — still rolls up to this canonical key. Replaced in 2024 by the 3-way split (school / preschool / extracurricular)."
  education-school:
    label-en: "School"
    label-uk: "Шкільні"
    color: "#4A2D87"
    icon: school
    active-years: [2024, 2025, 2026]
    size-variants-2026: [great, medium, tiny]
  education-preschool:
    label-en: "Preschool"
    label-uk: "Дошкільні"
    color: "#7B66B8"             # = colors.primary-300 in design.md
    color-token: "primary-300"
    icon: baby
    active-years: [2024, 2025, 2026]
    size-variants-2026: [small, great]
  education-extracurricular:
    label-en: "Extracurricular & vocational"
    label-uk: "Позашкільні, профтехосвіта"
    color: "#9E5FAB"
    icon: compass
    active-years: [2024, 2025, 2026]
  # Public-space improvement (blue family)
  improvement-general:
    label-en: "Public-space improvement"
    label-uk: "Благоустрій"
    color: "#2D6BAB"
    icon: hammer
    active-years: [2023, 2024, 2025, 2026]
    aliases: ["Інший благоустрій (2023)"]
  improvement-streets:
    label-en: "Small-streets improvement"
    label-uk: "Благоустрій малих вулиць"
    color: "#1A4F82"
    icon: route
    active-years: [2020, 2021, 2023, 2024, 2025, 2026]
    aliases: ["Вулиці / Ремонт малих вулиць (2020)", "Ремонт малих вулиць (2021)"]
  # Heritage (warm)
  heritage:
    label-en: "Cultural / architectural heritage"
    label-uk: "Архітектурна спадщина"
    color: "#A0571F"
    icon: landmark
    active-years: [2021, 2026]
    aliases: ["Об'єкти культурної спадщини (2021)"]
  # Green / environmental
  greenery:
    label-en: "Greenery & urban-environment"
    label-uk: "Зелені проєкти"
    color: "#3D7C3F"
    icon: tree-deciduous
    active-years: [2023, 2025, 2026]
  # Defense (graphite — solemn)
  afu-support:
    label-en: "AFU (Armed Forces) support"
    label-uk: "Допомога ЗСУ"
    color: "#3F4049"             # = colors.neutral-700 in design.md
    color-token: "neutral-700"
    icon: shield
    active-years: [2025, 2026]
  # Accessibility (teal — international convention)
  accessibility:
    label-en: "Accessibility"
    label-uk: "Доступність"
    color: "#0E7C8C"
    icon: accessibility
    active-years: [2025, 2026]
  # Catch-all
  other:
    label-en: "Other"
    label-uk: "Інші проєкти"
    color: "#71737E"             # = colors.neutral-500 in design.md
    color-token: "neutral-500"
    icon: package
    active-years: [2019, 2020, 2021, 2023, 2024, 2025, 2026]
    aliases: ["Інші (2019)", "Інше (2020, 2023)", "Малий/Великий інше (2021)"]
project-sizes:
  small:
    label-en: "Small"
    label-uk: "Малий"
    active-years: [2016, 2017, 2018, 2019, 2020, 2021]
  medium:
    label-en: "Medium"
    label-uk: "Середній"
    active-years: [2026]
    note: "First introduced in 2026 within the school sub-category."
  great:
    label-en: "Great"
    label-uk: "Великий"
    active-years: [2018, 2019, 2020, 2021, 2026]
  tiny:
    label-en: "Tiny"
    label-uk: "Маленький"
    active-years: [2026]
    note: "First introduced in 2026 within the school sub-category."
project-statuses:
  realized:
    label-en: "Implemented"
    label-uk: "Реалізований"
    color: "#2F8F4E"             # = colors.success
    bg-tint: "#E8F3EC"
    text: "#1E6B39"
    icon: circle-check
    finality: terminal-positive
  in-progress:
    label-en: "In progress"
    label-uk: "На реалізації"
    color: "#2563EB"             # = colors.info
    bg-tint: "#E8EEFD"
    text: "#1E4FBF"
    icon: loader-circle
    finality: active
  participated:
    label-en: "Participated"
    label-uk: "Брав участь"
    color: "#71737E"             # = colors.neutral-500
    bg-tint: "#EFEFF1"           # = colors.neutral-100
    text: "#3F4049"              # = colors.neutral-700
    icon: vote
    finality: neutral
  rejected:
    label-en: "Rejected"
    label-uk: "Відхилений"
    color: "#D97706"             # = colors.warning
    bg-tint: "#FEF3E2"
    text: "#A05905"
    icon: circle-x
    finality: recoverable
  rejected-permanent:
    label-en: "Permanently rejected"
    label-uk: "Відхилений остаточно"
    color: "#DC2626"             # = colors.error
    bg-tint: "#FCE9E9"
    text: "#A01818"
    icon: ban
    finality: terminal-negative
  impossible:
    label-en: "Impossible to implement"
    label-uk: "Неможливо реалізувати"
    color: "#3F4049"             # = colors.neutral-700
    bg-tint: "#E2E2E6"           # = colors.neutral-200
    text: "#1A1A1A"
    icon: triangle-alert
    finality: terminal-factual
  removed:
    label-en: "Removed"
    label-uk: "Видалений"
    color: "#9FA0A9"             # = colors.neutral-400
    bg-tint: "#F7F7F8"           # = colors.neutral-50
    text: "#71737E"              # = colors.neutral-500
    icon: trash-2
    finality: terminal-administrative
    note: "Administrative removal by moderator. Distinct from `rejected` (failed review on merits) and `impossible` (factual unfeasibility)."
author-gender:
  # Orthogonal axis: author gender. Two purples for clear light-vs-deep contrast, neutral grey for unknown.
  # Display order: female → male → unknown (light to dark; female is historical majority).
  female:
    label-en: "Women"
    label-uk: "Жінки"
    color: "#9C8BCC"             # = colors.primary-200 in design.md
    color-token: "primary-200"
    available-years: [2016, 2017, 2018, 2019, 2020, 2021, 2023, 2024, 2025, 2026]
    note: "Source: column `authorSex`."
  male:
    label-en: "Men"
    label-uk: "Чоловіки"
    color: "#4E3C84"             # = colors.primary-900 in design.md
    color-token: "primary-900"
    available-years: [2016, 2017, 2018, 2019, 2020, 2021, 2023, 2024, 2025, 2026]
  unknown:
    label-en: "Unknown"
    label-uk: "Невідомо"
    color: "#CACAD1"             # = colors.neutral-300 in design.md
    color-token: "neutral-300"
    available-years: [2016]
    note: "Only 2016 has `n/a` entries (29 of 80 projects). 2017+ cycles have no n/a authors."
voter-gender:
  # Orthogonal axis: gender of citizens who voted (distinct from author-gender above).
  # Shares the author-gender palette intentionally — visualizations comparing the two axes
  # (e.g. female authors vs female voters) read symmetrically by color.
  # Legends MUST disambiguate "автори" vs "виборці", since the colors are identical across the two axes.
  # Source: voter registry. Available 2021–2026 (no voter-gender data before 2021; 2022 absent per `years-without-pb`).
  female:
    label-en: "Women voters"
    label-uk: "Жінки-виборчині"
    color: "#9C8BCC"             # = colors.primary-200 in design.md (same as author-gender.female)
    color-token: "primary-200"
    available-years: [2021, 2023, 2024, 2025, 2026]
  male:
    label-en: "Men voters"
    label-uk: "Чоловіки-виборці"
    color: "#4E3C84"             # = colors.primary-900 in design.md (same as author-gender.male)
    color-token: "primary-900"
    available-years: [2021, 2023, 2024, 2025, 2026]
  # No `unknown` key today — voter dataset has no n/a entries. If a future export introduces
  # them, add `voter-gender.unknown` with `colors.neutral-300` in a MINOR bump (same as author).
map-tokens:
  marker:
    type: map-pin
    size: 24
    stroke: "2px solid #FFFFFF"
    fill: "{canonical-categories.<key>.color}"
  cluster:
    shape: circle
    sizes-px: [28, 40, 56]
    bg: "{colors.primary-100}"   # #EEEAF7
    border: "2px solid {colors.primary-500}"  # #654EA3
    label: "Phenomena 14–16px 700, tabular-nums"
  winner-star:
    size: 10
    fill: "{colors.secondary-500}"  # #FFEC08
    stroke: "1px solid {colors.ink}"  # #1A1A1A
    placement: "top-right of marker"
  choropleth-sequential:
    stops:
      - "#F6F4FB"                 # primary-50
      - "#EEEAF7"                 # primary-100
      - "#9C8BCC"                 # primary-200
      - "#7B66B8"                 # primary-300
      - "#4E3C84"                 # primary-900
    polygon-border: "1.5px solid #CACAD1"  # neutral-300
years-without-pb: [2022]
districts-color-policy: rules-by-scenario
districts:
  ivano-frankivsk:
    label-uk: "Івано-Франківськ"
    label-en: "Ivano-Frankivsk"
    type: city
  vovchynets:
    label-uk: "Вовчинець"
    label-en: "Vovchynets"
    type: village
  krykhivtsi:
    label-uk: "Крихівці"
    label-en: "Krykhivtsi"
    type: village
  uhornyky:
    label-uk: "Угорники"
    label-en: "Uhornyky"
    type: village
  khryplyn:
    label-uk: "Хриплин"
    label-en: "Khryplyn"
    type: village
  mykytyntsi:
    label-uk: "Микитинці"
    label-en: "Mykytyntsi"
    type: village
  chukalivka:
    label-uk: "Чукалівка"
    label-en: "Chukalivka"
    type: village
  cherniiv:
    label-uk: "Черніїв"
    label-en: "Cherniiv"
    type: village
  pidpechery:
    label-uk: "Підпечери"
    label-en: "Pidpechery"
    type: village
  pidluzhzhia:
    label-uk: "Підлужжя"
    label-en: "Pidluzhzhia"
    type: village
  berezivka:
    label-uk: "Березівка"
    label-en: "Berezivka"
    type: village
  bratkivtsi:
    label-uk: "Братківці"
    label-en: "Bratkivtsi"
    type: village
  dobrovliany:
    label-uk: "Добровляни"
    label-en: "Dobrovliany"
    type: village
  drahomyrchany:
    label-uk: "Драгомирчани"
    label-en: "Drahomyrchany"
    type: village
  kaminne:
    label-uk: "Камінне"
    label-en: "Kaminne"
    type: village
  kolodiivka:
    label-uk: "Колодіївка"
    label-en: "Kolodiivka"
    type: village
  radcha:
    label-uk: "Радча"
    label-en: "Radcha"
    type: village
  tysmenychany:
    label-uk: "Тисменичани"
    label-en: "Tysmenychany"
    type: village
  uzyn:
    label-uk: "Узин"
    label-en: "Uzyn"
    type: village
---

> **EN — primary artifact for AI agents.** Read in Ukrainian: [design-data.ua.md](./design-data.ua.md).

# PB Ivano-Frankivsk — Real Data Reference

This file extends [design.md](./design.md) with the **real, year-by-year structure of Participatory Budgeting in Ivano-Frankivsk (2016–2026)**: which categories existed in each year, their canonical colors and icons, real project statuses, and map tokens.

The core `design.md` deliberately stays minimal. This file is the **data layer**: agents pull category colors, icons, and statuses from here when generating analytical artifacts (heatmaps, donuts, choropleths, status badges).

---

## TL;DR

- **10 cycles across 2016–2026** (PB was not held in 2022).
- **Categorization changed every year** — 2016–2017 had no thematic split (size only); 2024 split education into 3 sub-categories; 2025 added Defense (ЗСУ) and Accessibility; 2026 introduced size sub-tiers within education.
- **Four orthogonal axes**: thematic category (color + icon), project size (Малий / Середній / Великий / Маленький — badge modifier), author gender, and voter gender. The two gender axes share one two-purple palette — legends must disambiguate «автори» vs «виборці».
- **11 canonical categories** unify all year-specific labels into a stable color + icon set.
- **7 real project statuses**, mapped to the design-system semantic palette (success / info / warning / error / neutral / graphite / muted-grey).
- **Map tokens** (markers, clusters, winner stars, choropleth scale) live here, not in `design.md`.

---

## 1. About this file

### Purpose
- Source of truth for **what existed in each year** of PB Ivano-Frankivsk.
- Single canonical mapping `category → color → icon`, stable across years even when the city renamed/split/merged categories.
- Reference for AI agents generating multi-year visualizations: heatmaps, streamgraphs, donuts, comparative charts, choropleth maps.

### Relationship to `design.md`
- `design.md` defines the **system** (colors, typography, components, rules). It does not name real-world PB categories.
- `design-data.md` defines the **data** (real categories, real statuses). Every color it introduces is either reused from `design.md` (via `color-token` reference) or a category-specific extension that complies with the WCAG AA contrast rules in `design.md` §2.

### When to use this file
- Generating any multi-category chart with 5+ segments — pull from `canonical-categories`.
- Generating a status badge for analytical dashboards — use the 7 statuses below, not the 2 promotional badges in `design.md` §2.
- Generating a city map with project markers — use `map-tokens` here.
- Cross-year comparison — consult §3 «Year-over-year notes» for renamings.

### Versioning
- Currently in `0.x` (beta) — the canonical palette and icons are proposals subject to municipal review.
- Same semver policy as `design.md` (see [CLAUDE.md](./CLAUDE.md)). MAJOR if any canonical color or icon changes; MINOR for new categories, statuses, or expanded `active-years` for an existing category; PATCH for wording.
- Bump in lockstep with `design-data.ua.md`.

---

## 2. Categories per year (raw)

This is the historical truth, **not generalized**. Each year used its own labels. The canonical mapping in §3 unifies them.

### 2016
- **Sizes only:** Малий
- **Thematic categories:** none

### 2017
- **Sizes only:** Малий
- **Thematic categories:** none

### 2018
- **Sizes:** Малий, Великий
- **Thematic categories:** none

### 2019
- **Sizes:** Малий, Великий
- **Geographic scope:** Загальноміський, Локальний
- **Categories:** Освітні, Інші

### 2020
- **Sizes / funding tracks:** Малий, Великий, Вулиці (a separate track for small-street repair)
- **Categories:** Освіта, Інше (the latter covers «благоустрій, житлову політику, охорону здоров'я»)

### 2021
- **Funding tracks (size + theme combined):**
  - Малий освітній
  - Малий інше
  - Великий освітній
  - Великий інше
  - Ремонт малих вулиць
  - Об'єкти культурної спадщини
- **Underlying categories:** Малий, Великий, Благоустрій малих вулиць, Об'єкти культурної спадщини

### 2022
- **PB was not held.**

### 2023
- **Categories (thematic only — size split dropped):**
  - Освіта (Освітні)
  - Інший благоустрій
  - Благоустрій малих вулиць
  - Зелені проєкти

### 2024
- **Categories:**
  - Шкільні
  - Дошкільні
  - Позашкільні, профтехосвіта
  - Благоустрій
  - Благоустрій малих вулиць
  - Інші проєкти

### 2025
- **Categories:**
  - Допомога ЗСУ
  - Шкільні
  - Дошкільні
  - Позашкільні, профтехосвіта
  - Благоустрій
  - Благоустрій малих вулиць
  - Зелені проєкти *(category was available but received 0 submissions in 2025)*
  - Доступність
  - Інші проєкти

### 2026
- **Categories (with size sub-tiers inside education):**
  - Допомога ЗСУ
  - Зелені проєкти
  - Інші проєкти
  - Благоустрій малих вулиць
  - Благоустрій
  - Позашкільні, профтехосвіта
  - Доступність
  - Архітектурна спадщина
  - Дошкільні (малі)
  - Дошкільні (великі)
  - Шкільні (великі)
  - Шкільні (середні)
  - Шкільні (маленькі)

---

## 3. Year-over-year notes

How categories evolved — important for any chart that crosses year boundaries.

| Year | Change | What this means for visualizations |
|---|---|---|
| 2016 → 2018 | Sizes only, no thematic split | Pre-2019 years cannot be broken down by category. In a category-over-time chart, group them as «Без категоризації» or omit. |
| 2018 → 2019 | First thematic split: «Освітні» vs «Інші»; geographic scope added | Education becomes trackable from 2019 forward. |
| 2019 → 2020 | «Вулиці» appears as a funding track | Maps onto canonical `improvement-streets`. |
| 2020 → 2021 | Size × theme matrix: Малий/Великий × Освітній/Інше; heritage track added | When charting 2021, you may either flatten to thematic categories (Освіта / Інше / Малі вулиці / Спадщина) or keep the matrix — depending on the artifact. |
| 2022 | **PB not held** | **Omit 2022 entirely from chart axes.** The 10-point sequence is 2016, 2017, 2018, 2019, 2020, 2021, 2023, 2024, 2025, 2026 — no 2022 slot. A subtitle/caption note «у 2022 БУ не проводився» is sufficient context. Never allocate axis space to a year with no data. |
| 2022 → 2023 | Size split dropped entirely; pure thematic categories; «Зелені проєкти» appears | Major rebrand. From 2023 onward, charts can use the canonical 11-category palette directly. |
| 2023 → 2024 | Education splits 1 → 3 (Шкільні / Дошкільні / Позашкільні); «Інший благоустрій» renamed → «Благоустрій»; «Зелені проєкти» absent | Multi-year education charts: choose either roll-up (`education-general`) or fan-out (3 subcategories). |
| 2024 → 2025 | Adds «Допомога ЗСУ»; adds «Доступність»; «Зелені проєкти» returns | War-context categories. Color choices for ЗСУ are deliberately solemn graphite, not red/yellow/green. |
| 2025 → 2026 | «Об'єкти культурної спадщини» (last seen 2021) returns as «Архітектурна спадщина»; size sub-tiers reappear inside Шкільні/Дошкільні | Same canonical key `heritage` — just a label change. Size sub-tiers are visualized as badge modifiers, not separate colors (see §5). |

### Canonical mapping table

How year-specific labels reduce to canonical category keys:

| Raw label (year) | Canonical key |
|---|---|
| Освітні (2019), Малий/Великий освітній (2021), Освіта (2020, 2023) | `education-general` |
| Шкільні (2024+), Шкільні (великі/середні/маленькі) (2026) | `education-school` |
| Дошкільні (2024+), Дошкільні (малі/великі) (2026) | `education-preschool` |
| Позашкільні, профтехосвіта (2024+) | `education-extracurricular` |
| Благоустрій (2024+), Інший благоустрій (2023) | `improvement-general` |
| Інші (2019), Інше (2020), Малий/Великий інше (2021), Інші проєкти (2024+) | `other` |
| Благоустрій малих вулиць (2021, 2023+), Вулиці / Ремонт малих вулиць (2020), Ремонт малих вулиць (2021) | `improvement-streets` |
| Об'єкти культурної спадщини (2021), Архітектурна спадщина (2026) | `heritage` |
| Зелені проєкти (2023, 2025, 2026) | `greenery` |
| Допомога ЗСУ (2025, 2026) | `afu-support` |
| Доступність (2025, 2026) | `accessibility` |

---

## 4. Canonical categorical palette

Stable category → color → icon mapping. Each category keeps the same color and icon across all years it appears.

| Canonical key | Label (UA) | HEX | Source/role | Icon (Lucide) | Active years |
|---|---|---|---|---|---|
| `education-general` | Освіта | `#654EA3` | `colors.primary-500` from design.md | `graduation-cap` | 2019, 2020, 2021, 2023 |
| `education-school` | Шкільні | `#4A2D87` | extension (deeper purple) | `school` | 2024–2026 |
| `education-preschool` | Дошкільні | `#7B66B8` | `colors.primary-300` from design.md | `baby` | 2024–2026 |
| `education-extracurricular` | Позашкільні, профтехосвіта | `#9E5FAB` | extension (purple-mauve) | `compass` | 2024–2026 |
| `improvement-general` | Благоустрій | `#2D6BAB` | extension (civic blue) | `hammer` | 2023–2026 |
| `improvement-streets` | Благоустрій малих вулиць | `#1A4F82` | extension (deeper navy-blue) | `route` | 2020, 2021, 2023–2026 |
| `heritage` | Архітектурна спадщина | `#A0571F` | extension (terracotta/bronze) | `landmark` | 2021, 2026 |
| `greenery` | Зелені проєкти | `#3D7C3F` | extension (deep green) | `tree-deciduous` | 2023, 2025, 2026 |
| `afu-support` | Допомога ЗСУ | `#3F4049` | `colors.neutral-700` from design.md | `shield` | 2025, 2026 |
| `accessibility` | Доступність | `#0E7C8C` | extension (teal) | `accessibility` | 2025, 2026 |
| `other` | Інші проєкти | `#71737E` | `colors.neutral-500` from design.md | `package` | 2019, 2020, 2021, 2023–2026 |

### Contrast against `#FDFDFD` canvas

All extension colors satisfy WCAG 2.1 SC 1.4.11 (≥ 3:1 for non-text graphical objects — chart fills, icons, marker bodies). For text labels on a chart background, use the chip pattern from `design.md` §4 («Tags / Chips»): `bg = rgba(color, 0.15)` + dark text version, never raw color as a text background.

| HEX | Approx. contrast vs `#FDFDFD` | Suitable for |
|---|---|---|
| `#654EA3` | 7.0:1 ✓ AA | text + fills |
| `#4A2D87` | ~12:1 ✓ AAA | text + fills |
| `#7B66B8` | ~4.4:1 ✓ AA-large / fills | fills, large text |
| `#9E5FAB` | ~4.0:1 ✓ AA-large / fills | fills, large text |
| `#2D6BAB` | ~5.4:1 ✓ AA | text + fills |
| `#1A4F82` | ~8.4:1 ✓ AAA | text + fills |
| `#A0571F` | ~4.6:1 ✓ AA-large / fills | fills, large text |
| `#3D7C3F` | ~4.2:1 ✓ AA-large / fills | fills, large text |
| `#3F4049` | ~10:1 ✓ AAA | text + fills |
| `#0E7C8C` | ~4.0:1 ✓ AA-large / fills | fills, large text |
| `#71737E` | 4.7:1 ✓ AA (verified in design.md) | text + fills |

> Re-verify with WebAIM contrast-checker before any external publication.

### Fixed display order

When a chart has multiple categories visible at once (donut, stacked bar, streamgraph), use this order — left-to-right, top-to-bottom — so identical data reads identically across every artifact:

1. `education-general` → 2. `education-school` → 3. `education-preschool` → 4. `education-extracurricular` → 5. `improvement-general` → 6. `improvement-streets` → 7. `heritage` → 8. `greenery` → 9. `afu-support` → 10. `accessibility` → 11. `other`

For year-specific charts (e.g., 2025 donut), keep the relative order of those categories that exist, just collapse the rest.

---

## 5. Project sizes (orthogonal axis)

Size is **not** a category — it's a modifier. A 2026 «Шкільні (великі)» project is canonical key `education-school` with a `great` size badge.

| Size | UA label | Active years | Visual treatment |
|---|---|---|---|
| `small` | Малий | 2016–2021 | small badge before/after title; `bg = neutral-100`, `text = neutral-700`, pill 20px |
| `medium` | Середній | 2026 | same shape; `bg = primary-100`, `text = primary-900` |
| `great` | Великий | 2018–2021, 2026 | same shape; `bg = primary-200`, `text = primary-900` |
| `tiny` | Маленький | 2026 | same shape; `bg = neutral-50`, `text = neutral-700` |

Size badges are subordinate to category color — a project card always primarily reads as its category, with the size as a secondary chip.

---

## 6. Gender axes (orthogonal)

Two distinct gender axes live alongside category (§4) and size (§5):

- **§6.1 — Author gender** (`author-gender`): the person who submitted the project.
- **§6.2 — Voter gender** (`voter-gender`): the citizens who voted.

Both share the same female/male/unknown palette and the same restraint rules (no icons, no yellow, no main-card color). **The legend MUST disambiguate «автори» vs «виборці»**, since the colors are identical across the two axes. Use these axes only for dedicated gender-distribution visualizations (donuts, bar charts, stacked bars per year, per-project gender breakdown for voters). Yellow is forbidden for either gender on either axis — yellow stays a non-gendered importance accent per `design.md` §2 yellow rule.

### 6.1 Author gender (`author-gender`)

The person who submitted the project.

#### Palette — authors

| Key | UA label | EN label | HEX | Source/role |
|---|---|---|---|---|
| `female` | Жінки | Women | `#9C8BCC` | `colors.primary-200` from design.md (lighter purple) |
| `male` | Чоловіки | Men | `#4E3C84` | `colors.primary-900` from design.md (deeper purple) |
| `unknown` | Невідомо | Unknown | `#CACAD1` | `colors.neutral-300` from design.md (muted grey) |

#### Rules — authors

- **Fixed display order:** `female` → `male` → `unknown`. In legends, female (light purple) sits before male (deep purple), reflecting that women are the historical majority of PB authors (e.g. 2019: 79 women vs 51 men); `unknown` (neutral grey) closes the legend as a non-purple "missing data" tail.
- **Contrast between female and male:** `#9C8BCC` vs `#4E3C84` differs by ~29% lightness (~3.2:1 ratio) — passes WCAG 2.1 SC 1.4.11 for non-text graphical objects (≥ 3:1).
- **`unknown` only appears for 2016** (29 of 80 projects had `authorSex = n/a`). For 2017+ the segment should not be drawn at all unless data adds it.

#### Data availability — authors (snapshot)

| Year | Source | Female | Male | Unknown |
|---|---|---:|---:|---:|
| 2016 | `authorSex` column | 27 | 24 | 29 |
| 2017 | `authorSex` column | 28 | 24 | — |
| 2018 | `authorSex` column | 81 | 58 | — |
| 2019 | `authorSex` column | 79 | 51 | — |
| 2020 | `authorSex` column | TBD | TBD | — |
| 2021 | `authorSex` column | TBD | TBD | — |
| 2022 | PB not held — `years-without-pb` | — | — | — |
| 2023 | `authorSex` column | TBD | TBD | — |
| 2024 | `authorSex` column | TBD | TBD | — |
| 2025 | `authorSex` column | TBD | TBD | — |
| 2026 | `authorSex` column | TBD | TBD | — |

Coverage is complete across the 10 PB cycles; only 2016 carries `unknown` entries (29 of 80 projects had `authorSex = n/a`). 2022 row is the only structural gap and is omitted from every multi-year chart per `years-without-pb`. The TBD cells are filled into this table as the next data ingest lands; the YAML `available-years` already reflects full coverage.

#### Display examples — authors

- **Donut «гендер авторів за 10 років»** — two segments (`female`, `male`); `unknown` only if non-zero across the window.
- **Stacked bar «жінки/чоловіки серед переможців, за роком»** — one bar per year, two stacks (female bottom, male top, following the fixed order); 2022 omitted from the axis per `years-without-pb`.
- **Two-up KPI cards** — «жінки 65%» (#9C8BCC fill) next to «чоловіки 35%» (#4E3C84 fill), Phenomena 56px 900 numbers, captions in Proxima Nova.

### 6.2 Voter gender (`voter-gender`)

The citizens who voted in a given cycle. **Distinct from author-gender** — the same project can be submitted by a male author and receive 70 % of its votes from women.

#### Palette — voters

| Key | UA label | EN label | HEX | Source/role |
|---|---|---|---|---|
| `female` | Жінки-виборчині | Women voters | `#9C8BCC` | `colors.primary-200` from design.md (same as `author-gender.female` — intentional) |
| `male` | Чоловіки-виборці | Men voters | `#4E3C84` | `colors.primary-900` from design.md (same as `author-gender.male` — intentional) |

> No `unknown` key today — the voter dataset has no n/a entries. If a future export introduces them, add `voter-gender.unknown` with `colors.neutral-300` in a MINOR bump (same color rule as author).

#### Rules — voters

- **Fixed display order:** `female` → `male` (light-to-dark; women are the historical majority of voters too — e.g. 2021: 38 000 women vs 12 122 men, ~76 % female).
- **Disambiguation in legends is mandatory.** Write «жінки-виборчині» / «жінки-авторки» — never just «жінки». In a 2-up panel comparing the two axes, position an axis-label band above each chart («ВИБОРЦІ» / «АВТОРИ»).
- **Per-project breakdown is valid.** When showing votes-by-gender for a single project («двір на Галицькій: 70 % жіночих голосів»), split the project's vote bar into two segments using the female/male HEX. The card chip still uses the project's **category** color — gender split is a secondary visualization.

#### Data availability — voters (snapshot)

| Year | Source | Female (votes) | Male (votes) |
|---|---|---:|---:|
| 2016–2020 | not collected | — | — |
| 2021 | voter registry | 38 000 | 12 122 |
| 2022 | PB not held — `years-without-pb` | — | — |
| 2023 | voter registry | TBD | TBD |
| 2024 | voter registry | TBD | TBD |
| 2025 | voter registry | TBD | TBD |
| 2026 | voter registry | TBD | TBD |

Pre-2021 voter gender is not in the source data — render the gap as a footnote («гендер виборців доступний з 2021»), not as silent zero bars. 2022 is omitted from any voter-gender axis the same way as for every other multi-year chart, per `years-without-pb`.

#### Display examples — voters

- **Donut «жінки/чоловіки серед виборців 2021»** — two segments using the voter-gender palette, center label «50 122 голоси» Phenomena Black.
- **Stacked bar 2021–2026** — two segments per year (female bottom, male top); 5 bars total (2021, 2023, 2024, 2025, 2026); 2022 absent from axis.
- **2-up axis comparison «АВТОРИ vs ВИБОРЦІ» for one year** — two donuts side by side, identical female/male HEX; axis-label band «АВТОРИ» above left, «ВИБОРЦІ» above right. Reader sees, say, that 60 % female authors translated into 75 % female voters.
- **Per-project breakdown** — on a project page, a thin horizontal bar split female/male in voter-gender colors, with absolute votes labelled at the segment edges.

---

## 7. Project statuses

Seven real project statuses from PB administrative data. Use these for analytical dashboards. The two promotional badges in `design.md` §2 («Переможець року», «Реалізовано») remain available for promo/pitch material — they are not duplicated here.

| Status | UA label | Fill color | Bg tint | Text | Icon (Lucide) | Finality |
|---|---|---|---|---|---|---|
| `realized` | Реалізований | `#2F8F4E` (success) | `#E8F3EC` | `#1E6B39` | `circle-check` | terminal-positive |
| `in-progress` | На реалізації | `#2563EB` (info) | `#E8EEFD` | `#1E4FBF` | `loader-circle` | active |
| `participated` | Брав участь | `#71737E` (neutral-500) | `#EFEFF1` (neutral-100) | `#3F4049` (neutral-700) | `vote` | neutral |
| `rejected` | Відхилений | `#D97706` (warning) | `#FEF3E2` | `#A05905` | `circle-x` | recoverable |
| `rejected-permanent` | Відхилений остаточно | `#DC2626` (error) | `#FCE9E9` | `#A01818` | `ban` | terminal-negative |
| `impossible` | Неможливо реалізувати | `#3F4049` (neutral-700) | `#E2E2E6` (neutral-200) | `#1A1A1A` | `triangle-alert` | terminal-factual |
| `removed` | Видалений | `#9FA0A9` (neutral-400) | `#F7F7F8` (neutral-50) | `#71737E` (neutral-500) | `trash-2` | terminal-administrative |

### Reading the statuses

- **`realized` (Реалізований)** — project was implemented after winning. Positive terminal state.
- **`in-progress` (На реалізації)** — project is currently being built. Active state, not terminal.
- **`participated` (Брав участь)** — project competed in a vote but did not win that cycle. Neutral, can be re-submitted.
- **`rejected` (Відхилений)** — failed administrative review for this cycle. Author may revise and resubmit.
- **`rejected-permanent` (Відхилений остаточно)** — failed final review with no path forward. Terminal negative.
- **`impossible` (Неможливо реалізувати)** — administrative verdict that physical/legal/financial implementation is not feasible. Graphite (not red) — communicates fact, not blame.
- **`removed` (Видалений)** — administrative removal by a moderator (not a verdict on the project's merits). Muted neutral grey, deliberately quieter than `rejected` or `impossible` — signals «no longer in the dataset for this cycle», not failure. Appears in every cycle 2020–2026 (between 2 and 12 entries per year).

### Badge geometry

Match the chip geometry in `design.md` §4:
- height 24–28px, padding 4px 10px, radius 999px (pill)
- Proxima Nova 12px 600
- icon left, 14px, color = badge text color

---

## 8. Map tokens

The full set of map-specific tokens. `design.md` §9 only states general icon rules; this section is the source of truth for everything map-related.

### Project marker

- Shape: `map-pin` (Lucide), size 24×24px
- Fill: `{canonical-categories.<key>.color}` — the project's category color
- Stroke: 2px solid `#FFFFFF` (separates from map tiles)
- Drop-shadow: `0 1px 2px rgba(26, 26, 26, 0.25)` for legibility on light tiles

### Winner overlay

When the project is a year's winner, overlay a small star on the marker:
- Icon: `star` (Lucide) or 5-pointed SVG, size 10px
- Fill: `#FFEC08` (`secondary-500`)
- Stroke: 1px solid `#1A1A1A` (`ink`) — required so yellow-on-light remains visible
- Placement: top-right of marker, slight overlap

### Cluster

When zoom level groups multiple markers:
- Shape: circle
- Sizes: 28px (2–9 projects), 40px (10–49), 56px (50+)
- Background: `#EEEAF7` (`primary-100`)
- Border: 2px solid `#654EA3` (`primary-500`)
- Label: count, Phenomena 14–16px 700, color `#1A1A1A`, `tabular-nums`
- Hover: border thickens to 3px, no color change

### Choropleth (district-level intensity)

Sequential 5-stop scale for «projects per district» or «budget per district»:
1. `#F6F4FB` (`primary-50`) — lowest
2. `#EEEAF7` (`primary-100`)
3. `#9C8BCC` (`primary-200`)
4. `#7B66B8` (`primary-300`)
5. `#4E3C84` (`primary-900`) — highest

District polygon outline: 1.5px solid `#CACAD1` (`neutral-300`).

For a diverging scale (e.g., budget delta vs. previous year), pair `primary` (positive) with `error` tints (`#FCE9E9` → `#DC2626`), neutral midpoint `#FDFDFD`.

### 2022 — omitted entirely

2022 is not a PB cycle and receives **no visual space** in any chart, slider, or animation.

- **Chart axes (heatmap, bar, streamgraph, timeline):** 10 discrete data points — 2016, 2017, 2018, 2019, 2020, 2021, 2023, 2024, 2025, 2026. The axis jumps directly from 2021 to 2023.
- **Year-range slider:** 10 discrete stops (one per actual cycle). No 2022 position.
- **Context note:** mention «у 2022 БУ не проводився» once in the chart subtitle or caption — never as an axis element.

---

## 9. Usage by AI agents

### How to reference this file

In a prompt, point the agent to **both** `design.md` (system) and `design-data.md` (data):

> Use `design.md` for typography, spacing, brand colors, components. Use `design-data.md` for category palette, status badges, map tokens, gender axis. Do not invent categories or colors.

### Token reference syntax in prompts

When prompts need a category color, write `{data.canonical-categories.<key>.color}` — analogous to `{colors.primary-500}` in `design.md`. Examples:

- `{data.canonical-categories.education-school.color}` → `#4A2D87`
- `{data.canonical-categories.greenery.icon}` → `tree-deciduous`
- `{data.project-statuses.realized.bg-tint}` → `#E8F3EC`
- `{data.project-statuses.removed.color}` → `#9FA0A9`
- `{data.author-gender.female.color}` → `#9C8BCC`
- `{data.author-gender.male.color}` → `#4E3C84`
- `{data.voter-gender.female.color}` → `#9C8BCC` (intentionally same as author female — legends must disambiguate)
- `{data.voter-gender.male.color}` → `#4E3C84` (intentionally same as author male)
- `{data.map-tokens.cluster.border}` → `2px solid #654EA3`
- `{data.districts-color-policy}` → `rules-by-scenario` (means: do not pull a per-district HEX from this file; apply the scenario-based rules in §10.3 instead)

If an agent encounters a gap (a real category not yet listed here), leave a `<!-- TODO: design-data.md needs <key> -->` comment in the artifact — never invent.

### Common multi-year visualization patterns

- **Heatmap (categories × years)** — rows: canonical categories that existed at least once across the chosen window; cells use a sequential primary scale. Cells for years where the category did not exist: render as `neutral-100` with a diagonal hatch or leave blank with «—».
- **Donut for one year** — segments use the canonical color for each category present that year, in fixed display order (§4).
- **Streamgraph 2016–2026** — pre-2019 years collapse into a single «Без категоризації» band in `neutral-300`; 2022 is completely absent from the X-axis (axis goes 2021 → 2023 directly); from 2024 the education band optionally splits into 3 ribbons.
- **Comparison 2016 vs 2026** — left side has only size-based bars; right side has the full canonical breakdown. Make the asymmetry the story («від одного типу до 11 категорій»).

---

## 10. Districts (громади)

PB projects come from the **Ivano-Frankivsk amalgamated territorial community** (об'єднана територіальна громада, ОТГ). After the 2020 amalgamation reform, the community consists of **19 entities**: the city of Ivano-Frankivsk plus 18 surrounding villages.

### 10.1 Canonical list

Use these exact spellings as the source of truth — different administrative sources may write the same village as «Хриплин», «с. Хриплин», or «село Хриплин»; canonicalize to the form below.

| Key | Label (UA) | Label (EN) | Type |
|---|---|---|---|
| `ivano-frankivsk` | Івано-Франківськ | Ivano-Frankivsk | city |
| `vovchynets` | Вовчинець | Vovchynets | village |
| `krykhivtsi` | Крихівці | Krykhivtsi | village |
| `uhornyky` | Угорники | Uhornyky | village |
| `khryplyn` | Хриплин | Khryplyn | village |
| `mykytyntsi` | Микитинці | Mykytyntsi | village |
| `chukalivka` | Чукалівка | Chukalivka | village |
| `cherniiv` | Черніїв | Cherniiv | village |
| `pidpechery` | Підпечери | Pidpechery | village |
| `pidluzhzhia` | Підлужжя | Pidluzhzhia | village |
| `berezivka` | Березівка | Berezivka | village |
| `bratkivtsi` | Братківці | Bratkivtsi | village |
| `dobrovliany` | Добровляни | Dobrovliany | village |
| `drahomyrchany` | Драгомирчани | Drahomyrchany | village |
| `kaminne` | Камінне | Kaminne | village |
| `kolodiivka` | Колодіївка | Kolodiivka | village |
| `radcha` | Радча | Radcha | village |
| `tysmenychany` | Тисменичани | Tysmenychany | village |
| `uzyn` | Узин | Uzyn | village |

All 18 villages joined the community in 2020. PB data prior to 2020 covers only the city; from 2020 onward, projects from any of the 19 entities are eligible.

### 10.2 City-vs-villages asymmetry

The community is structurally lopsided: 1 city accounts for the vast majority of PB participation; 18 small villages share a long tail. Naive visualizations are misleading.

**Bad pattern** — a 19-segment donut where Ivano-Frankivsk is 90% and the rest is unreadable: looks like a single purple circle with confetti.

**Good patterns:**
- **Show the city separately**: «Івано-Франківськ — 1 412 проєктів. Топ-5 серед сіл: …» — pull the city out of the comparison.
- **Normalize per 1000 residents** when comparing absolute numbers — exposes engagement intensity, not raw scale.
- **Two-segment summary** «місто vs усі села разом» when a single split is needed.
- **Villages-only mode** for a deep-dive feature on rural participation — explicit toggle/filter.

### 10.3 Color rules by scenario

This file does **not** assign fixed colors per district. Use the rules below; they reuse `design.md` core tokens, never introduce district-specific HEX.

| Scenario | Color rule |
|---|---|
| Choropleth / density heatmap (district = intensity) | Sequential primary scale: `primary-50` → `primary-100` → `primary-200` → `primary-300` → `primary-900`. Color encodes value, not identity. |
| Bar chart — all districts on X-axis | Single fill `primary-500`. The district is the label. |
| Top-N ranking | Rank-based: `secondary-500` (yellow + 1.5px ink stroke) for #1; `primary-500` for #2–3; `primary-300` for #4–5; `neutral-500` for #6+. Color encodes rank, not identity. |
| 2-way head-to-head comparison | District A → `primary-500`; District B → `primary-300`. |
| Multi-line trend (3–5 lines) | Fixed order: `primary-900` / `primary-500` / `primary-300` / `primary-200` / `#3F4049` (graphite). Assign in order of appearance in the narrative; legend mandatory. |
| Donut with 5–7 entities + «Інші» | Same multi-line fixed order; «Інші» segment → `neutral-300`. |
| Map markers for individual projects | Marker fill = **category color** (per §4), never district color. The district is encoded by geographic position. |

### 10.4 When fixed colors per district may emerge later

If real PB data narratives consistently feature **2–4 «hero» districts** (e.g., one village wins multiple top-N rankings; another drives a recurring story arc), those districts may receive canonical colors in a future MINOR bump. Until that pattern emerges from actual data, fixed colors are deliberately deferred.

---

## 11. Known gaps

- **Fixed «hero district» colors.** §10 enumerates all 19 community entities and gives rules-by-scenario for color, but does **not** assign canonical colors per district. Such colors will be added in a future MINOR bump only when 2–4 «hero» districts emerge from real PB data narratives — overcommitting now would lock the system to predictions, not facts.
- **Real project counts and budgets per category.** This file maps colors and icons, not numeric data. Aggregated counts per year/category come from the PB administrative export, not from a design artifact.
- **Author-record categories** (top-N authors with most winning projects). Not a design concern; lives in product data.

---

## Quick reference

```
CANONICAL CATEGORIES (11)
  education-general          #654EA3   graduation-cap
  education-school           #4A2D87   school
  education-preschool        #7B66B8   baby
  education-extracurricular  #9E5FAB   compass
  improvement-general        #2D6BAB   hammer
  improvement-streets        #1A4F82   route
  heritage                   #A0571F   landmark
  greenery                   #3D7C3F   tree-deciduous
  afu-support                #3F4049   shield
  accessibility              #0E7C8C   accessibility
  other                      #71737E   package

PROJECT STATUSES (7)
  realized              success-green
  in-progress           info-blue
  participated          neutral-grey
  rejected              warning-amber
  rejected-permanent    error-red
  impossible            graphite
  removed               muted-grey  (admin removal — not a verdict)

AUTHOR GENDER (orthogonal axis — who submitted)
  female    #9C8BCC  primary-200   (lighter purple)
  male      #4E3C84  primary-900   (deeper purple)
  unknown   #CACAD1  neutral-300   (2016 only)
  Order: female → male → unknown. No icons.

VOTER GENDER (orthogonal axis — who voted)
  female    #9C8BCC  primary-200   (same as author female — intentional)
  male      #4E3C84  primary-900   (same as author male — intentional)
  Order: female → male. Available 2021, 2023–2026 (2022 skipped per years-without-pb).
  Legends MUST disambiguate "автори" vs "виборці" — palettes overlap.

YEARS COVERED: 2016–2026 (10 cycles, 2022 skipped)

DISTRICTS: 19 (1 city + 18 villages, since 2020)
  Color policy: rules-by-scenario (§10.3), no fixed-color-per-district
```
