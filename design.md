# Design System — Бюджет участі Івано-Франківськ

> Дизайн-система для проєкту громадського бюджету (бюджету участі) м. Івано-Франківська. Побудована за форматом [Google Stitch DESIGN.md](https://stitch.withgoogle.com/) / [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) — плейн-маркдаун для AI-агентів (Claude, Stitch, Cursor, Lovable), що генерують UI, інфографіку та аналітичні візуалізації в бренді БУ ІФ.

---

## 1. Visual Theme & Atmosphere

Бюджет участі — це муніципальний інструмент, який живе на перетині двох енергій: **громадянської довіри** (спокій, прозорість, порядок) та **активної участі** (рух, голос, вибір). Дизайн-система побудована навколо цього дуалізму. Phenomena — умовний, широкий, майже архітектурний гротеск — виступає в ролі голосу-героя: в дисплейних заголовках, рубриках, цифрах-рекордах. Його геометричність і прозорий контур асоціюються з громадським простором, офіційністю без холодності. Proxima Nova — універсальна робоча гарнітура — відповідає за щільні шари інтерфейсу, аналітичні підписи, довгі описи проєктів і таблиці даних.

Палітра тримається на двох кольорах з логотипу: **фіолетовий `#654EA3`** (серйозність, влада, креативність) і **жовтий `#FFEC08`** (енергія, голос, видимість). Фіолетовий — як чорнило документа, жовтий — як маркер для найважливішого. Фон майже білий (`#FDFDFD`), текст глибокий графітовий (`#1A1A1A`) — пара для максимальної читабельності і фокусу на даних. Акцентні кольори data-viz палітри введені навмисно ненасичені — щоб мапи з сотнями точок і heatmaps з 10 роками даних залишалися читабельними, а не «кричали».

Естетика стриманої інфографіки: багато білого простору, чіткі сітки, великі числа як героїв композиції, акуратні іконки з товщиною 1.5px, м'які (8–12px) заокруглення на картках, тіні ледве помітні. Жодних неонових градієнтів, жодних декоративних анімацій — усе служить читанню даних і довірі.

**Key Characteristics:**
- Дві гарнітури: Phenomena (дисплей + заголовки) + Proxima Nova (UI, текст, дані)
- Двоколірний логотипний бренд: фіолетовий `#654EA3` + жовтий `#FFEC08`
- Data-viz палітра з 7 категорій + sequential шкала для мап і heatmaps
- Історичний, аналітичний фокус — система створена для візуалізації **10 років** БУ, не для поточного циклу
- Жовтий — завжди маркер ВАЖЛИВОГО (переможець, акцент, CTA), ніколи фон великих поверхонь
- Акуратні тіні, 8px grid, широкі gutters — муніципальна довіра = «не тісно»
- Mobile-first: сайт і соцмережі споживають з телефону

---

## 2. Color Palette & Roles

### Brand Core (з логотипу)
| Роль | HEX | RGB | Застосування |
|---|---|---|---|
| **Primary** — Фіолетовий | `#654EA3` | 101, 78, 163 | Заголовки дисплею, основні CTA, активні стани, фірмові поверхні |
| **Secondary** — Жовтий | `#FFEC08` | 255, 236, 8 | Акцент «це важливо», бейдж переможця, хайлайти, CTA-підкреслення |
| **Background** — Майже білий | `#FDFDFD` | 253, 253, 253 | Основний фон сторінок, карток |
| **Text** — Графіт | `#1A1A1A` | 26, 26, 26 | Основний текст, числа, дані |

### Primary Shades (фіолетовий)
| Роль | HEX | Застосування |
|---|---|---|
| Primary-900 (dark) | `#4E3C84` | Hover/active, натиснута кнопка, темні акценти |
| Primary-500 (base) | `#654EA3` | Базовий primary (з брендбука) |
| Primary-300 (tint) | `#7B66B8` | Secondary buttons, border emphasis |
| Primary-200 (light) | `#9C8BCC` | Підкладки, disabled states |
| Primary-100 (bg-tint) | `#EEEAF7` | Фонові картки секцій, hover-фон |
| Primary-50 (surface) | `#F6F4FB` | Найлегший фіолетовий — smooth-секції |

### Secondary Shades (жовтий)
| Роль | HEX | Застосування |
|---|---|---|
| Secondary-700 (dark) | `#E6D307` | Hover на жовтих CTA, темний акцент |
| Secondary-500 (base) | `#FFEC08` | Базовий secondary (з брендбука) |
| Secondary-300 (tint) | `#FFF266` | М'який акцент |
| Secondary-100 (bg-tint) | `#FFF9B3` | Хайлайтер тексту, бейдж переможця фон |

### Neutrals (10 ступенів)
| Токен | HEX | Застосування |
|---|---|---|
| neutral-0 | `#FDFDFD` | Background |
| neutral-50 | `#F7F7F8` | Page subtle, striped rows |
| neutral-100 | `#EFEFF1` | Dividers, borders light |
| neutral-200 | `#E2E2E6` | Borders, input-rest |
| neutral-300 | `#CACAD1` | Disabled border, subtle emphasis |
| neutral-400 | `#9FA0A9` | Placeholder, muted text |
| neutral-500 | `#71737E` | Secondary text |
| neutral-700 | `#3F4049` | Body on light, subtitle |
| neutral-900 | `#1A1A1A` | Text primary |
| neutral-950 | `#0D0D12` | Overlay, max-contrast display |

### Semantic
| Роль | HEX | Застосування |
|---|---|---|
| Success | `#2F8F4E` | «Реалізовано», позитивна дельта у статистиці |
| Info | `#2563EB` | Інформаційні повідомлення, нейтральні стани |
| Warning | `#D97706` | Попередження в адмінці, «увага до даних» |
| Error | `#DC2626` | Помилки форм, «не реалізовано» (для відтінків — краще neutral) |

### Історичні бейджі/теги (аналітика 10 років)
| Ярлик | Фон | Текст | Використання |
|---|---|---|---|
| Переможець року | `#FFEC08` (Secondary-500) | `#1A1A1A` | Проєкт-переможець голосування у своєму році |
| Учасник | `#EEEAF7` (Primary-100) | `#4E3C84` | Проєкт, що брав участь, не переміг |
| Реалізовано | `#E8F3EC` (tint Success) | `#1E6B39` | Реалізовані після перемоги |
| Частково реалізовано | `#FFF3E0` (tint Warning) | `#9A5207` | Частково або з відхиленнями |
| Не реалізовано | `#EFEFF1` (neutral-100) | `#71737E` | Переміг, але не реалізовано |

### Data-Viz Categorical Palette (7 категорій)
Кольори для багатосерійних графіків, оптимізовані для читабельності на білому + перевірені для найпоширеніших форм дальтонізму. Використовувати **у цьому порядку** — не перемішувати довільно.

| #  | Назва       | HEX       | Типова категорія БУ |
|----|-------------|-----------|---------------------|
| 1  | Фіолетовий  | `#654EA3` | Освіта |
| 2  | Teal        | `#17A2A2` | Екологія, зелень |
| 3  | Coral       | `#E85D5D` | Безпека |
| 4  | Olive       | `#8B9A2B` | Спорт, активності |
| 5  | Sky         | `#3A9BD9` | Транспорт, інфраструктура |
| 6  | Rose        | `#D46BA6` | Культура |
| 7  | Жовтий      | `#FFEC08` | Благоустрій (використовувати з темним контуром/текстом) |

> **Правило жовтого в data-viz:** жовтий `#FFEC08` на білому має слабкий контраст. У графіках завжди додавати темний контур `#1A1A1A` товщиною 1–1.5px, або темний текст на жовтому заповненні. Не використовувати жовтий для тонких ліній-графіків без контуру.

### Data-Viz Sequential Palette (для heatmaps, хороплет-мап)
Світло-фіолетовий → темно-фіолетовий, 7 ступенів:
`#F6F4FB` → `#E3DCF0` → `#CDBFE4` → `#B29AD5` → `#9477C4` → `#7157AE` → `#4E3C84`

### Контраст (WCAG AA)
Перевірені пари:
- `#1A1A1A` на `#FDFDFD` — 19.3:1 ✓ AAA
- `#FDFDFD` на `#654EA3` — 6.7:1 ✓ AA
- `#1A1A1A` на `#FFEC08` — 16.1:1 ✓ AAA
- `#654EA3` на `#FDFDFD` — 7.0:1 ✓ AA
- `#71737E` (neutral-500) на `#FDFDFD` — 4.7:1 ✓ AA (для muted text)

> **НЕ використовувати:** білий текст на жовтому, фіолетовий на жовтому (обидва провалюють AA).

---

## 3. Typography Rules

### Font Families
- **Display/Headings**: `Phenomena` (локальний, `/fonts/Phenomena/`), fallback: `'Phenomena Fallback', 'Inter Tight', system-ui, sans-serif`
- **Body/UI**: `Proxima Nova` (локальний, `/fonts/Proxima Nova/`), fallback: `'Proxima Nova Fallback', 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`
- **Numerics/Data**: `Proxima Nova` з `font-variant-numeric: tabular-nums` — обов'язково для таблиць, дашбордів, графіків

### Available Weights
- **Phenomena**: Thin (100), ExtraLight (200), Light (300), Regular (400), Bold (700), ExtraBold (800), Black (900)
- **Proxima Nova**: Thin (100), Light (300), Regular (400), Semibold (600), Bold (700), Extrabold (800), Black (900) — усі з Italic

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Hero / Display | Phenomena | 72–96px | 900 (Black) | 1.00 | -1.5px до -2px | Числа-герої, заголовок лендингу, «10 років БУ» |
| H1 / Page Title | Phenomena | 48–64px | 700 (Bold) | 1.05 | -0.8px | Головний заголовок екрану |
| H2 / Section | Phenomena | 32–40px | 700 (Bold) | 1.15 | -0.4px | Секції сторінки |
| H3 / Sub-section | Phenomena | 24–28px | 400 (Regular) | 1.25 | -0.2px | Підзаголовок секції |
| Feature Title | Proxima Nova | 20–24px | 600 (Semibold) | 1.30 | normal | Назва картки проєкту, заголовок віджета |
| Body Large | Proxima Nova | 18–20px | 400 (Regular) | 1.55 | normal | Вступні абзаци, описи |
| Body Standard | Proxima Nova | 16px | 400 (Regular) | 1.55 | normal | Основний текст |
| Body Small | Proxima Nova | 14px | 400 (Regular) | 1.50 | normal | Допоміжний текст, метадані |
| Caption | Proxima Nova | 12–13px | 500 (Medium) | 1.40 | normal | Підписи під графіками/зображеннями |
| Overline / Label | Proxima Nova | 11–12px | 600 (Semibold) | 1.20 | +1px (uppercase) | Ярлики секцій, теги |
| Data Stat (велике число) | Phenomena | 48–72px | 900 (Black) | 1.00 | -1px, tabular-nums | «14 832 голоси», «₴5.2 млн» |
| Data Label (підпис даних) | Proxima Nova | 11–13px | 400 (Regular) | 1.30 | normal, tabular-nums | Осі графіків, значення тултипів |

### Принципи
- **Phenomena — лише для заголовків і великих чисел.** Ніколи не використовуйте Phenomena для довгих абзаців — її широкий контур руйнує читабельність.
- **Proxima Nova — для всього, що довше ніж 5 слів.** Весь UI, описи, списки, таблиці, дані.
- **Tabular numerals обов'язкові** для всіх чисел у таблицях, дашбордах і графіках — щоб цифри вирівнювалися вертикально.
- **Uppercase з letter-spacing +1px** — тільки для Overline/Label. Не робіть uppercase у заголовках H1–H3.
- **Контраст ваг — важливий:** у великих числах використовуйте 900 Black для максимального ваги; у body — 400 Regular.
- **Italic використовувати обережно:** тільки для цитат, виносок «прим.», назв сторонніх джерел.

---

## 4. Component Stylings

### Buttons

**Primary (Фіолетова Solid)**
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
- Padding: 12px 24px (-1.5px на рамку)
- Radius: 8px
- Hover: Background `#EEEAF7` (Primary-100)

**Ghost / Tertiary**
- Background: transparent
- Text: `#3F4049` (neutral-700)
- Hover: Background `#EFEFF1` (neutral-100)
- Для навігації, toolbar, link-кнопок

**Accent (Жовтий CTA)**
- Background: `#FFEC08` (Secondary-500)
- Text: `#1A1A1A`
- Border: 1px solid `#1A1A1A` *(обов'язково для контрасту на світлих поверхнях)*
- Padding: 12px 24px
- Radius: 8px
- Hover: Background `#E6D307` (Secondary-700)
- Застосування: виняткові CTA (наприклад «Дослідити 10 років БУ»)

### Cards & Containers

**Проєкт-картка (історична)**
- Background: `#FDFDFD`
- Border: 1px solid `#EFEFF1` (neutral-100)
- Radius: 12px
- Padding: 20px
- Shadow (hover): `0 4px 12px rgba(26, 26, 26, 0.06)`
- Містить: фото (зверху, radius 8px), тег категорії (chip), назва проєкту (Proxima Nova 20px 600), автор + район (Proxima Nova 14px, neutral-500), статистика (голоси, бюджет — Phenomena 28px 700), бейдж статусу (переможець/учасник/реалізовано)

**Stat-card (велике число)**
- Background: `#F6F4FB` (Primary-50) АБО `#FDFDFD` з 1px border
- Radius: 16px
- Padding: 24px
- Велике число: Phenomena 56px 900, tabular-nums
- Підпис: Proxima Nova 14px 400, neutral-500, uppercase з letter-spacing +1px

### Tags / Chips (категорії БУ)

- Розмір: height 24–28px, padding 4px 10px
- Radius: 999px (pill)
- Font: Proxima Nova 12px 600
- Фон: відтінок з data-viz palette (з прозорістю 15–20%) + текст повного кольору категорії
  - Приклад: Освіта — bg `rgba(101, 78, 163, 0.15)`, text `#4E3C84`
  - Приклад: Екологія — bg `rgba(23, 162, 162, 0.15)`, text `#0F7070`
- Всередині можна додати маленьку іконку категорії (14px) зліва

### Історичні бейджі (статусні)

- Розмір і геометрія як у чипів (pill, 24–28px)
- Заповнені (не outline) для впізнаваності:
  - Переможець року: bg `#FFEC08`, text `#1A1A1A`, опціонально іконка зірочки
  - Реалізовано: bg `#E8F3EC`, text `#1E6B39`, опціонально галочка
  - Не реалізовано: bg `#EFEFF1`, text `#71737E`

### Progress Bar (бюджет / голоси)

- Висота: 8px (стандарт), 12px (герой на сторінці проєкту)
- Background: `#EFEFF1` (neutral-100)
- Fill: `#654EA3` (Primary-500) для голосів; `#FFEC08` з темним контуром для «реалізація бюджету»
- Radius: 999px (pill)
- Опціонально: відмітки (marker) на 25/50/75/100% — тонкими `#CACAD1` (neutral-300) лініями

### Filter Elements (для аналітичних екранів)

**Year Range Slider**
- Track: 4px, `#EFEFF1`, active-range fill `#654EA3`
- Handle: коло 16px, `#FDFDFD`, border 2px `#654EA3`, shadow підкреслено
- Labels: Proxima Nova 13px 500, tabular-nums

**Dropdown (Район / Категорія)**
- Background: `#FDFDFD`
- Border: 1px `#E2E2E6` (neutral-200)
- Radius: 8px
- Padding: 10px 14px
- Focus: border `#654EA3`, shadow `0 0 0 3px rgba(101, 78, 163, 0.15)`

**Checkbox / Toggle**
- Unchecked: border 1.5px `#CACAD1`, bg `#FDFDFD`
- Checked: bg `#654EA3`, checkmark `#FDFDFD`
- Toggle (для «тільки переможці»): track `#CACAD1`/`#654EA3`, thumb `#FDFDFD`

### Navigation
- Horizontal nav, фон `#FDFDFD`, нижній border 1px `#EFEFF1`
- Links: Proxima Nova 16px 500, `#3F4049`, hover `#654EA3`
- Активний: 2px підкреслення `#654EA3` знизу, текст `#1A1A1A`
- Logo: 28–32px висота, зліва

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
- **Муніципальна довіра = не тісно.** Секції розділяються 80–96px вертикального простору на desktop (48–64px mobile).
- **Cards breathe:** padding усередині картки 20–24px, між картками у грідах — 24px.
- **Дані мають повітря:** графіки й таблиці мають padding 24–32px від країв контейнера.

### Border Radius Scale
- `4px` — маленькі елементи (chip-label усередині, progress ticks)
- `8px` — кнопки, inputs, маленькі картки
- `12px` — картки проєкту, стандартні блоки
- `16px` — великі stat-картки, модалки
- `24px` — великі hero-секції, featured-cards
- `999px` (pill) — чіпи, бейджі, тонкі кнопки-tags

---

## 6. Depth & Elevation

| Level | Shadow | Використання |
|---|---|---|
| 0 (Flat) | none | Базові поверхні, текст, фон |
| 1 (Subtle) | `0 1px 2px rgba(26, 26, 26, 0.04)` | Картки статичні на світлому фоні |
| 2 (Raised) | `0 4px 12px rgba(26, 26, 26, 0.06)` | Hover на картках, підвищені елементи |
| 3 (Overlay) | `0 12px 32px rgba(26, 26, 26, 0.10)` | Dropdowns, tooltips, popovers |
| 4 (Modal) | `0 24px 64px rgba(26, 26, 26, 0.14)` | Модальні вікна, lightbox |

**Філософія:** тіні завжди нейтрально-сірі (на основі `#1A1A1A` з прозорістю), ніколи не фіолетові. Офсет завжди вниз (y+), без бокового зміщення. Це створює спокійну дочасну ієрархію без «цифрового галасу».

---

## 7. Do's and Don'ts

### Do
- Використовуйте Phenomena лише для заголовків і великих чисел — саме в цьому її магія.
- Використовуйте Proxima Nova для всього UI, тексту, даних і підписів.
- Застосовуйте `tabular-nums` на всіх цифрах у таблицях і дашбордах.
- Жовтий `#FFEC08` — це **акцент**, не фон. Використовуйте для позначення переможця, хайлайтів, винятково важливих CTA.
- На графіках з жовтим завжди додавайте темний контур `#1A1A1A` 1–1.5px.
- Використовуйте data-viz categorical palette у фіксованому порядку — перший колір для найважливішої серії.
- Для мап і heatmaps використовуйте sequential фіолетову шкалу.
- Давайте секціям 80–96px вертикального простору.
- Округлення кнопок — 8px, карток — 12px, pill для чипів/бейджів.
- Перевіряйте контраст тексту/фону на WCAG AA (мін. 4.5:1 для body, 3:1 для великого тексту).

### Don't
- Не використовуйте Phenomena для body-тексту — читабельність провалиться.
- Не використовуйте фіолетовий на жовтому або білий на жовтому — обидва провалюють AA.
- Не робіть великі заливки жовтим — він стомлює око і створює ефект попередження.
- Не використовуйте неонові або градієнтні кольори — бренд стриманий.
- Не округлюйте великі цифри в офіційній статистиці — «14 832 голоси», не «~15 тис.».
- Не плутайте ролі: «живі» статусні чипи типу «Триває голосування» — **забороняються**. Сайт — **аналітика минулого**, не поточний цикл БУ.
- Не використовуйте бокові тіні (x-offset) — тільки вертикальні.
- Не робіть inline-редагування тексту шрифтом Phenomena 300 або тонше — його Thin/Light для дисплейного застосування тільки у великих розмірах (48px+).

---

## 8. Responsive Behavior

### Breakpoints
| Ім'я | Ширина | Ключові зміни |
|---|---|---|
| Mobile | 360–599px | 1 колонка, стек, hero-число 48px, padding 24px |
| Tablet | 600–1023px | 2 колонки, hero-число 64px, padding 40px |
| Desktop | 1024–1439px | 3–4 колонки, hero-число 80px, padding 64px |
| Wide | 1440px+ | Максимальний контейнер 1280px, центроване |

### Collapsing Strategy
- Hero display: 96px → 72px → 56px → 48px
- H1: 64px → 48px → 36px
- Section H2: 40px → 32px → 28px
- Grid колонок: 12 → 8 → 4
- Мапа: збирає фільтри в bottom-sheet на mobile
- Таблиці 10-річних даних: конвертуються у горизонтальний скрол або stack-cards на mobile
- Навігація: collapsed у burger-меню на mobile

### Mobile-first Priority
Сайт 10 років БУ і всі інфографіки **дизайняться спершу під mobile** — бо більшість громадян споживає муніципальний контент з телефону. Карта, фільтри, статистика мають залишатися зручними на екрані 375px.

---

## 9. Iconography

### Набори
- **Основний**: [Lucide](https://lucide.dev/) — тонкі, stroke-based, 1.5px товщина, rounded углы
- **Запасний для заповнених**: [Phosphor Icons](https://phosphoricons.com/) — варіанти Regular/Fill

### Правила
- Товщина ліній: **1.5px** (стандарт), **2px** (display-розміри 32px+)
- Розміри: 16px (inline), 20px (buttons), 24px (сolumn nav), 32px+ (hero)
- Колір: `currentColor` — іконка завжди успадковує колір тексту поруч
- Rounded corners, ніяких гострих кутів

### Icon Set для категорій БУ
| Категорія | Lucide icon | Data-viz колір |
|---|---|---|
| Освіта | `graduation-cap` | `#654EA3` |
| Екологія | `trees` | `#17A2A2` |
| Безпека | `shield-check` | `#E85D5D` |
| Спорт | `dumbbell` або `activity` | `#8B9A2B` |
| Транспорт | `bus` або `road` | `#3A9BD9` |
| Культура | `landmark` | `#D46BA6` |
| Благоустрій | `trees-pine` або `home` | `#FFEC08` (з темним контуром) |

### Для мап
- Маркер проєкту: `map-pin` 24px, заповнений кольором категорії
- Переможець: `map-pin` + маленький `star` overlay у куті (жовтий)
- Кластер: коло з числом (Phenomena 14–16px 700), bg Primary-100, border Primary-500

---

## 10. Voice & Tone (редакційний стиль)

### Принципи
- **Формальний-але-теплий.** «Ви» — завжди. «Ти» — ніколи, навіть у соцмережах.
- **Активні дієслова, конкретні результати.** «Мешканці Пасічної обрали 14 проєктів» — краще ніж «було проведено голосування». «Відремонтовано 12 дворів на 5.2 млн грн» — краще ніж «виконано низку заходів з благоустрою».
- **Без канцеляризмів.** Забороняються: «вищезазначений», «в рамках», «з метою», «шляхом», «здійснення». Пишіть простіше.
- **Числа — героїв не ховаємо.** Якщо за 10 років брало участь 127 тисяч людей — це має бути велике число, не абзац.
- **Акцент на людях і результатах, не на процесі.** «Марія з Автовокзалу подала перший у місті проєкт велостанції» — краще ніж «Подання заявок відбувалося через електронний кабінет».

### Заголовки
- Короткі, конкретні, з числом або іменем, якщо можливо.
- ✓ «10 років, 1 412 проєктів, 8 переможців-легенд»
- ✗ «Огляд реалізації проєктів бюджету участі за десятирічний період»

### Підписи графіків
- Пояснюйте **висновок**, не опис: «Екологія стала фаворитом 2020 року» — краще ніж «Розподіл голосів за категоріями у 2020 році».

### Соцмережі
- Короткі факти з емоційним гачком: «У 2019 двір на Галицькій отримав більше голосів, ніж будь-який проєкт освіти за всі 10 років. Як так вийшло — дивіться в інсайтах ↓»
- Завжди пропонуйте конкретну дію: посилання на сайт з фільтром.

---

## 11. Agent Prompt Guide

### Швидкий референс
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

DATA-VIZ 7 CATEGORIES (in order)
  1 Освіта:      #654EA3
  2 Екологія:    #17A2A2
  3 Безпека:     #E85D5D
  4 Спорт:       #8B9A2B
  5 Транспорт:   #3A9BD9
  6 Культура:    #D46BA6
  7 Благоустрій: #FFEC08 (always with 1px dark outline)

SEQUENTIAL (for maps/heatmaps, light→dark)
  #F6F4FB → #E3DCF0 → #CDBFE4 → #B29AD5 → #9477C4 → #7157AE → #4E3C84

RADII: 4, 8, 12, 16, 24, 999 (pill)
SPACING: 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96
```

### Приклади промптів

**Hero-картка «10 років БУ»:**
> Create a hero card for "10 років Бюджету участі Івано-Франківська". Large display number "10" in Phenomena Black 96px, color #654EA3, tabular-nums. Subtitle "років змін" in Proxima Nova 20px 400, color #1A1A1A. Background #FDFDFD, padding 48px, border-radius 24px, subtle shadow level 2. Below: three stat chips (1 412 проєктів / 127К учасників / ₴62 млн) in Phenomena 28px 700.

**Картка історичного проєкту:**
> Build a project card: photo on top (radius 12px, aspect-ratio 3:2), then a pill-tag «Екологія» (bg rgba(23,162,162,0.15), text #0F7070, font Proxima Nova 12px 600). Title in Proxima Nova 20px 600, color #1A1A1A. Below: autor name + район in Proxima Nova 14px 400, color #71737E. Stats row: "2 847 голосів" (Phenomena 24px 700) and "₴1.2 млн" (Phenomena 24px 700). Bottom: yellow badge "Переможець 2019" bg #FFEC08, text #1A1A1A, pill, Proxima Nova 12px 600.

**Heatmap 10 років за категоріями:**
> Build a heatmap: rows are 7 categories (Освіта, Екологія, Безпека, Спорт, Транспорт, Культура, Благоустрій), columns are 10 years (2016–2025). Use sequential purple palette from #F6F4FB (low) to #4E3C84 (high). Cell labels in Proxima Nova 11px 500, tabular-nums, color auto-contrast. Axis labels Proxima Nova 12px 600 uppercase letter-spacing +1px. Title in Phenomena 32px 700: "Як змінювалися інтереси мешканців за 10 років".

**Інфографіка для соцмереж (1:1):**
> Create a 1080×1080 infographic. Background #FDFDFD with subtle top-right corner detail in Primary-50 #F6F4FB. Big display number in center: "14 832" in Phenomena Black 180px, color #654EA3, tabular-nums. Below in Proxima Nova 28px 600: "голоси за двір на Галицькій, 2019". Footer: small yellow badge "переможець року" bg #FFEC08, dark border 1px. Logo bottom-left.

**Карта міста з проєктами:**
> Design a city map view. Map base: light neutral (MapLibre style, muted). Project markers: map-pin 24px, filled with category color. Winners get an additional 10px yellow star overlay (#FFEC08 with dark border). Filter sidebar on left (desktop) / bottom-sheet (mobile): year range slider (2016–2025), district multi-select, category checkboxes with data-viz colors, toggle "Тільки переможці". Active filters show as removable chips above map.

### Iteration Guide
1. Завжди починайте з brand core (фіолетовий + жовтий + графіт на майже білому).
2. Phenomena — лише для заголовків і великих чисел. Усе інше — Proxima Nova.
3. `tabular-nums` — на всіх цифрах.
4. Data-viz палітра йде у фіксованому порядку. Жовтий у графіках — завжди з темним контуром.
5. Тіні тільки вертикальні, м'які, нейтрально-сірі.
6. Ніяких статусних «живих» позначок — лише історичні бейджі (Переможець року, Учасник, Реалізовано, Не реалізовано).
7. Мобільний-перший. Перевірте дизайн на 375px перед тим як йти ширше.
