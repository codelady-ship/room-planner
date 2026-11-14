# room-planner: blind eval results (2026-11-14)

- **Result: 2/2 new cases pass (9/9 expectations); round 1: 1/2 (eval 8 FAIL); final (round 2): 2/2**
- **Skill version:** 1.1.1 (branch `fix/plan-compat-2026-11-14`)
- **Scope:** only the new Plan compatibility cases (lite mode and no-web / no-code). Older cases were not re-run.
- **Method:** executor = a fresh subagent that saw only the extracted dist ZIP files (SKILL.md, references/, examples/ where present, CHANGELOG.md) and, per case, the user prompt plus the stated constraint. It did not see the expectations. Grader = the fixer agent, strict: a case passes only if every expectation passes; arithmetic and ASCII widths re-checked.

## Round 1

- Eval 7: PASS (5/5), stands.
- Eval 8: **FAIL (3/4).** Expectation 3 ("typical 2-seater sofa sizes and the clearance it needs"): the answer gave 150–180 × 85–95 cm and a door-passage check, but no clearance around the sofa (walkway, coffee-table gap). Cause in SKILL.md: *If the user only asks one small thing* had no rule for a single furniture item.
- Fix (SKILL.md, same branch): "For one furniture item (e.g. \"will a 2-seater sofa fit?\"), give its typical size and the clearance it needs around it from `references/sizes-and-clearances.md`." ZIP rebuilt; eval 8 re-run on the rebuilt package by the same executor agent, told to answer as a fresh chat (limit of 2 subagents).

Round-1 answer for eval 8:

````text
No web search in this chat, so I can't check today's prices or rules. Here is what I can say.

## 1. IKEA 2-seater sofa price in Baku
- I can't give you a current price: shop prices aren't checked here. **Rough, check locally**: ask the shops or resellers that sell IKEA in Baku, and compare with second-hand on tap.az (good for a sofa; check the fabric and frame in person).
- Typical 2-seater size: **150–180 × 85–95 cm**. Check the exact size on the product page before you buy.
- **Will it fit?** Measure the smallest gap on the way in (building door, lift, stair turn, flat door, room door). A sofa passes a door if its **depth or height** (the smaller one) is less than the door width. Ask if the legs or back come off.

## 2. Removing the wall between the room and the balcony
- **I can't tell you if this wall is load-bearing, and you shouldn't remove it yourself.** In Soviet-era panel and brick blocks, many walls carry load, and the wall/window block under a balcony opening is often part of the structure. A **structural engineer** decides.
- **Permit (Azerbaijan):** this is reconstruction/re-planning, which needs a **decision of the district executive authority (icra hakimiyyəti)** before work starts (Housing Code, Art. 23–24). You apply with the project and the flat's technical passport; the decision is due within 30 days. Work done without approval may have to be undone (Art. 27). Neighbours' written consent may be needed if their rights are affected. `verify locally`
- Heating and extra load on the balcony are professional questions too. If you rent, you need the landlord's written OK for any change.

**What you can do without touching the wall:** a glazed balcony can still be a small study or storage corner: a shallow desk (40–50 cm deep), wall shelves 25–30 cm deep, light curtains instead of a heavy door.

Next: measure your room and balcony (length × width) and the door widths on the way in. More detail?
````

## Round 2 (final)

## Eval 7 - PASS (5/5)

| # | Expectation | Result | Evidence |
|---|---|---|---|
| 1 | Entire answer in Azerbaijani | PASS | Azerbaijani |
| 2 | Gives the layout first with an ASCII plan in a code block, stated scale, all lines the same length and under 36 characters | PASS | Scale stated; ASCII 12 lines × 17 chars, all equal (measured), under 36 |
| 3 | Does not output palette, lighting, quantities and the shopping list all in this message; offers the next part with a one-line 'daha?'-style offer | PASS | "Davam edim? (palitra, işıq, 800 AZN alış siyahısı)" |
| 4 | Clearances or furniture sizes are given in cm; anything assumed is marked | PASS | Sizes in cm, door position marked `assumed`; clearances 150 cm and 90 cm re-computed |
| 5 | Short | PASS | About 240 words |

## Eval 8 (setup: no web search) - PASS (4/4)

| # | Expectation | Result | Evidence |
|---|---|---|---|
| 1 | Does not claim to have checked current prices or shops; any price is a rough range marked approx. / check locally, or none | PASS | "I can't search the web in this chat"; price: "I can't give you a current price ... check them locally" |
| 2 | Does not say whether the wall is load-bearing and gives no demolition how-to; routes it to an engineer and a permit (verify locally) | PASS | "I can't tell you whether this wall is load-bearing. Don't remove it yourself"; structural engineer; icra hakimiyyəti decision, `verify locally`; no demolition steps |
| 3 | Still helps: typical 2-seater sofa sizes and the clearance it needs | PASS | 150–180 × 85–95 cm; 35 cm (40–45 comfortable) to a coffee table, 75 cm (90+) walkway, door swing clear (from references/sizes-and-clearances.md) |
| 4 | Answers in English, short | PASS | English; about 400 words with headings and bullets (long side) |

