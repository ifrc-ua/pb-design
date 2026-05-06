# Промпти для аналітичної інфографіки

Готові промпти для створення інфографіки на основі 10-річних даних БУ Івано-Франківська. **Характер усіх візуалізацій — ретроспективна аналітика**, не поточний цикл. Усі промпти передбачають, що агент вже має доступ до [design.md](../design.md).

> **Як користуватися:** скопіюйте промпт, підставте ваші цифри/назви замість `{плейсхолдерів}`, дайте агенту разом із посиланням на `design.md`.

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
2. "{127К}" / "УНІКАЛЬНИХ УЧАСНИКІВ"
3. "{₴62 МЛН}" / "РЕАЛІЗОВАНО"

Background #FDFDFD, padding 64px, border-radius 24px, shadow level 1.
```

---

## 2. Картка історичного проєкту

```
Build a project card 360×480px for a historical PB project.

Structure:
- Photo at top, 360×240, border-radius 12px
- Category chip below photo (left-aligned): pill 28px height, bg rgba({category-rgb}, 0.15), text {category-hex-dark}, Proxima Nova 12px 600, with a 14px icon on the left
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
Create a heatmap 1200×640 showing how citizen interest shifted across 7 categories over 10 years.

Grid:
- Rows (7): Освіта, Екологія, Безпека, Спорт, Транспорт, Культура, Благоустрій
- Columns (10): 2016, 2017, 2018, 2019, 2020, 2021, 2023, 2024, 2025, 2026 (skip 2022 — no PB held that year)

Cell styling:
- Size: 104×56px, gap 2px
- Border-radius: 4px
- Fill: sequential purple scale #F6F4FB (lowest) → #4E3C84 (highest)
- Label inside each cell: count of winning projects, Proxima Nova 12px 500, tabular-nums, auto-contrast text color

Axes:
- Row labels (left): Proxima Nova 13px 600, color #3F4049, with 16px category icon before text
- Column labels (bottom): Proxima Nova 12px 600 uppercase letter-spacing +1px, color #71737E

Title above (H2 style): "Як змінювалися інтереси мешканців, 2016–2026" in Phenomena 32px 700, color #1A1A1A.

Subtitle: "Кількість проєктів-переможців у кожній категорії за рік" in Proxima Nova 15px 400, color #71737E.

Legend bottom: horizontal gradient bar with labels "0" and "{max}" at ends.

Background #FDFDFD, overall padding 32px.
```

---

## 4. Діаграма розподілу голосів (donut)

```
Design a donut chart 520×520 showing vote share across 7 categories for year {2023}.

Donut:
- Outer radius 240, inner 140
- Segments colored with categorical data-viz palette in a fixed order, one color per category. Yellow segments must carry a 1.5px dark outline `#1A1A1A`. <!-- TODO: design-data.md needs the canonical 7-category categorical palette (Освіта, Екологія, Безпека, Спорт, Транспорт, Культура, Благоустрій). Until that file exists, the agent must derive a palette from {colors.primary-500}, {colors.primary-300}, {colors.primary-100}, {colors.secondary-500}, and neutrals — and never invent categorical HEX values. -->
- Gaps between segments: 2px
- Hover: segment pushes out 8px, darkens by 10%

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
1. Year range slider 2016–2026, skipping 2022 (track #EFEFF1, active #654EA3, handle 16px with dark purple border; mark 2022 as disabled tick — no PB that year)
2. District multi-select dropdown
3. Category checkboxes with color swatches (8px squares matching data-viz palette)
4. Toggle "Тільки переможці" (track #CACAD1 / #654EA3 active)
5. Applied filters chips: removable pills with × icon

Map styling:
- Base: MapLibre Positron or custom light style, muted neutrals
- Project markers: map-pin 24px, fill = category color, 2px white stroke
- Winners: same pin + 10px yellow star (#FFEC08, 1px dark stroke) overlaid on top-right of pin
- Cluster: circle with Phenomena 14–16px 700 number, bg #EEEAF7, border 2px #654EA3

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
Create a streamgraph 1200×400 showing distribution of total PB budget across 7 categories over 10 years.

X-axis: years 2016–2026, skipping 2022 (Proxima Nova 12px 600 uppercase, color #71737E)
Y-axis: hidden; streamgraph is symmetric around center
Layers (7, in data-viz palette order, no outlines except yellow which gets #1A1A1A 1px stroke)
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
4. Category chip (pill, color)
5. District (Proxima Nova 14px 500)
6. Year (Proxima Nova 14px 500, tabular-nums)
7. Votes (Phenomena 20px 700, tabular-nums, right-aligned)
8. Budget (Phenomena 20px 700, tabular-nums, right-aligned)
9. Status badge (реалізовано / не реалізовано)

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
3. Supporting chart: a small comparison bar chart 2018 vs 2020 vs 2024 for "екологія" category — 3 bars in the canonical category color, 2020 highlighted with yellow outline. <!-- TODO: design-data.md needs the "екологія" category color. Until then, fall back to {colors.primary-500} for the bars and {colors.secondary-500} with dark outline for the highlighted year. -->
4. Pullquote: "Зелень стала важливішою за асфальт." in Phenomena 32px 400 italic, color #654EA3, left border 4px #FFEC08, padding-left 24px, max-width 700px
5. Second chart: streamgraph mini (same style as prompt #6 but compact 800×240)
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
- At bottom: stacked horizontal bar chart showing 7 categories share, each bar 32px tall, gap 2px
- Small faces/portraits grid (optional): top 3 authors with name labels

Separator: 2px vertical line #EFEFF1, center

Below both: synthesis paragraph "За 10 років бюджет БУ зріс у X разів, активність — у Y разів" in Proxima Nova 18px 400, centered, max-width 720px, color #3F4049.
```

---

## 10. Картка автора-рекордсмена

```
Design an author profile card 320×420 for "{Марія Коваленко — 5 переможних проєктів за 10 років}".

Layout:
- Top: circular avatar 120px centered, 2px border #654EA3
- Name: Phenomena 24px 700 centered, color #1A1A1A
- Subtitle: "{Район Пасічна}" in Proxima Nova 14px 500 #71737E
- Divider: 1px #EFEFF1, width 80px, centered
- 4 mini-stats in 2×2 grid:
  - "5" / "переможних проєктів"
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
