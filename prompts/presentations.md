# Промпти для слайдів презентацій

Промпти для створення слайдів у 16:9 (1920×1080) про історичні дані БУ ІФ — для виступів у мерії, на громадських обговореннях, конференціях.

Передбачається, що агент має доступ до [design.md](../design.md).

---

## Загальні правила слайдів

- Формат: **1920×1080** (16:9), з safe-zone 80px з усіх боків
- Фон: `#FDFDFD` (основний), `#F6F4FB` (акцентний) або `#1A1A1A` (інверсія для секційних слайдів)
- Логотип у нижньому правому куті, 32px висота
- Номер слайду + «БУ ІФ · 10 років» у нижньому лівому куті, Proxima Nova 14px 500 `#71737E`
- Верхній дискретний розділювач: 4px `#FFEC08` на 120px від лівого краю у верхній частині слайду (як «підкреслення»)
- Максимум 1 ключова ідея на слайд
- Шрифти: Phenomena для заголовків і чисел, Proxima Nova для всього решти

---

## 1. Cover slide (обкладинка)

```
Create a 1920×1080 title slide.

Background: solid #FDFDFD with a large circle shape top-right (radius 1100px, fill #EEEAF7, partially off-canvas — only bottom-left quarter visible).

Content (left-aligned, starting at x=160):
- Overline "ГРОМАДСЬКА ПРЕЗЕНТАЦІЯ · 2026" in Proxima Nova 20px 600 uppercase letter-spacing +2px color #71737E at y=320
- Giant title "10 років Бюджету участі" Phenomena Black 160px color #1A1A1A at y=380, single line
- Below: "Івано-Франківськ" Phenomena 96px 400 color #654EA3 at y=560
- Lead paragraph (max-width 900px): "Як змінювалися пріоритети мешканців, хто переможці-рекордсмени і що дані розповідають про нас" in Proxima Nova 26px 400 color #3F4049 at y=720
- Speaker line bottom: "Ім'я Прізвище · Посада" in Proxima Nova 22px 600 color #1A1A1A at y=920

Bottom-right: small URL "pb.if.ua" in Proxima Nova 18px 500 color #71737E.
```

---

## 2. Section divider (розділювач розділу)

```
Create a 1920×1080 section-divider slide.

Background: solid #1A1A1A.
Top-right corner: thin 4px line in #FFEC08 that extends from edge 200px inward.

Content centered vertically:
- Giant section number "02" in Phenomena Black 320px color #FFEC08, left-aligned at x=160
- Section title "Географія участі" in Phenomena 96px 700 color #FDFDFD at y=center+40
- Short subtitle "Які райони голосують активніше і чому" Proxima Nova 28px 400 color rgba(253,253,253,0.7) below title

No logo, no slide number (divider is visually clean).
```

---

## 3. Big Number slide

```
Create a 1920×1080 "one big number" slide.

Background #FDFDFD.
Content:
- Eyebrow line at y=280: "ЗА 10 РОКІВ" in Proxima Nova 28px 600 uppercase letter-spacing +2px color #654EA3, x=160
- Giant number centered: "127 400" in Phenomena Black 480px color #1A1A1A tabular-nums, center-aligned horizontally, y=450 baseline
- Below number: "унікальних учасників" in Phenomena 64px 400 color #1A1A1A, centered
- Footnote annotation: "кожен п'ятий повнолітній мешканець міста" Proxima Nova 24px 500 italic color #71737E, centered, y=bottom-120

Optional: thin yellow underline (4px, width 200px) between giant number and subtitle.
```

---

## 4. Chart slide (графік + інсайт)