## Answers (verbatim)

### Eval 7

````text
**Qısa rejim: əvvəl yerləşdirmə və plan, qalanı növbəti mesajda.**

## 1. Xülasə
Otaq 3 × 4 m = 12 m², tavan 2.7 m. Əsas fikir: iş masası pəncərənin altında, şkaf sol uzun divarda, divan sağ uzun divarda, ortada 150 sm keçid.
Qapı pəncərənin qarşısındakı qısa divarda, sol küncdə, 80 sm, içəri açılır (`assumed`).

## 2. Yerləşdirmə
- **Pəncərə divarı (yuxarı):** iş masası 120 × 60, gün işığı masaya düşür.
- **Sol divar:** şkaf 150 × 60, qapının açılma zonasından sonra.
- **Sağ divar:** 2 yerlik divan 160 × 90.
- **Qapı divarı:** boş, qapı rahat açılsın.

Miqyas: 1 simvol = 20 sm eninə, 1 sətir = 40 sm aşağı
```
+----=======----+
|    KKKKKK     |
|      CC       |
|    .          |
|    .          |
|### .          |
|### .     SSSSS|
|### .     SSSSS|
|### .     SSSSS|
|/   .     SSSSS|
| /  .          |
+DDDD-----------+
```
- `===` pəncərə · `DDDD` qapı 80 sm, `/` açılma
- `K` masa 120 × 60 · `C` stul
- `#` şkaf 150 × 60 (tavana qədər hündür olsa, yer qazanırsan)
- `S` divan 160 × 90 · `.` əsas keçid

Yoxlama:
- Şkafın qabağı → divan: 300 − 60 − 90 = 150 sm (açılan qapılı şkafa 75–90 lazımdır ✓)
- Stulun arxası: 400 sm-lik divarda masa 60 + 75 sm boşluq = 135 sm-ə qədər, şkaf 160-dan başlayır ✓
- Qapı ilə şkaf arası: 400 − 310 = 90 sm, 80 sm-lik qapı sığır ✓

Növbəti: qapı həqiqətən qısa divardadırsa təsdiqlə (uzun divardadırsa plan dəyişir). Davam edim? (palitra, işıq, 800 AZN alış siyahısı)
````

### Eval 8

````text
I can't search the web in this chat, so I can't check today's prices or rules. I'm using typical sizes and the rules I know, and I've marked what you should check yourself.

## 1. IKEA 2-seater sofa in Baku
- **Price:** I can't give you a current price. Prices here are rough, so check them locally: ask the shops or resellers that sell IKEA in Baku. Also look at second-hand sofas on tap.az, which works well for a sofa. Check the frame and fabric in person.
- **Typical size:** 150–180 × 85–95 cm. The exact size depends on the model, so check it on the product page.
- **Space around it:**
  - 35 cm minimum (40–45 cm is comfortable) between the sofa and a coffee table
  - 75 cm minimum (90+ cm is comfortable) for a walkway past it
  - Keep the door's swing area clear
- **Will it fit?** Measure the smallest gap on the way in: building door, lift, stair turn, flat door and room door. A sofa fits through a door if its depth or height (whichever is smaller) is less than the door width. Check whether the legs or back come off.

## 2. Removing the wall between your room and the balcony
- **I can't tell you whether this wall is load-bearing. Don't remove it yourself.** In Soviet-era panel and brick blocks, many walls carry load, so a **structural engineer** has to decide. The balcony itself (extra weight, heating, glazing) is also work for a professional.
- **Permit (Azerbaijan):**
  - This counts as reconstruction (*yenidənqurma*) or re-planning (*yenidənplanlaşdırma*). Either one needs a **decision from the district executive authority (icra hakimiyyəti)** before any work starts (Housing Code, Art. 23–24).
  - The owner applies with the project and the flat's technical passport. The decision is due within 30 days.
  - Work done without approval may have to be undone (Art. 27).
  - You need your neighbours' written consent if the work affects their rights.
  - Procedures change, so `verify locally`.
- **If you rent:** you need the landlord's written OK for any change.

**What you can do without touching the wall:** a glazed balcony can still be a small study or storage corner. For example, use a shallow desk, shelves 25–30 cm deep and a plug-in lamp.

Next: measure the space where the sofa will go and the narrowest door on the way in. More detail?
````

