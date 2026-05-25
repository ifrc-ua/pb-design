# Промпти для аналітичної інфографіки

Готові промпти для створення інфографіки на основі 10-річних даних БУ Івано-Франківська. **Характер усіх візуалізацій — ретроспективна аналітика**, не поточний цикл. Усі промпти передбачають, що агент має доступ до [design.md](../design.md) (система) та [design-data.md](../design-data.md) (реальні категорії, статуси, мап-токени).

> **Як користуватися:** скопіюйте промпт, підставте ваші цифри/назви замість `{плейсхолдерів}`, дайте агенту разом із посиланнями на `design.md` і `design-data.md`.

---

## 1. Hero-картка «10 років у числах»

```
Create a hero stat card 1280×520px for the landing page of "10 років БУ Івано-Франківська".

Layout: three equal columns divided by thin Primary-100 #EEEAF7 lines.

Each column contains:
- Big display number in Phenomena Black, 96px, color #654EA3, tabular-nums
- Below: label in Proxima Nova 16px 600 uppercase, letter-spacing +1px, color #71737E

Column values:
1. "{1 412}" / "ПРОЄКТІВ ЗА 10 РОКІВ"
2. "{127 тис.}" / "УНІКАЛЬНИХ УЧАСНИКІВ"
3. "{₴62 МЛН}" / "РЕАЛІЗОВАНО"

Background #FDFDFD, padding 64px, border-radius 24px, shadow level 1.
```

---

## 2. Картка історичного проєкту

```
Build a project card 360×480px for a historical PB project.

Structure:
- Photo at top, 360×240, border-radius 12px
- Category chip below photo (left-aligned): pill 28px height, bg rgba({category-rgb}, 0.15), text {category-hex-dark}, Proxima Nova 12px 600, with a 14px icon on the left. Pull color and icon from {data.canonical-categories.<key>.color} and {data.canonical-categories.<key>.icon} (see design-data.md §4).
- Title: Proxima Nova 20px 600, color #1A1A1A, max 2 lines
- Meta line: "{Ім'я Автора} · {Район}" in Proxima Nova 14px 400, color #71737E
- Stats row (two values side by side):
  - "{2 847}" голосів — Phenomena 24px 700 + label 12px 500 uppercase
  - "₴{1.2 млн}" бюджет — same style
- Bottom-right badge: "Переможець {2019}" — pill bg #FFEC08, text #1A1A1A, Proxima Nova 12px 600, with small star icon

Card: bg #FDFDFD, border 1px #EFEFF1, radius 12px, padding 20px, shadow level 1 (hover level 2).

Variables: {title}, {author}, {district}, {year}, {category}, {votes}, {budget}, {photo_url}.
```

---

## 3. Heatmap категорій × років

```
Create a heatmap 1200×640 showing how citizen interest shifted across PB categories over 10 cycles (2016–2026, skip 2022).

Grid rows — use the canonical-category list from design-data.md, only those with active-years overlapping the chosen window. For a full 2019–2026 window, that is 11 rows in this fixed order:
1. Освіта (education-general)
2. Шкільні (education-school)
3. Дошкільні (education-preschool)
4. Позашкільні, профтехосвіта (education-extracurricular)
5. Благоустрій (improvement-general)
6. Благоустрій малих вулиць (improvement-streets)
7. Архітектурна спадщина (heritage)
8. Зелені проєкти (greenery)
9. Допомога ЗСУ (afu-support)
10. Доступність (accessibility)
11. Інші проєкти (other)

Columns: 2016, 2017, 2018, 2019, 2020, 2021, 2023, 2024, 2025, 2026 — 10 columns total. Do NOT add a 2022 column (no slot, no disabled tick — simply absent). The subtitle «у 2022 БУ не проводився» in the chart subtitle is sufficient context.

Cell styling:
- Size: 104×56px, gap 2px
- Border-radius: 4px
- Fill: sequential purple scale {colors.primary-50} (lowest) → {colors.primary-900} (highest)
- Label inside each cell: count of winning projects, Proxima Nova 12px 500, tabular-nums, auto-contrast text color
- For (category, year) pairs where the category did not exist that year (consult design-data.md §3 active-years): fill {colors.neutral-100} with a 1px diagonal hatch in {colors.neutral-300}, no number

Axes:
- Row labels (left): Proxima Nova 13px 600, color #3F4049, with 16px category icon (see design-data.md §4) before text in the canonical category color
- Column labels (bottom): Proxima Nova 12px 600 uppercase letter-spacing +1px, color #71737E

Title above (H2 style): "Як змінювалися інтереси мешканців, 2016–2026" in Phenomena 32px 700, color #1A1A1A.

Subtitle: "Кількість проєктів-переможців у кожній категорії за рік" in Proxima Nova 15px 400, color #71737E.

Legend bottom: horizontal gradient bar with labels "0" and "{max}" at ends.

Background #FDFDFD, overall padding 32px.
```