```
Create a 1920×1080 slide with a chart and takeaway.

Left column (50%, x=160–960):
- Title "Динаміка бюджету БУ, 2016–2026" Phenomena 44px 700 at y=200
- Chart 720×480: grouped bars per year, primary bars #654EA3, highlighted year 2023 #FFEC08 with dark stroke
- X-axis Proxima Nova 14px 600 uppercase, Y-axis values above each bar in Phenomena 18px 700 tabular-nums

Right column (50%, x=1000–1760):
- Headline "Ковідний рік став переломним" Phenomena 52px 700 color #1A1A1A at y=200, max 3 lines
- Supporting paragraph below: "У 2020 бюджет виріс на 40%, а кількість проєктів — у півтора раза. Мешканці хотіли змінити простір навколо себе." Proxima Nova 22px 400 color #3F4049 line-height 1.55, max-width 720px
- Key stat pull-quote bottom: "+40%" in Phenomena Black 120px color #654EA3 tabular-nums, label "зростання бюджету у 2020" Proxima Nova 18px 500 uppercase letter-spacing +1px color #71737E

Subtle divider 2px #EFEFF1 between columns.
```

---

## 5. Map slide (мапа)

```
Create a 1920×1080 slide showing a city-wide map.

Left 35% (x=80–720):
- Title "Де живуть активісти" Phenomena 44px 700
- Short paragraph explaining what's shown (Proxima Nova 22px 400 #3F4049, max-width 540px)
- Legend: 4 density levels with square swatches (sequential purple scale) + label each

Right 65% (x=720–1840):
- Map of Івано-Франківськ (MapLibre or Mapbox light style) with choropleth fill per district using sequential purple
- Thin #1A1A1A 1.5px borders between districts
- District labels in Proxima Nova 14px 600 color #1A1A1A, drop-shadow 2px white for legibility
- Top 3 districts marked with yellow star markers (#FFEC08 16px with dark border)

Title overlay on map top-right: "Активність 2016–2026" small pill Proxima Nova 14px 600 uppercase on white #FDFDFD semi-opaque bg.
```

---

## 6. Comparison slide (порівняння)

```
Create a 1920×1080 comparison slide "2016 vs 2026".

Two columns split 50/50 with 2px vertical divider #EFEFF1 at x=960.

Each column structure:
- Year header Phenomena Black 200px tabular-nums (left column color Primary-900 #4E3C84 for 2016, right column Primary-500 #654EA3 for 2026), centered horizontally in column
- Below: 3 stat rows, each:
  - Label Proxima Nova 18px 600 uppercase letter-spacing +1px color #71737E
  - Value Phenomena 56px 900 color #1A1A1A tabular-nums

Stats to show:
- Кількість проєктів
- Голосів подано
- Бюджет (₴)

Bottom band spanning full width: y=920, height 80px, bg #FFEC08
- Centered text "За 10 років бюджет виріс у 4 рази, активність — у 6" Phenomena 32px 700 color #1A1A1A
```

---

## 7. Timeline slide

```
Create a 1920×1080 horizontal timeline slide.

Title top: "10 років — 10 моментів" Phenomena 56px 700 color #1A1A1A, x=160, y=160

Timeline at y=500 (vertical center):
- Horizontal line 3px #EFEFF1 from x=160 to x=1760
- 10 dots evenly spaced (16px, filled #654EA3), one per actual PB year: 2016, 2017, 2018, 2019, 2020, 2021, 2023, 2024, 2025, 2026. Exactly 10 positions — no slot for 2022, axis goes 2021 → 2023 directly.
- Year labels below each dot: Proxima Nova 16px 600 tabular-nums color #71737E

Above the line (alternating for labels), callouts for 4–5 key moments:
- Each callout: pill bg #FFF9B3 (Secondary-100) border 1px #E6D307, radius 8px
- Content: year + event, Proxima Nova 16px 500 color #1A1A1A
- Connected to its dot with thin 1px line
- Examples: "2018: перші 100 проєктів", "2020: рекорд активності", "2023: перший громадський простір на 10 млн"

Footer: "Повний таймлайн у додатку" Proxima Nova 18px 500 color #71737E, bottom-right.
```

---

## 8. Quote slide

```
Create a 1920×1080 quote/testimonial slide.

Background #F6F4FB (Primary-50).

Left side (40%, x=160):
- Portrait photo circular 400×400, border 4px #FFEC08

Right side (60%, x=720):
- Large quotation mark "«" in Phenomena 200px color #654EA3 opacity 0.4 at top
- Quote text Phenomena 40px 400 italic color #1A1A1A line-height 1.3, max-width 960px, 4–5 lines
  Example: "Коли мій двір переміг у голосуванні, я вперше відчула, що моя думка важить у цьому місті."
- Attribution below: "— Марія К., Пасічна · проєкт-переможець 2019" Proxima Nova 20px 600 color #71737E
```

