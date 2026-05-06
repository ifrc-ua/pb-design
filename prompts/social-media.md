# Промпти для соцмереж

Готові промпти для створення постів у Facebook, Instagram, Threads про історичні дані БУ Івано-Франківська. Формати: **1:1** (1080×1080), **4:5** (1080×1350), **9:16 Stories** (1080×1920).

Усі промпти передбачають, що агент має доступ до [design.md](../design.md).

---

## 1. Пост-факт «велике число» (1:1)

```
Create a square 1080×1080 social post.

Layout (centered composition):
- Background #FDFDFD
- Top-right corner decorative shape: quarter-circle in #F6F4FB radius 480px, subtle
- Big display number centered vertically at ~40% from top: "{14 832}" in Phenomena Black 240px, color #654EA3, tabular-nums
- Below number: contextual line in Proxima Nova 40px 600, color #1A1A1A, max 2 lines, e.g. "голоси за двір на Галицькій"
- Below that: small meta line in Proxima Nova 22px 400 color #71737E: "{2019, проєкт-переможець}"
- Bottom area:
  - Yellow pill badge bottom-center: "ПЕРЕМОЖЕЦЬ РОКУ" bg #FFEC08 text #1A1A1A, Proxima Nova 16px 700 uppercase letter-spacing +1px, dark 1px border
- Bottom-left 48px margin: logo "Бюджет участі ІФ" lockup, 28px height
- Bottom-right 48px margin: URL "pb.if.ua" in Proxima Nova 16px 500 color #71737E

Overall padding 80px (keep safe zone for IG grid crop).
```

---

## 2. Пост-інсайт з мікрографікою (4:5)

```
Create a vertical 1080×1350 post for Instagram.

Top section (400px):
- Hook headline in Phenomena 52px 700, color #1A1A1A, left-aligned, max-width 920px, 3 lines
  Example: "За 10 років екологія обігнала дороги втричі"
- Left margin 80px

Middle section (550px):
- A mini streamgraph or 2-bar comparison, title above ("2016 vs 2026"):
  - Two grouped bars per year (exemplifying two categories)
  - Colored per data-viz palette
  - Y-axis removed; values shown directly above/inside bars in Phenomena 28px 700 tabular-nums
- Max chart height 440px

Bottom section (400px):
- Key takeaway paragraph in Proxima Nova 26px 400 color #3F4049, max 4 lines
- Hashtags row: Proxima Nova 20px 500 color #654EA3, e.g. "#БюджетУчасті #ІваноФранківськ #10роківзмін"
- Logo bottom-left, URL bottom-right

Background #FDFDFD. Add a very subtle 3px #FFEC08 horizontal line between sections.
```

---

## 3. Story 9:16 — провокативне питання

```
Create a 1080×1920 vertical Story.

Background: gradient from #FDFDFD (top) to #F6F4FB (bottom), or flat #FDFDFD.

Top (safe zone starts at 250px from top):
- Small overline "ПИТАННЯ ДНЯ" in Proxima Nova 28px 600 uppercase letter-spacing +2px color #654EA3

Middle (centered):
- Large question in Phenomena 80px 700, color #1A1A1A, max 4 lines, leading 1.05
  Example: "Хто голосує активніше — Пасічна чи Каскад?"

Answer reveal block (bottom, ~400px above bottom safe zone):
- Split bar: 2 horizontal bars, one per district
  - District 1: bar width proportional, fill `{colors.primary-500}`, label Phenomena 36px 700 with count
  - District 2: fill `{colors.primary-300}`, same style
- Winner district gets a small yellow star icon next to name
<!-- TODO: design-data.md may define a canonical district palette; until then, derive contrast from primary shades (primary-500 vs primary-300) — never invent district HEX values. -->

Footer (last 200px):
- "Дивись усі райони →" CTA — Proxima Nova 24px 600 color #654EA3 with arrow
- Logo 40px centered
```

---

## 4. Пост-карусель «Рік в цифрах» (4:5, 5 слайдів)

Спільні правила для карусельних слайдів:
- Розмір 1080×1350
- Bg #FDFDFD
- На кожному слайді маленький лічильник угорі "{1}/5" у Proxima Nova 18px 600 #71737E
- Внизу праворуч стрілка "→" 32px для навігації
- Єдиний футер: logo + "pb.if.ua"

```
SLIDE 1 (cover):
- Phenomena 88px 900 centered: "{2023} у цифрах"
- Subtitle Proxima Nova 26px 400 color #71737E: "Бюджет участі Івано-Франківська"
- Background: subtle purple dotted pattern (#EEEAF7 dots 4px, 24px grid, opacity 40%)
- Bottom-center yellow pill "ЛИСТАЙ →"

SLIDE 2 (key stat):
- "{187}" in Phenomena Black 280px color #654EA3 tabular-nums, centered
- "поданих проєктів" Proxima Nova 40px 500 below
- "рекорд за 8 років" small annotation in pill #FFF9B3 with 1px border #E6D307

SLIDE 3 (category breakdown):
- Title: "Куди йшли голоси" Phenomena 48px 700
- Donut chart 600×600 centered (style per infographics.md #4)
- Legend below in 2 rows

SLIDE 4 (winner):
- Project photo large (radius 24px) top 60%
- Winner info below: title + author + district + "3 421 голос"
- Yellow "ПЕРЕМОЖЕЦЬ" pill overlaid top-right of photo

SLIDE 5 (CTA):
- "Дослідити всі 10 років →" Phenomena 64px 700 color #654EA3
- URL "pb.if.ua" large, Proxima Nova 36px 600
- Subtle arrow animation hint
```