---

## 4. Діаграма розподілу голосів (donut)

```
Design a donut chart 520×520 showing vote share across PB categories for year {2023}.

Donut:
- Outer radius 240, inner 140
- Segments colored with the canonical-category palette from design-data.md §4. Use only the categories that were active in {2023}. For 2023 specifically those are: Освіта (education-general), Інший благоустрій → improvement-general, Благоустрій малих вулиць (improvement-streets), Зелені проєкти (greenery). Pull each fill from {data.canonical-categories.<key>.color}.
- Render segments in the canonical fixed display order from design-data.md §4, regardless of segment size.
- Gaps between segments: 2px
- Hover: segment pushes out 8px, darkens by 10%
- Never use yellow {colors.secondary-500} as a categorical segment fill — it is reserved as the «exceptionally important» accent. To highlight a single category, add a 1.5px dark outline `#1A1A1A` over its native color.

Center:
- Big number "{14 832}" in Phenomena Black 56px, color #1A1A1A, tabular-nums
- Below: "голосів у {2023}" in Proxima Nova 14px 500, color #71737E

Legend right side:
- Category name + % + count, in Proxima Nova 14px 500
- Color swatch 12×12 rounded 2px before text
- Sorted by size descending
```

---

## 5. Карта міста з проєктами

```
Design a responsive map layout for city-wide PB analytics.

Desktop (1440×900):
- Left sidebar 320px: filters
- Right: map with controls top-right

