# CLAUDE.md

Guidance for AI agents (Claude Code, Cursor, etc.) working in this repo.

## What this repo is

A design system for **Participatory Budget of Ivano-Frankivsk** (Бюджет участі Івано-Франківськ), written in the [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) format — a plain-markdown spec that AI agents read to generate on-brand UI, infographics, and analytical visualizations.

This is **not a codebase**. There is no build, no tests, no runtime. The deliverables are markdown files that other agents consume.

## Primary artifact

**[design.md](./design.md)** is the single source of truth for the design system (colors, typography, components, rules). External projects reference it via raw GitHub URL, so:

- Do not rename or move `design.md`.
- Preserve heading anchors when editing — external prompts may link to specific sections.
- Structural rewrites need explicit user approval. Small edits (values, wording, new rows in tables) are fine.

## Language

- Respond to the user in **Ukrainian** — that is their working language.
- Ensure the primary `design.md` file remains in **English** for maximum AI understanding.
- Keep the localized copy `design.ua.md` in **Ukrainian**.
- Meta-documentation for agents (this file) stays in English.

## Repo layout

```
design.md           ← main design system (do not restructure lightly)
design-data.md      ← future/optional: created when real data viz is needed
README.md           ← human-facing intro (English)
README.ua.md        ← human-facing intro (Ukrainian)
prompts/            ← ready-made prompts for typical tasks
  infographics.md
  social-media.md
  presentations.md
fonts/              ← licensed commercial fonts — do not modify or redistribute
```

## Conventions

- **New prompts** go in `prompts/` as a new `.md` file, following the structure of existing ones.
- **Do not create** new top-level docs (extra READMEs, CHANGELOG, CONTRIBUTING, etc.) unless the user asks, **with one exception**: you may create `design-data.md` when an analytical artifact demands extended categorical palettes or map data. Leave a `<!-- TODO: design-data.md needs X -->` comment if encountering a gap in the core design.
- **Do not touch `fonts/`** — files there are licensed (Proxima Nova, Phenomena) and governed by an org-level agreement.
- **Brand colors are fixed**: purple `#654EA3` + yellow `#FFEC08` on near-white `#FDFDFD` with graphite `#1A1A1A` text. Shades and semantic tokens are defined in `design.md` §2 — reuse them, don't invent new ones.

## Versioning (`design.md` YAML frontmatter)

The `version: X.Y.Z` field at the top of `design.md` follows semver. Bump it whenever `design.md` or `design.ua.md` changes — git log alone is too noisy for downstream consumers.

- **MAJOR** (`1.0.0` → `2.0.0`) — token removed or renamed; component contract changed; breaking rule reversed (e.g. yellow now allowed as large fill). Anything that *breaks* an existing artifact downstream.
- **MINOR** (`1.0.0` → `1.1.0`) — new token added; new component; new rule; new prompt file; new responsive breakpoint. Additive, non-breaking.
- **PATCH** (`1.0.0` → `1.0.1`) — wording, comments, typos, clarifications, table cell edits that do not change values. Pure cosmetics.

Bump `version` in **both** `design.md` and `design.ua.md` in the same commit. The two files must always carry the same version number.

## Scope

The system is built for **analytics of 10 years of PB Ivano-Frankivsk across the 2016–2026 timeframe** (PB was not held in 2022, hence 10 cycles within an 11-year span) — historical aggregation, not the current voting cycle. When in doubt about tone, favor: restraint, whitespace, big numbers as heroes, muted data-viz palette.
