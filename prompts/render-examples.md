# Render examples — promptи для генерації картинок у `assets/{ai-model}/`

> Для одноразового використання: 5 self-contained промптів, кожен працює без потреби бачити `design.md`/`design-data.md` — всі токени вшиті всередину. Згенеруйте картинки в різних AI, складіть результати у папку `assets/{ai-model}/` (наприклад `assets/Claude-opus-4.7/`) з підписом «згенеровано {AI}» в README цієї папки.

> ⚠️ **Числа в усіх 5 промптах нижче — для дизайн-цілей, не для аналітики.** Значення на кшталт «1 412 проєктів», «127 тис. учасників», «₴62 млн», «24% Шкільні», «2 847 голосів», матриця heatmap — це орієнтовні placeholder'и для перевірки візуального стилю, токенів і композиції. Реальні цифри підставлятимуться з analytics-джерела при production-використанні. У README кожної AI-папки повторити це застереження.

## Як цим користуватися

1. Виберіть промпт нижче.
2. Вставте у чат AI-інструмента (рекомендації для кожного нижче).
3. Збережіть картинку як PNG у відповідну папку `assets/{ai-model}/` (наприклад `assets/Claude-opus-4.7/`) з описовим іменем: `hero-card.png`, `mobile-stats.png`, `donut-2025.png`, `project-card.png`, `heatmap.png`. AI-суфікс не потрібен — він уже у назві батьківської папки.
4. Якщо результат не сподобався — попросіть «refine: tighten spacing» / «сильніше вирівняй» / запустіть в іншому інструменті.

### Які AI пробувати