---

## 9. Takeaway / closing slide

```
Create a 1920×1080 closing slide with 3 key takeaways.

Title top: "Що нам розповіли дані" Phenomena 56px 700 color #1A1A1A at y=140, x=160

Three columns (equal width, 560px each, gaps 40px) at y=340:

Each column:
- Big icon top (80px, Lucide or Phosphor, color #654EA3)
- Takeaway headline Phenomena 32px 700 color #1A1A1A, 2 lines
- Supporting text Proxima Nova 18px 400 color #3F4049 line-height 1.55, 4 lines

Example takeaways:
1. 🌳 "Екологія перемогла асфальт" / "За 10 років зелень і парки обігнали ремонт доріг утричі"
2. 🏙 "Центр проти районів" / "72% переможних проєктів у центрі — нерівність простору, яку видно в цифрах"
3. 📈 "Ковід прискорив БУ" / "У 2020 активність виросла на 40% — криза посилила участь"

Bottom full-width CTA band:
- y=900, height 180px, bg #1A1A1A
- Left: "Дослідити 127 тисяч голосів →" Phenomena 36px 700 color #FDFDFD
- Right: URL "pb.if.ua" Phenomena 36px 700 color #FFEC08
```

---

## 10. Thank-you slide

```
Create a 1920×1080 thank-you closing.

Background #FDFDFD with large "+" shape top-right (fill #FFEC08, 800×800px, 50% off-canvas, subtle).

Centered vertically:
- "Дякуємо." Phenomena Black 320px color #1A1A1A
- Below: "Питання?" Phenomena 80px 400 color #654EA3
- Contact line: "ім'я.прізвище@ifrc.org.ua · @ifbudget" Proxima Nova 24px 500 color #71737E
- URL "pb.if.ua" Phenomena 40px 700 color #654EA3 at bottom-center
```

---

## Генерація повної колоди

```
Create a 15-slide deck in 1920×1080 using the PB IF design system.

Structure (each item references a template above by its title — see headings `## N. <Name>`):
1. Cover slide — use the `Cover slide` template
2. Agenda — 4-item list, Proxima Nova 28px, numbered with Phenomena 48px 700 purple
3. Section divider "Контекст" — use the `Section divider` template
4. Big number: "1 412 проєктів" — use the `Big Number slide` template
5. Chart: budget dynamics 2016–2026 — use the `Chart slide` template
6. Section divider "Географія" — use the `Section divider` template
7. Map slide with district activity — use the `Map slide` template
8. Big number: "127 400 учасників" — `Big Number slide` template variant
9. Section divider "Люди" — use the `Section divider` template
10. Quote slide — use the `Quote slide` template
11. Comparison 2016 vs 2026 — use the `Comparison slide` template
12. Timeline 10 років — use the `Timeline slide` template
13. Section divider "Інсайти" — use the `Section divider` template
14. Takeaways — use the `Takeaway / closing slide` template
15. Thank-you — use the `Thank-you slide` template

Use consistent footer (slide number + project name + logo), consistent 4px yellow top-detail line on non-divider slides, consistent color palette, consistent fonts.
```

---

## Підказки

1. **Експорт:** запитайте агента «return as 15 separate HTML files (one per slide) using inlined fonts via @font-face pointing to /fonts/, so they can be exported to PDF».
2. **Для Keynote/PowerPoint:** агент не зробить рідний `.pptx`, але може створити HTML/SVG — експортуйте через браузер у PDF, потім вставте в Keynote як зображення або через «Insert Slides from File».
3. **Консистентність:** завжди вказуйте «use the same footer pattern across all slides».
4. **Шрифти в HTML:** нехай агент вкаже `@font-face { src: url('/fonts/Phenomena/Phenomena-Black.otf') format('opentype'); }` — тоді при експорті PDF шрифти збережуться.
5. **Діаграми:** для складних — проси SVG з Recharts-подібною структурою; для простих — inline SVG з пропорційно розрахованими bars.
