<p align="center">
  <img src="assets/pb_photo_ua.png" alt="Обкладинка Бюджету участі" width="800">
</p>

<p align="center">
  <b>Універсальний стандарт для дизайн-рішень</b>
</p>

<p align="center">
  <a href="./prompts/"><img src="https://img.shields.io/badge/AI--Agent-Ready-2F8F4E" alt="AI Ready"></a>
  <a href="./design.ua.md"><img src="https://img.shields.io/badge/Format-DESIGN.md-654EA3" alt="Format"></a>
  <a href="./design.ua.md"><img src="https://img.shields.io/badge/Language-UA_/_EN-FFEC08?labelColor=1A1A1A" alt="Languages"></a>
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-FFEC08?labelColor=1A1A1A" alt="License"></a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 Read in English</a>
</p>

# Дизайн-система «Бюджет участі Івано-Франківської громади»

Дизайн-система для бюджету участі (громадського бюджету) Івано-Франківської громади у форматі [DESIGN.md](https://github.com/VoltAgent/awesome-design-md) — плейн-маркдаун, який читають AI-агенти (Claude, Stitch, Cursor, Lovable, v0) і генерують UI, інфографіку та аналітичні візуалізації в бренді бюджету участі Івано-Франківська.

## Що тут є

- **[design.md](./design.md)** — головний документ дизайн-системи: кольори, шрифти, компоненти, правила.
- **Шрифти:** [Phenomena](https://www.fontfabric.com/fonts/phenomena/) (заголовки, безкоштовний для використання, але redistribution заборонено) і Proxima Nova (текст/UI, комерційний) — файли не включені до репозиторію і не повинні комітитися.
- **[prompts/](./prompts/)** — готові промпти для типових задач:
  - `infographics.md` — аналітична інфографіка (heatmaps, діаграми голосів, мапи, рейтинги)
  - `social-media.md` — пости для соцмереж (1:1, 4:5, stories 9:16)
  - `presentations.md` — слайди для презентацій мерії/громади

## Як цим користуватися з AI

### Спосіб 1 — дати посилання на raw-файл
Відкрийте чат з Claude (claude.ai, Claude Code, Cursor) і напишіть:

> Використай дизайн-систему з цього документа: https://raw.githubusercontent.com/ifrc-ua/pb-design/main/design.md
>
> Створи [що саме — інфографіку/картку/слайд].

Агент завантажить `design.md` і буде дотримуватися усіх правил — шрифтів, палітри, геометрії.

### Спосіб 2 — скопіювати у свій проєкт
Склонуйте цей репозиторій (або скопіюйте `design.md` у корінь вашого проєкту) і вкажіть AI-інструменту, де його шукати:

- **Claude Code**: створіть `CLAUDE.md` поряд із `design.md` з одним рядком — `Use the design system in design.md for all UI work.` Claude Code автоматично читає `CLAUDE.md` на початку кожної сесії.
- **Cursor**: створіть `.cursorrules` поряд із `design.md` з тим самим рядком. Cursor вставляє `.cursorrules` у кожен промпт.
- **Інші агенти**: більшість приймає system-prompt або «rules» файл — направте його на `design.md` один раз.

Просто покласти `design.md` у папку **недостатньо** — агенту треба сказати дивитися на нього.

### Спосіб 3 — вставити вміст у чат
Відкрийте `design.md`, скопіюйте весь вміст, вставте в чат з інструкцією:

> Ось дизайн-система проєкту. Нижче йде завдання.
>
> [вставити вміст design.md]
>
> Завдання: [ваше завдання]

## Швидкий приклад промпту

> Використай дизайн-систему з https://raw.githubusercontent.com/ifrc-ua/pb-design/main/design.md
>
> Створи інфографіку 1080×1080 для Instagram: топ-5 категорій БУ Івано-Франківська за 10 років (2016–2026, у 2022 БУ не проводився), з кількістю проєктів-переможців у кожній. Стиль: стриманий, дані у центрі уваги, фіолетовий фон-акцент у куті.

## Структура файлів

```text
pb-design/
├── README.md           ← human-facing intro (English)
├── README.ua.md        ← цей файл (українською)
├── CLAUDE.md           ← інструкції для AI-агентів, що працюють у цьому репо
├── LICENSE             ← MIT
├── design.md           ← головна дизайн-система (English) — джерело правди
├── design.ua.md        ← дизайн-система (українською)
├── design-data.md      ← реальні категорії/статуси/мап-токени БУ (English)
├── design-data.ua.md   ← реальні категорії/статуси/мап-токени БУ (українською)
├── prompts/            ← готові промпти для типових задач
│   ├── infographics.md       ← аналітична інфографіка, графіки, мапи
│   ├── social-media.md       ← пости Instagram/Facebook, stories, каруселі
│   ├── presentations.md      ← слайди 16:9 для виступів у мерії
│   └── render-examples.md    ← self-contained промпти для порівняння AI-інструментів
├── assets/             ← обкладинки для README + референс-рендери з AI
│   ├── pb_photo.png / pb_photo_ua.png   ← обкладинки README
│   ├── Claude-opus-4.7/      ← референс-рендери (у кожній папці є власний README)
│   ├── Gemini-3.1-pro/
│   └── v0-max/
└── .gitignore          ← виключає файли ліцензованих шрифтів (.otf/.ttf) з комітів
```

## Бренд у двох словах

- **Кольори:** фіолетовий ![](https://img.shields.io/badge/-%23654EA3-654EA3?labelColor=654EA3) + жовтий ![](https://img.shields.io/badge/-%23FFEC08-FFEC08?labelColor=FFEC08) на майже-білому ![](https://img.shields.io/badge/-%23FDFDFD-FDFDFD?labelColor=FDFDFD), текст ![](https://img.shields.io/badge/-%231A1A1A-1A1A1A?labelColor=1A1A1A).
- **Шрифти:** Phenomena — заголовки й великі числа; Proxima Nova — усе інше.
- **Характер:** муніципальна довіра + енергія громади. Стриманість, ясність, великі числа, багато повітря.
- **Контекст:** аналітика **10 років БУ** Івано-Франківська за період 2016–2026 (у 2022 БУ не проводився). Не поточний цикл.

## Принципи дизайну у двох словах

- **Accessibility-first** — кожна колірна пара у `design.md` перевірена за WCAG AA (≥4.5:1 для основного тексту). Без винятків.
- **Стриманість замість декору** — без градієнтів, неону, паралаксу. Дані — герой; інтерфейс відсувається.
- **AI-parseable + human-readable** — YAML-frontmatter для машин, проза — для пояснення *чому* за кожним правилом. Обидва синхронізовані; YAML — джерело правди при конфлікті.
- **Mobile-first** — спершу проєктуємо на 375px шириною; touch-targets 44×44px; bottom-sheets замість hover-only взаємодій.
- **Статична тиша з одним фірмовим штрихом** — без анімації за замовчуванням; єдиний хореографічний момент — count-up великих чисел при появі у viewport. Завжди поважає `prefers-reduced-motion`.
- **Числа за українською локаллю** — нерозривний пробіл для тисяч (`14 832`), кома для десяткових (`3,7%`), `tabular-nums` скрізь. AI-агенти, які за замовчуванням пишуть `14,832`, виправляються специфікацією.
- **Явне «out of scope»** — dark mode, активне голосування, адмін-UI і форми подачі свідомо не дизайнуються. Реальні дані БУ (категорії, статуси, мап-токени) виокремлені у `design-data.md`; якщо чогось бракує — AI-агенти залишають маркер `<!-- TODO: design-data.md needs X -->` замість того щоб фабрикувати.

## Ліцензія та шрифти

Дизайн-система поширюється за ліцензією [MIT](https://opensource.org/licenses/MIT).

Шрифти **не включені до цього репозиторію** — і не повинні бути додані до нього. Завантажуйте локально для роботи:

- **Phenomena** — безкоштовно для особистого та комерційного використання на [fontfabric.com](https://www.fontfabric.com/fonts/phenomena/) (завантаження через email-форму, 7 накреслень, Thin → Black). Fontfabric Free Fonts EULA **забороняє redistribution** файлів шрифту — не завантажуйте `.otf` / `.ttf` у публічні репозиторії. `@font-face`-вбудовування на власному сайті дозволено.
- **Proxima Nova** — комерційна ліцензія на [Mark Simonson Studio](https://www.marksimonson.com/fonts/view/proxima-nova). Безкоштовної версії немає; redistribution заборонено.

Якщо оригінальні шрифти недоступні, використовуйте такі безкоштовні замінники з Google Fonts (ліцензія OFL):
- Для **Phenomena** (заголовки): [Inter Tight](https://fonts.google.com/specimen/Inter+Tight) (накреслення 900 Black).
- Для **Proxima Nova** (UI і текст): [Inter](https://fonts.google.com/specimen/Inter) (з обов'язковим `tabular-nums` для цифр).
- *Другий резерв:* Geist Sans / Geist Mono.

Детальні інструкції щодо корекції міжлітерного інтервалу та висоти рядка для замінників дивіться у файлі `design.md`.


## Внесення змін

1. Внесіть правки у відповідний файл.
2. `git add . && git commit -m "коротко що змінили"`
3. `git push`

Зміни одразу підхопляться агентами, що посилаються на raw-URL.

---

*Створено на базі шаблону [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) від VoltAgent.*
