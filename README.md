# Room Planner

> Give your room's measurements, budget and style. Get a text layout with an ASCII floor plan, furniture sizes and clearances, a colour palette with hex codes, a lighting plan, a shopping list by budget level and a prompt to visualise it with free image tools.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Skill](https://img.shields.io/badge/Claude-Skill-D97757.svg)](SKILL.md)
[![Price: Free](https://img.shields.io/badge/price-free-brightgreen.svg)](#license)

A free, text-only skill by Codelady Abroad for students, renters and first-time home owners. It runs anywhere a plain prompt runs: Claude Code, the Claude app, other agents or a simple website form. No scripts, files or paid tools.

## What you get

- A short list of questions, only for what is missing (size, doors and windows, sun direction, who lives there, budget, style).
- Layout in words plus an ASCII plan drawn to scale that fits a phone screen.
- Furniture table with sizes and the walkway clearance in front of each item.
- Three 60-30-10 colour palettes with hex codes, matched to the room's light.
- Three-layer lighting plan (ambient, task, accent) with lux targets, a lumen calculation and kelvin.
- Shopping list split into Basic / Better / Later, with a budget split and a contingency line.
- Renovation order of trades, if repairs are planned.
- A ready image prompt and free tools to see the room before buying.
- Small-flat tips for Baku-style apartments.
- Answers in the user's language.

## Safety

The skill says plainly that load-bearing walls, electrics, gas, wet-zone moves, balconies and permits are for a licensed professional, and never gives how-to steps for them.

## Example request

> My bedroom is 3.2 × 3.6 m, ceiling 2.7 m. The window is on the short wall and faces north, the door is in the opposite corner. I need a double bed, a desk for studying and a wardrobe. Budget 1500 AZN. I like calm, warm Scandinavian style.

## Install

- **Claude Code:** copy this folder to `~/.claude/skills/room-planner/`.
- **Claude app:** zip the folder (with `SKILL.md` inside `room-planner/`) and upload it under *Customize → Skills*.
- **Any other agent or a web form:** use the body of `SKILL.md` as the system prompt. `references/` holds optional tables.

Test prompts and expected points: [`evals/evals.json`](evals/evals.json).

## Sources and credits

Written from scratch. Numbers are common good-practice values, rounded, informed by:
- Neufert, *Architects' Data* (furniture sizes, clearances)
- NKBA Kitchen & Bath Planning Guidelines (work triangle, aisles)
- EN 12464-1 and the IES Lighting Handbook (lux ranges; home values set lower)
- WCAG 2.2 contrast and the light-reflectance-value guidance used in accessible design
- ADA 2010 Standards (wheelchair turning circle and door widths)
- The gap analysis in Codelady Abroad's own research notes, which found no free text-only interior skill good enough (the idea of a text interior planner also appears in curiositech's `interior-design-expert`; no text was taken from it).

Always check sizes against real products and local rules.

## License

[MIT](LICENSE) © 2026 Codelady Abroad
