# Agensi listing: Room Planner

DRAFT. Nothing has been submitted. The owner pastes these fields into agensi.io/dashboard/submit herself.

| | |
|---|---|
| ZIP to upload | `room-planner\dist\room-planner.zip` (built by `scripts\build-agensi-zip.ps1`) |
| ZIP contents | SKILL.md, references/ (3), examples/ (1), CHANGELOG.md. No README, LICENSE, evals or tests |
| Version | 1.1.1 |
| Price | **Free** |
| Brand | Codelady Abroad |

## Name (≤ 60)
```text
Room Planner: Layout, Colours, Light and Renovation Budget
```

## Summary (≤ 300)
```text
Free room and small-flat planner. Give sizes, budget and style; get an ASCII floor plan with clearances, a 60-30-10 palette, a lighting plan, paint/tile/flooring quantities, a budget shopping list, a renovation order with quote checks and an image prompt. Risky work goes to pros.
```

## Description
```markdown
Tell it your room size, doors, windows, budget and style. It plans the room the way an interior designer would, in short phone-friendly sections and in your language.

You get:
- an ASCII floor plan drawn to scale, with furniture sizes and walkway clearances
- three 60-30-10 colour palettes with hex codes, matched to your window's light
- a three-layer lighting plan with lux, lumens and kelvin
- paint litres, tiles, flooring and wallpaper rolls, each with a one-line calculation
- a shopping list (Basic / Better / Later) and a budget split with contingency
- a renovation order, a quote check and a contractor checklist
- renter-friendly ideas, a "will it fit through the door" check and a moving-in checklist
- an image prompt to see the room in free image tools

**Where it stops:** it never gives steps for walls, wiring, gas or plumbing and never says a wall is or isn't load-bearing. It routes those to licensed pros and the local authority. Prices are rough and local, and it gives no exact quotes.
```

## Categories (up to 3; pick the closest names in the dropdown)
1. Branding & Design
2. Productivity
3. Education & Learning

## Tags (10)
interior-design, room-layout, floor-plan, home-renovation, small-apartment, renters, lighting, color-palette, budget, free

## Use cases (8)
1. Plan a bedroom or study room layout from its measurements
2. Check walkway and furniture clearances before buying
3. Choose a colour palette and lighting plan for a dark room
4. Calculate paint, tiles, flooring or wallpaper to buy
5. Split a renovation budget and check a contractor quote
6. Make a small rented flat better without drilling
7. Check if a sofa or wardrobe will fit through the door
8. Get an image prompt to visualise the finished room

## Compatibility note
```text
Text only: no scripts, no web access, no paid tools. Works on any agent that can load a SKILL.md. Answers are short enough for a phone.
Plan compatibility: works on Free, Pro, Max and Team plans. Short on messages? Say so and it answers one part at a time.
```

## "See it in action" demo
Paste `examples/murad-rented-study-bedroom.md` (request + full result, about 2,300 characters).

## Limitations / FAQ
- Not a structural, electrical or legal service. In Azerbaijan, flat re-planning needs the district executive authority's decision (Housing Code, Art. 23–24); the skill says `verify locally`.
- Paint hex codes are screen colours; match paint in the shop.
- Material amounts are estimates; check the coverage on the product.

## Docs URL
Leave empty until the GitHub repo is public (then `https://github.com/codelady-ship/room-planner` and uncomment `docs_url` in SKILL.md).

## Evidence you may quote
Blind evals: see `tests/blind-eval-results-2026-11-11.md`.