Sidebar filters:
1. Year range slider with 10 discrete stops — one per actual PB cycle: 2016, 2017, 2018, 2019, 2020, 2021, 2023, 2024, 2025, 2026. The slider jumps from 2021 directly to 2023 — no 2022 stop. Styling: track #EFEFF1, active range #654EA3, handle 16px circle white/purple-border.
2. District multi-select dropdown
3. Category checkboxes with color swatches (8px squares — pull each color from {data.canonical-categories.<key>.color} in design-data.md §4; only show categories whose active-years overlap the selected year range)
4. Toggle "Тільки переможці" (track #CACAD1 / #654EA3 active)
5. Applied filters chips: removable pills with × icon

Map styling — strictly per design-data.md §8:
- Base: MapLibre Positron or custom light style, muted neutrals
- Project markers: map-pin 24px, fill = {data.canonical-categories.<project-category-key>.color}, 2px white stroke
- Winners: same pin + 10px yellow star ({colors.secondary-500}, 1px dark stroke {colors.ink}) overlaid on top-right of pin
- Cluster: circle 28/40/56px with Phenomena 14–16px 700 number, bg {colors.primary-100}, border 2px {colors.primary-500}

Popover on pin click:
- 320px wide, radius 12px, shadow level 3
- Photo thumb 80×60, title (Proxima Nova 16px 600), author+year (14px 400 #71737E), stats line, "Детальніше →" link in #654EA3

Mobile (375×812):
- Map full-screen
- Filters collapsed into bottom-sheet (drag handle at top)
- Applied filters as horizontal scroll chips above map
```

---

## 6. Streamgraph — еволюція бюджету

```
Create a streamgraph 1200×400 showing distribution of total PB budget across canonical categories over 10 cycles (2016–2026, skip 2022).

X-axis: 10 years in order — 2016, 2017, 2018, 2019, 2020, 2021, 2023, 2024, 2025, 2026. Do NOT add a 2022 slot. Axis jumps from 2021 to 2023. (Proxima Nova 12px 600 uppercase, color #71737E)
Y-axis: hidden; streamgraph is symmetric around center
Layers — use canonical categories from design-data.md §4 in the fixed display order. For each layer, fill = {data.canonical-categories.<key>.color}. Years where a category did not yet exist are 0-height for that layer (the layer only appears when its active-years begin). Pre-2019 years are merged into a single «Без категоризації» band in {colors.neutral-300} since no thematic split existed.
No outlines on category fills. Yellow {colors.secondary-500} is NOT used as a category color — only for highlighting a specific data point on top, in which case it carries a 1px {colors.ink} stroke.
Curves: smooth (monotone), no sharp corners.

Annotations:
- Small callouts on notable moments (e.g., "COVID: екологія +47%" in 2020) — Proxima Nova 12px 600, connected by thin 1px line to the layer
- Total budget per year shown above at each year tick: "₴{6.2 млн}" in Phenomena 16px 700 tabular-nums

Title: "₴62 млн за 10 років — куди йшли гроші" in Phenomena 32px 700.
Subtitle: "Розподіл реалізованих бюджетів за категоріями" in Proxima Nova 15px 400 #71737E.
Legend top-right as horizontal chips.
Background #FDFDFD, padding 32px.
```

---

## 7. Таблиця топ-10 проєктів-чемпіонів

```
Design a leaderboard table "Топ-10 проєктів за 10 років".

Columns (desktop):
1. № (40px, Phenomena 24px 700, color #654EA3)
2. Photo thumb (60×45, radius 6px)
3. Title + author line below (Proxima Nova 16px 600 title, 13px 400 #71737E author)
4. Category chip (pill) — bg = rgba({data.canonical-categories.<key>.color}, 0.15), text = darker version of the same color, with the canonical icon (design-data.md §4)
5. District (Proxima Nova 14px 500)
6. Year (Proxima Nova 14px 500, tabular-nums)
7. Votes (Phenomena 20px 700, tabular-nums, right-aligned)
8. Budget (Phenomena 20px 700, tabular-nums, right-aligned)
9. Status badge — pull from design-data.md §7 (one of: Реалізований, На реалізації, Брав участь, Відхилений, Відхилений остаточно, Неможливо реалізувати, Видалений)

Row:
- Height 72px
- Hover: bg #F6F4FB (Primary-50)
- Border-bottom 1px #EFEFF1 between rows
- Rank 1–3: rank number in yellow highlight pill

Header:
- bg #F7F7F8 (neutral-50)
- Sticky on scroll
- Labels: Proxima Nova 12px 600 uppercase letter-spacing +1px color #71737E

Mobile (< 600px):
- Card-based stack instead of rows
- Each card has rank + title + meta + stat row
```

---

## 8. Сторінка інсайту «Неочевидне»

```
Create a full-width insight storytelling page 1200px wide.

Structure:
1. Hero number at top-left: "47%" in Phenomena Black 160px, color #654EA3, tabular-nums
   Right: headline "Проєктів переможців 2020 — про екологію" in Phenomena 40px 700 on 2 lines
2. Lede paragraph: "У ковідний рік мешканці ІФ проголосували за проєкти озеленення і парків майже удвічі активніше..." Proxima Nova 20px 400 line-height 1.55, max-width 760px
3. Supporting chart: a small comparison bar chart 2018 vs 2020 vs 2024 for "Зелені проєкти" — 3 bars in {data.canonical-categories.greenery.color} (#3D7C3F), 2020 highlighted with a 1.5px {colors.ink} outline plus a small yellow {colors.secondary-500} accent dot above the bar. Note: «Зелені проєкти» as a formal category appeared only in 2023; for pre-2023 years use the data point if it exists in administrative records under a related label, otherwise mark the bar with «—» and a footnote.
4. Pullquote: "Зелень стала важливішою за асфальт." in Phenomena 32px 400 italic, color #654EA3, left border 4px #FFEC08, padding-left 24px, max-width 700px
5. Second chart: streamgraph mini — same style as the `Streamgraph — еволюція бюджету` template above, but compact 800×240
6. Callout box bottom: Light Primary-50 bg, radius 16px, padding 32px — "Дослідити всі інсайти →" CTA link in #654EA3 Proxima Nova 18px 600 + arrow

Overall: bg #FDFDFD, generous vertical spacing (64–96px between blocks), max-width 880px centered for text blocks, charts can go full 1200px.
```

---

## 9. Порівняння двох років side-by-side

```
Create a split-screen comparison 1200×600: left "2016" vs right "2026".

Each side:
- Year label top: Phenomena 72px 900, color #654EA3 (or Primary-900 for 2016, to differentiate)
- Below: 3 stat rows with label + big number
  - Проєкти-переможці: {N}
  - Голосів подано: {N}
  - Бюджет: ₴{N}
- At bottom: stacked horizontal bar chart showing the categories share for that side. Left side (2016) has only one segment «Без категоризації» in {colors.neutral-300} (no thematic split existed pre-2019). Right side (2026) splits across the 11 canonical categories from design-data.md §4 in fixed display order, each segment using {data.canonical-categories.<key>.color}. Each bar 32px tall, gap 2px.
- Top-3 authors strip (optional): names + район only, no portraits (per design.md §5). Format: "Марія К. · Пасічна · 5 переможних" each line, Proxima Nova 14px 500

Separator: 2px vertical line #EFEFF1, center

Below both: synthesis paragraph "За 10 років бюджет БУ зріс у X разів, активність — у Y разів" in Proxima Nova 18px 400, centered, max-width 720px, color #3F4049.
```

---

## 10. Картка автора-рекордсмена

```
Design an author profile card 320×420 for "{Марія Коваленко — 5 переможних проєктів за 10 років}".

Per design.md §5 — no avatars or portraits, ever (resident-privacy rule). The hero is the count, not the face.

Layout:
- Top hero block (centered): tiny overline "ПЕРЕМОЖНИХ ПРОЄКТІВ" Proxima Nova 11px 600 uppercase letter-spacing +1px color #71737E, then giant number "5" Phenomena Black 120px color #654EA3 tabular-nums, line-height 1.0
- Name: Phenomena 24px 700 centered, color #1A1A1A — "{Марія Коваленко}"
- Subtitle: "{Район Пасічна}" in Proxima Nova 14px 500 #71737E
- Divider: 1px #EFEFF1, width 80px, centered
- 3 mini-stats in horizontal row (the "5 переможних" stat already lives at the top as hero):
  - "12" / "поданих заявок"
  - "₴4.8М" / "реалізовано"
  - "2016–2024" / "активна"
  Each stat: Phenomena 28px 700 number + Proxima Nova 11px 500 uppercase letter-spacing +1px label #71737E
- Bottom: small list of her top 3 project titles in Proxima Nova 13px 500, each prefixed with a year tag

Card: bg #FDFDFD, border 1px #EFEFF1, radius 16px, padding 24px, shadow level 1.
```

---

## Підказки щодо використання

1. **Завжди передавайте `design.md`** агенту разом із промптом — без нього він не знатиме точних HEX і шрифтових розмірів.
2. **Замінюйте `{плейсхолдери}`** на реальні дані перед відправленням.
3. **Для SVG-експорту** додавайте: «Return as clean SVG with embedded fonts as text (not outlines), no PNG fallbacks.»
4. **Якщо агент вигадує кольори**, нагадайте: «Use ONLY colors from the design system — no generic purples or yellows.»
5. **Для Figma-плагінів (Stitch тощо)** можна дати прямий URL на `design.md`.