| AI | Найкраще для |
|---|---|
| **Claude** ([claude.ai](https://claude.ai), Artifacts) | HTML/CSS/SVG-рендери — точне дотримання токенів, копіюйте підсумкову HTML-сторінку, відкривайте в браузері, робіть screenshot |
| **v0** ([v0.dev](https://v0.dev)) | UI-компоненти у React/Tailwind — відмінний для карток, списків, мобільних layout'ів |
| **Gemini** ([gemini.google.com](https://gemini.google.com)) | Альтернативний HTML-рендер; іноді краще для chart-генерації |
| **ChatGPT (GPT-5 / o1)** | HTML/SVG, схоже на Claude; вбудований DALL-E для растрових інфографік (нижча точність токенів — використовуйте для «настрою», не для прецизійних UI) |
| **Stitch / Figma plugins** | Якщо є дизайн-інструмент — краще для production |

Для прецизійного дотримання брендових кольорів і чисел рекомендую **Claude або v0**. ChatGPT-image / DALL-E дають художніше але часто не попадають у точні HEX.

---

## Спільний brief (опційно — деякі AI працюють краще, якщо дати окремо перед промптом)

```
You are generating UI/infographic mockups for "Бюджет участі Івано-Франківська" (Ivano-Frankivsk Participatory Budgeting), a 10-year analytics design system covering 2016-2026 (PB was not held in 2022).

DESIGN TOKENS:
- Brand purple (primary-500): #654EA3
- Brand yellow (secondary-500): #FFEC08 — accent only, NEVER large fill, ALWAYS with #1A1A1A 1.5px outline when used in charts
- Background canvas: #FDFDFD
- Ink (text): #1A1A1A
- Primary shades: primary-50 #F6F4FB, primary-100 #EEEAF7, primary-200 #9C8BCC, primary-300 #7B66B8, primary-500 #654EA3, primary-900 #4E3C84
- Neutrals: neutral-100 #EFEFF1, neutral-200 #E2E2E6, neutral-300 #CACAD1, neutral-500 #71737E, neutral-700 #3F4049, neutral-900 #1A1A1A

FONTS (use Google Fonts CDN — these are FREE substitutes for the commercial originals Phenomena/Proxima Nova):
- Display/Headings: "Inter Tight" weight 900 — use for hero numbers, big titles
- Body/UI: "Inter" weights 400/500/600/700 — everything else
- All digits MUST have: font-variant-numeric: tabular-nums

UKRAINIAN NUMBER FORMATTING (mandatory):
- Thousands: non-breaking space U+00A0. Write "14 832" — never "14,832" or "14832"
- Decimals: comma. Write "3,7%" — never "3.7%"
- Currency: "₴" before number with non-breaking space: "₴1 412", "₴62 млн"

OUTPUT FORMAT: a single HTML file with embedded CSS, ready to open in browser. Inline all SVG. No external dependencies except Google Fonts CDN. Render at the exact pixel dimensions specified — page must fit without scrollbars.
```

---

## Промпт 1 — Hero card «10 років БУ» (desktop 1280×520)

**Best in:** Claude Artifacts, v0, Gemini.

```
Generate a single HTML file rendering a hero stat card at exactly 1280×520 pixels.

The card communicates "10 років Бюджету участі Івано-Франківська" — flagship landing-page block.

Brand tokens (use these exactly, do NOT improvise):
- Background canvas: #FDFDFD
- Brand purple: #654EA3 (use for big numbers)
- Ink/text: #1A1A1A
- Neutral-100 divider: #EFEFF1
- Neutral-500 muted: #71737E
- Primary-50 surface: #F6F4FB

Fonts via Google Fonts CDN:
<link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@900&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
- Display: Inter Tight 900 (substitute for Phenomena Black)
- Body: Inter (substitute for Proxima Nova)

LAYOUT:
- Card: bg #FDFDFD, padding 64px, border-radius 24px, shadow `0 1px 2px rgba(26,26,26,0.04), 0 4px 16px rgba(26,26,26,0.04)`
- Three equal columns separated by thin (1px) #EFEFF1 vertical lines.
- Each column has:
  - Big number: Inter Tight 900, 96px, color #654EA3, font-variant-numeric: tabular-nums
  - 24px gap below
  - Label: Inter 600, 14px, uppercase, letter-spacing +1px, color #71737E

CONTENT (use exactly):
- Column 1 number: "1 412" (with non-breaking space U+00A0 between "1" and "412") | Label: "ПРОЄКТІВ ЗА 10 РОКІВ"
- Column 2 number: "127 тис." (with non-breaking space U+00A0 between "127" and "тис.")  | Label: "УНІКАЛЬНИХ УЧАСНИКІВ"
- Column 3 number: "₴62 млн" (₴ followed by non-breaking space, then "62" + non-breaking space + "млн") | Label: "РЕАЛІЗОВАНО"

Below the card (outside, 16px gap): caption Inter 14px 400 #71737E, centered: "за період 2016–2026 (у 2022 БУ не проводився)" — use en-dash 2016–2026.

The whole thing should render exactly 1280px wide and 520px tall. No scrollbars. Body bg should be #F7F7F8 to make the card stand out slightly.
```

---

## Промпт 2 — Mobile stats screen (375×812)

**Best in:** v0, Claude Artifacts.

```
Generate a single HTML file rendering a mobile screen at exactly 375×812 pixels (iPhone safe area). This is the mobile version of the same "10 років БУ" stats data.

Brand tokens (use exactly):
- Canvas: #FDFDFD
- Page bg: #F7F7F8 (neutral-50)
- Primary-500: #654EA3
- Primary-50 surface: #F6F4FB
- Ink: #1A1A1A
- Neutral-500 muted: #71737E
- Neutral-100 divider: #EFEFF1

Fonts via Google Fonts:
<link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@900&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

LAYOUT (top to bottom inside the 375px viewport):

1. Status bar simulation 44px tall: subtle bg, "9:41" left, signal icons right (you can use simple unicode dots).

2. Header bar 56px: 
   - Left padding 20px: "Бюджет участі ІФ" Inter 17px 600 #1A1A1A
   - Right padding 20px: hamburger icon (3 horizontal lines), 24×24px, touch area 44×44px, color #1A1A1A

3. Hero block, padding 24px horizontal, 32px top:
   - "10 років" Inter Tight 900 56px #654EA3 tabular-nums, line-height 1.0
   - 8px gap
   - "Бюджету участі Івано-Франківська" Inter 18px 500 #71737E, line-height 1.3, max 2 lines

4. 32px gap, then stat cards stacked vertically, 16px gap between:
   Each card: bg #F6F4FB, border-radius 16px, padding 20px, height 96px
   Layout inside card: number left (large), label right (multi-line allowed):
   - Card 1: "1 412" Inter Tight 900 48px #654EA3 tabular-nums + label "проєктів за 10 років" Inter 14px 600 uppercase letter-spacing +0.5px #71737E
   - Card 2: "127 тис." (with non-breaking space U+00A0 between "127" and "тис.") + "учасників"
   - Card 3: "₴62 млн" + "реалізовано"

5. Footer note (after 24px gap): centered, Inter 13px 400 #71737E "у 2022 БУ не проводився"

6. Bottom safe area 34px (iOS gesture line area).

Container width: 375px. All horizontal margins 20-24px. Touch targets 44×44px minimum. Body bg outside the phone frame: a neutral grey #E2E2E6 to suggest device chrome.

Render at exactly 375×812.
```

---

## Промпт 3 — Donut chart «Категорії 2025» (Instagram square 1080×1080)

**Best in:** Claude Artifacts (HTML+SVG), v0.

```
Generate a single HTML file rendering a 1080×1080 Instagram-square infographic with a donut chart of PB category breakdown for year 2025.

Brand tokens:
- Canvas: #FDFDFD
- Subtle corner detail: #F6F4FB (primary-50)
- Ink: #1A1A1A
- Neutral-500 muted: #71737E
- Neutral-100 divider: #EFEFF1

Real PB Ivano-Frankivsk 2025 categories — use these EXACT 9 colors and labels in this exact display order:
1. Шкільні               — #4A2D87
2. Дошкільні             — #7B66B8
3. Позашкільні, профтехосвіта — #9E5FAB
4. Благоустрій           — #2D6BAB
5. Благоустрій малих вулиць — #1A4F82
6. Зелені проєкти        — #3D7C3F
7. Допомога ЗСУ          — #3F4049
8. Доступність           — #0E7C8C
9. Інші проєкти          — #71737E

Sample percentage values (use these exactly, sum = 100%):
1. Шкільні 24%
2. Дошкільні 14%
3. Позашкільні 11%
4. Благоустрій 13%
5. Благоустрій малих вулиць 18%
6. Зелені проєкти 9%
7. Допомога ЗСУ 6%
8. Доступність 3%
9. Інші проєкти 2%

Fonts via Google Fonts:
<link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@900&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

LAYOUT:
- Background #FDFDFD
- Top-right decorative: a quarter-circle of radius 480px in #F6F4FB, anchored to top-right corner (subtle, behind everything else).
- Padding 80px around content.

Top of canvas (y ≈ 80-200):
- Title: "Куди пішли голоси 2025" Inter Tight 900 56px #1A1A1A, left-aligned
- Subtitle below (8px gap): "Розподіл за категоріями" Inter 22px 500 #71737E

Donut chart centered at (540, 580):
- Outer radius 280px, inner radius 180px (donut, not pie)
- 9 segments in the order above, sized by percentage, gap 2px between segments (use stroke="#FDFDFD" stroke-width="2" if SVG path)
- Render as inline SVG paths
- Center label:
  - "187" Inter Tight 900 64px #1A1A1A tabular-nums
  - 8px below: "проєктів-переможців 2025" Inter 16px 500 #71737E

Leader-line callouts around the donut (NOT a bottom legend grid):
- For each segment, place a label OUTSIDE the ring at the segment's mid-angle
- Label format: "{Name} {percentage}%" on a single line — Inter 14px 500 #1A1A1A for the name, Inter 14px 700 #1A1A1A for the percentage (slightly bolder)
- Connector: 1.5px dot at the segment outer edge in the segment color, then a 1px #71737E polyline that travels radially outward ~28px, then bends 90° horizontally toward the label
- Labels on the LEFT half of the donut: right-aligned, baseline aligned with the horizontal line endpoint, ~12px horizontal padding from line to text
- Labels on the RIGHT half: left-aligned, mirror of above
- For small adjacent segments (<5% each), stack labels vertically on the same side with 16px line-height between them; offset the horizontal bend angles so polylines don't overlap
- Center label and footer remain unchanged. Do NOT render any bottom legend grid — labels live entirely on the perimeter.

Footer (y ≈ 1010-1050):
- Left: "Бюджет участі ІФ" Inter 14px 600 #654EA3
- Right: "pb.if.ua" Inter 14px 500 #71737E

CRITICAL: do NOT use yellow #FFEC08 as a segment fill — it's reserved for special accents only. The 9 segment colors are exactly as listed.

Render at exactly 1080×1080.
```

---

## Промпт 4 — Project card 360×480

**Best in:** v0 (UI-картки — їх профіль), Claude Artifacts.

```
Generate a single HTML file rendering one project card at exactly 360×480 pixels. The card shows a historical PB winning project.

Brand tokens:
- Canvas: #FDFDFD
- Border #EFEFF1
- Primary-500: #654EA3
- Education-school category: #4A2D87
- Education-school chip bg: rgba(74, 45, 135, 0.15)
- Ink: #1A1A1A
- Neutral-500 muted: #71737E
- Yellow accent: #FFEC08 (winner badge only)

Fonts via Google Fonts:
<link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@900&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

PROJECT DATA (use exactly):
- Title: "Дитячий майданчик у Хриплині — оновлення, гойдалки, безпечне покриття"
- Author + community: "Ольга Дмитришин · Хриплин"
- Category: "Шкільні" (use icon: a small graduation-cap or school SVG, 14px)
- Votes: 2 847 (with non-breaking space U+00A0)
- Budget: ₴1,2 млн (₴, nbsp, 1, comma, 2, nbsp, "млн")
- Year: 2024
- Winner status: yes

LAYOUT (top to bottom, padding 20px around card):
1. Photo placeholder: 320×216, border-radius 8px. Fill with a subtle linear gradient from #EEEAF7 (top-left) to #CACAD1 (bottom-right). Center label inside: "📷 фото проєкту" Inter 13px 500 color rgba(26,26,26,0.4). 
2. 12px gap.
3. Category chip (pill): height 28px, padding 4px 10px, radius 999px, bg rgba(74, 45, 135, 0.15), text "Шкільні" #4A2D87 Inter 12px 600. Add a 14px school-style icon on the left (use Lucide-style SVG: a graduation cap outline 1.5px stroke #4A2D87).
4. 12px gap.
5. Title: Inter 17px 600 #1A1A1A, line-height 1.3, max 2 lines (use `display: -webkit-box; -webkit-line-clamp: 2;`).
6. 4px gap.
7. Meta: "Ольга Дмитришин · Хриплин" Inter 14px 400 #71737E.
8. 16px gap.
9. Stats row: two equal-width columns separated by 1px #EFEFF1 vertical line:
   - Left: "2 847" Inter Tight 700 28px #1A1A1A tabular-nums, then 4px gap, then "ГОЛОСІВ" Inter 11px 600 uppercase letter-spacing +1px #71737E
   - Right: "₴1,2 млн" Inter Tight 700 28px #1A1A1A tabular-nums, then 4px gap, then "БЮДЖЕТ" same label style
   (700 — not 900 — matches `design.md §4 Project Card` which sets stats at Phenomena 28px **700**; Black/900 is reserved for hero numbers `data-stat` / `display-hero`)
10. 16px gap.
11. Bottom-aligned: Yellow winner badge (pill): bg #FFEC08, border 1px solid #1A1A1A, height 28px, padding 4px 12px, radius 999px. Inside: small star icon (★ or SVG) 14px, then "ПЕРЕМОЖЕЦЬ 2024" Inter 12px 700 uppercase letter-spacing +1px color #1A1A1A.

Card itself: bg #FDFDFD, border 1px solid #EFEFF1, border-radius 12px, total dimensions exactly 360×480 (so internal content area is 320×440 minus paddings).

Body bg outside card: #F7F7F8.

Render at 360×480.
```

---

## Промпт 5 — Heatmap «Категорії × Роки» (desktop 1200×640)

**Best in:** Claude Artifacts (precision SVG), Gemini. (v0 хуже з кастомними grid'ами.)

```
Generate a single HTML file rendering a heatmap at exactly 1200×640 pixels. It shows winning-project counts by PB category × year for Ivano-Frankivsk 2016–2026.

Brand tokens:
- Canvas: #FDFDFD
- Sequential primary scale: #F6F4FB → #EEEAF7 → #9C8BCC → #7B66B8 → #4E3C84
- Inactive cell bg: #EFEFF1, hatch #CACAD1
- Disabled column: #CACAD1
- Ink: #1A1A1A
- Neutral-500 muted: #71737E
- Neutral-700: #3F4049

Fonts:
<link href="https://fonts.googleapis.com/css2?family=Inter+Tight:wght@900&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

GRID:
- 11 rows (categories) × 11 columns (years 2016-2026)
- Cell size: 70×34, gap 2px, radius 4px
- 2022 does NOT appear in the grid — 10 columns only (2021 → 2023 directly)

ROWS (in this exact order, with category color dot 8px before label; row label = Inter 13px 600 #3F4049 right-aligned with 12px gap to grid):
1. Освіта                       (#654EA3)
2. Шкільні                      (#4A2D87)
3. Дошкільні                    (#7B66B8)
4. Позашкільні, профтехосвіта   (#9E5FAB)
5. Благоустрій                  (#2D6BAB)
6. Благоустрій малих вулиць     (#1A4F82)
7. Архітектурна спадщина        (#A0571F)
8. Зелені проєкти               (#3D7C3F)
9. Допомога ЗСУ                 (#3F4049)
10. Доступність                 (#0E7C8C)
11. Інші проєкти                (#71737E)

COLUMNS — exactly 10, NO 2022 COLUMN AT ALL. Axis goes from 2021 directly to 2023:
2016 | 2017 | 2018 | 2019 | 2020 | 2021 | 2023 | 2024 | 2025 | 2026
(Year labels: Inter 12px 600 uppercase letter-spacing +1px #71737E, tabular-nums)
Do NOT add any disabled/greyed 2022 slot. Mention "у 2022 БУ не проводився" only in the chart subtitle.

CELL VALUES — use this matrix exactly (rows in same order as above; "—" means inactive — render as #EFEFF1 with diagonal hatch in #CACAD1, no number):

| Cat \\ Year     | 2016 | 2017 | 2018 | 2019 | 2020 | 2021 | 2023 | 2024 | 2025 | 2026 |
| Освіта         |  —   |  —   |  —   |  7   |  5   |  —   |  4   |  —   |  —   |  —   |
| Шкільні        |  —   |  —   |  —   |  —   |  —   |  —   |  —   |  9   |  11  |  8   |
| Дошкільні      |  —   |  —   |  —   |  —   |  —   |  —   |  —   |  4   |  5   |  6   |
| Позашкільні    |  —   |  —   |  —   |  —   |  —   |  —   |  —   |  3   |  4   |  5   |
| Благоустрій    |  —   |  —   |  —   |  —   |  —   |  —   |  6   |  8   |  10  |  12  |
| Малі вулиці    |  —   |  —   |  —   |  —   |  4   |  5   |  6   |  7   |  8   |  9   |
| Спадщина       |  —   |  —   |  —   |  —   |  —   |  2   |  —   |  —   |  —   |  1   |
| Зелені         |  —   |  —   |  —   |  —   |  —   |  —   |  3   |  —   |  5   |  7   |
| ЗСУ            |  —   |  —   |  —   |  —   |  —   |  —   |  —   |  —   |  4   |  5   |
| Доступність    |  —   |  —   |  —   |  —   |  —   |  —   |  —   |  —   |  2   |  3   |
| Інші проєкти   |  —   |  —   |  —   |  8   |  10  |  —   |  5   |  4   |  4   |  3   |

CELL FILL by value (sequential primary scale):
- 1-2: #EEEAF7 (text color #1A1A1A)
- 3-5: #9C8BCC (text color #1A1A1A)
- 6-9: #7B66B8 (text color #FDFDFD)
- 10+: #4E3C84 (text color #FDFDFD)
- inactive (—): bg #EFEFF1 with 1px diagonal hatch lines #CACAD1, no text

Cell number rendering: Inter 13px 500, tabular-nums, centered.

ABOVE GRID (top of canvas, padding 32px from edges):
- Title: "Як змінювалися інтереси громади, 2016–2026" Inter Tight 900 28px #1A1A1A
- 4px gap
- Subtitle: "Кількість проєктів-переможців у кожній категорії за рік. У 2022 БУ не проводився." Inter 14px 400 #71737E

BELOW GRID (after 24px gap):
- Legend horizontal: 5 colored squares 16×16 with values "0" "1-2" "3-5" "6-9" "10+" labels under each. Inter 12px 500 #3F4049.

Background #FDFDFD. Render at exactly 1200×640.
```

---

## Поради під час генерації

1. **Якщо AI ігнорує точні HEX** і дає «приблизно фіолетовий» — попросіть «strictly use the HEX values from my instructions, do not approximate». 
2. **Якщо AI вставляє ваги Phenomena/Proxima Nova** замість Inter Tight/Inter — нагадайте: «use only Google Fonts CDN — Inter Tight + Inter, no commercial font names».
3. **Якщо число «1 412» рендериться як «1,412»** — попросіть «use a literal non-breaking space U+00A0 between thousands; never use comma as thousand separator».
4. **Якщо результат у Claude Artifacts** — натисніть «Open in browser», зробіть screenshot з DevTools у точному розмірі (Ctrl+Shift+M → Custom dimensions).
5. **Для v0** — після генерації в'ю, експортуйте у Figma або зробіть screenshot Chrome DevTools у device mode.

Після того, як зберете 4–5 картинок у відповідну папку `assets/{ai-model}/`, створимо там `README.md` з підписами (див. існуючі приклади: [`assets/Claude-opus-4.7/README.md`](../assets/Claude-opus-4.7/README.md), [`assets/Gemini-3.1-pro/README.md`](../assets/Gemini-3.1-pro/README.md), [`assets/v0-max/README.md`](../assets/v0-max/README.md)).