---

## 5. Пост-перемога (1:1) — святковий

```
Create a 1080×1080 celebratory post for a realized project.

Layout:
- Full-bleed project photo as background, with overlay: bottom 60% darkened with linear-gradient from transparent to rgba(26,26,26,0.75)
- Top-right corner: yellow "РЕАЛІЗОВАНО {2021}" pill bg #FFEC08 text #1A1A1A Proxima Nova 20px 700 uppercase
- Bottom text block (white on darkened gradient):
  - Project title Phenomena 56px 700 color #FDFDFD, max 3 lines
  - Meta line Proxima Nova 20px 500 color rgba(253,253,253,0.8): "{автор}, {район}, {категорія}"
  - Stats row: "₴{1.2 МЛН}" and "{2 847} ГОЛОСІВ" in Phenomena 32px 900 color #FFEC08, Proxima Nova 14px 600 uppercase labels below
- Logo bottom-left corner 40px, white version
```

---

## 6. Story 9:16 — календар реалізації

```
Create 1080×1920 Story showing timeline of project implementation.

Title top (safe zone start):
- "Від ідеї до реалізації" Phenomena 56px 700 color #1A1A1A
- Subtitle Proxima Nova 24px 400 color #71737E: "Проєкт «{Дитячий майданчик на Галицькій}»"

Middle — vertical timeline:
- Left vertical line 3px #EFEFF1 at x=140
- 4 dots (16px, filled #654EA3) with right-side cards:
  1. "Листопад 2019" + "Подача заявки"
  2. "Січень 2020" + "Голосування — 2 847 голосів"
  3. "Травень 2020" + "Старт робіт"
  4. "Вересень 2020" + "Відкриття" — this dot is yellow #FFEC08 with 2px dark stroke
- Each card: Proxima Nova 22px 600 for date, 26px 500 for event text
- Between dots: thin 1px vertical line same color

Bottom CTA: "Дізнатися історію на сайті →" Proxima Nova 24px 600 color #654EA3
Logo + URL bottom-center.
```

---

## 7. Пост-порівняння «До / Після» (1:1)

```
Create 1080×1080 before/after post.

Layout: 50/50 vertical split.
Left half: "ДО" photo (before) with "ДО" label bottom-left in Phenomena 28px 700 white on semi-dark pill
Right half: "ПІСЛЯ" photo (after) with "ПІСЛЯ" label, same style but pill bg #FFEC08 text #1A1A1A

Top overlay (both sides):
- Thin yellow strip 8px #FFEC08 at very top

Bottom overlay (both sides, full width, bg #1A1A1A opacity 0.8):
- Project name Phenomena 32px 700 color #FDFDFD
- Meta: "{рік реалізації}, {район}" Proxima Nova 16px 500 color rgba(253,253,253,0.7)
- Budget: "₴{1.2 млн}" Phenomena 24px 900 color #FFEC08, right-aligned
```

---

## 8. Пост-рейтинг «Активні райони» (4:5)

```
Create 1080×1350 post: district activity ranking.

Title top:
- "Топ-5 районів за 10 років" Phenomena 52px 700
- Subtitle Proxima Nova 22px 400 #71737E: "За кількістю поданих проєктів"

List (5 rows, each 180px tall):
- Rank number left, 72px width, Phenomena 88px 900, colors:
  - #1 yellow #FFEC08 with dark 2px stroke
  - #2–3 #654EA3
  - #4–5 #9C8BCC
- District name + project count, vertical:
  - Name Phenomena 36px 700
  - Count Phenomena 28px 900 #654EA3 tabular-nums + "проєктів" Proxima Nova 18px 500 #71737E
- Horizontal bar fill showing relative count (full width minus 60px), Primary-500 for #1, Primary-300 for others

Bottom CTA: "Детально за роками →" + URL
Logo bottom-left.
```

---

## Підказки

1. **Кольорова консистентність** — завжди кажіть «use ONLY design system colors».
2. **Шрифти** — якщо генератор зображень не має Phenomena/Proxima Nova, просіть «use closest fallback: Inter Tight for display, Inter for body».
3. **Контраст** — на ілюстраціях з білим фоном жовтий ЗАВЖДИ з темним контуром/рамкою.
4. **Safe zones** — для Stories залишайте 250px зверху і 450px знизу порожніми (місце для UI Instagram).
5. **Carousels** — мінімум 3, максимум 10 слайдів. Оптимум — 5.
6. **Мова** — завжди українська, з правильним відмінюванням цифр («1 проєкт, 2 проєкти, 5 проєктів»).
