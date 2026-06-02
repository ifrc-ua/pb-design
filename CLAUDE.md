# CLAUDE.md

Guidance for AI agents (Claude Code, Cursor, etc.) working in this repo.

## What this repo is

A design system for **Participatory Budget of Ivano-Frankivsk** (Бюджет участі Івано-Франківськ), written in the [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) format, a plain-markdown spec that AI agents read to generate on-brand UI, infographics, and analytical visualizations.

This is **not a codebase**. There is no build, no tests, no runtime. The deliverables are markdown files that other agents consume.

## Primary artifacts

**[design.md](./design.md)**: single source of truth for the design **system** (colors, typography, components, rules).

**[design-data.md](./design-data.md)**: single source of truth for the **data layer** (real PB categories per year 2016–2026, canonical category palette, project statuses, map tokens).

External projects reference both via raw GitHub URL. Both files have a Ukrainian counterpart (`design.ua.md`, `design-data.ua.md`) which must be kept in lockstep.

- Do not rename or move these files.
- Preserve heading anchors when editing, external prompts may link to specific sections.
- Structural rewrites need explicit user approval. Small edits (values, wording, new rows in tables) are fine.

## Language

- Respond to the user in **Ukrainian**: that is their working language.
- Ensure the primary `design.md` file remains in **English** for maximum AI understanding.
- Keep the localized copy `design.ua.md` in **Ukrainian**.
- Edit the English file first, then mirror the change into its `.ua.md` twin in the same commit (see «Pre-commit consistency checklist»).
- Meta-documentation for agents (this file) stays in English.

## Repo layout

```
design.md           ← main design system (do not restructure lightly)
design.ua.md        ← Ukrainian copy of design.md (keep in lockstep)
design-data.md      ← real PB categories/statuses/map tokens (data layer)
design-data.ua.md   ← Ukrainian copy of design-data.md (keep in lockstep)
README.md           ← human-facing intro (English)
README.ua.md        ← human-facing intro (Ukrainian)
LICENSE             ← MIT
prompts/            ← ready-made prompts for typical tasks
  infographics.md       ← analytical infographics, charts, maps
  social-media.md       ← Instagram/Facebook posts, stories, carousels
  presentations.md      ← 16:9 deck slides
  render-examples.md    ← self-contained prompts for AI tool comparison
assets/             ← cover images + AI-generated reference renders
  pb_photo.png / pb_photo_ua.png  ← README covers
  Claude-opus-4.7/  ← reference renders + per-folder README
  Gemini-3.1-pro/
  v0-max/
fonts/              ← (NOT in repo, gitignored) licensed fonts for local use; download per README
```

## Conventions

- **New prompts** go in `prompts/` as a new `.md` file, following the structure of existing ones.
- **Do not create** new top-level docs (extra READMEs, CHANGELOG, CONTRIBUTING, etc.) unless the user asks. If `design-data.md` lacks a needed category/status/map token, extend that file (and its `.ua.md` twin) rather than fabricating values; leave a `<!-- TODO: design-data.md needs X -->` comment in any artifact when a gap remains.
- **Do not touch `fonts/`**: files there are licensed (Proxima Nova, Phenomena) and governed by an org-level agreement.
- **Brand colors are fixed**: purple `#654EA3` + yellow `#FFEC08` on near-white `#FDFDFD` with graphite `#1A1A1A` text. Shades and semantic tokens are defined in `design.md` §2, reuse them, don't invent new ones.

## Local fonts (use them when rendering)

The real brand fonts are on disk at `fonts/Phenomena/` (7 weights) and `fonts/Proxima-Nova/` (13 weights incl. italics), **use these whenever you render anything locally** (HTML/CSS `@font-face` via relative path, matplotlib `font_manager.fontManager.addfont()`, Pillow/Cairo `ImageFont.truetype("fonts/Phenomena/Phenomena-Black.otf", size)`, Playwright/Puppeteer, Inkscape, etc.). Prefer them over the Inter Tight / Inter fallbacks documented in `design.md` §3, those fallbacks exist only for external tools (Lovable, v0, Stitch, Canva, GitHub raw-URL flow) that cannot reach this filesystem. The folder is gitignored; never commit `.otf`/`.ttf`/`.woff` files.

## Versioning (YAML frontmatter)

Both `design.md` and `design-data.md` carry a `version: X.Y.Z` field that follows semver. Bump it whenever the file (or its `.ua.md` twin) changes, git log alone is too noisy for downstream consumers.

- **MAJOR** (`1.0.0` → `2.0.0`), token removed or renamed; component contract changed; canonical category color/icon changed; breaking rule reversed. Anything that *breaks* an existing artifact downstream.
- **MINOR** (`1.0.0` → `1.1.0`), new token; new component; new rule; new prompt file; new responsive breakpoint; new canonical category or status; new map token. Additive, non-breaking.
- **PATCH** (`1.0.0` → `1.0.1`), wording, comments, typos, clarifications, table cell edits that do not change values. Pure cosmetics.

Each file's English and Ukrainian copies (e.g. `design.md` ↔ `design.ua.md`) must always carry the same version number, bumped in the same commit. `design.md` and `design-data.md` version independently of each other.

On every version bump, create and push the matching git tag: `design-vX.Y.Z` for the design system, `data-vX.Y.Z` for the data layer. The README tells downstream users to pin to the newest tag, so a missing tag silently strands them on an older release.

## Pre-commit consistency checklist (twin files)

A manual gate (no script) to run before committing any change to `design.md`, `design-data.md`, or their `.ua.md` twins. It catches the EN/UA drift and stale-tag mistakes.

1. **English first.** Edit the English file (`design.md` / `design-data.md`), then mirror the same change into its `.ua.md` twin in the **same commit**. English is canonical; Ukrainian is the localized copy.
2. **Version parity.** After the edit, the English file and its Ukrainian twin carry the **same** `version:`.
3. **Bump on change.** If a file's content changed at all, its `version:` was bumped per the MAJOR/MINOR/PATCH rules above (and `updated:`, where present, is today's date).
4. **Section parity.** The set of headings/anchors is identical across the two twins. External prompts deep-link to anchors, so a section added or renamed in one must appear in the other.
5. **Tag on bump.** Every version bump has its matching tag (`design-vX.Y.Z` / `data-vX.Y.Z`) created and pushed in the same push. A bumped version with no pushed tag silently strands downstream consumers.

`design.md` and `design-data.md` version independently: a commit may bump one pair and leave the other untouched, fine, as long as each changed file satisfies 1–5.

## Scope

The system is built for **analytics of 10 years of PB Ivano-Frankivsk across the 2016–2026 timeframe** (PB was not held in 2022, hence 10 cycles within an 11-year span), historical aggregation, not the current voting cycle. When in doubt about tone, favor: restraint, whitespace, big numbers as heroes, muted data-viz palette.
