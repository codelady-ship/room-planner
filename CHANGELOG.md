# Changelog

All notable changes to this project are documented here.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and the project uses [Semantic Versioning](https://semver.org/).

## [1.1.0] - 2026-11-11

Research-driven features before the Agensi listing (open-skills research, 2026-11-11).

### Added
- **Material quantities:** paint litres, laminate/parquet, tiles with waste, wallpaper rolls, each shown as a one-line calculation (`references/materials-and-checklists.md`).
- **Quote check and contractor checklist:** red flags, 3 itemised quotes, payment tied to finished stages, 10% held until snags are fixed.
- **Measuring guide** and **"will it fit?" check** for lifts, stairs and doors.
- **Renter-friendly mode** (no drilling, reversible changes, landlord's written OK, move-in photos).
- **Moving-in checklist** with often-forgotten items and a buy-by-urgency order.
- Renovation order now marks phases without water or gas, a safe pause point and long-lead items to order early; contingency 15–20% for old buildings.
- `examples/murad-rented-study-bedroom.md`.
- Agensi frontmatter (`version`, `summary`, `tags`, `keywords`, `use_cases`), `scripts/build-agensi-zip.ps1`, `LISTING.md`, evals 4–6 and blind test results in `tests/`.

### Fixed (checked on official pages, 2026-11-11)
- Azerbaijani permits: flat reconstruction and re-planning need a decision of the district executive authority under the Housing Code, Art. 23–24 (30-day decision; unapproved work may have to be undone, Art. 27). Still marked `verify locally`.
- Gas: Azəriqaz (hotline 104) wording; its rules forbid unauthorised gas-line work and replacing or adding gas devices yourself.

### Fixed (blind evals, 2026-11-11)
- ASCII plan scale line now sits above the code block, so every plan line stays under 36 characters and the same length.
- A full plan ends with one next step naming the key `assumed` value, not a list of questions.
- Narrow-kitchen work order (fridge → worktop → sink → worktop → hob) and sizes in SKILL.md.
- "Will it fit?": standing an item on end only helps if its footprint fits the lift floor.
- Lumen example now uses the ×1.25 loss factor from the lighting reference; recount plan lines after drawing.

## [1.0.0] - 2026-11-10

### Added
- First release: ASCII floor plan with clearances, 60-30-10 palettes, three-layer lighting, budget shopping list, renovation order, image prompt, Baku small-flat tips, safety routing. MIT.
