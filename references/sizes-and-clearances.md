# Sizes and clearances (quick reference)

Typical sizes in cm. Real products vary; always check the product page. Clearances are common good-practice values gathered from standard architecture references; "min" is the tight limit, "good" is comfortable.

## Furniture sizes (W × D × H)

| Item | Typical size |
|---|---|
| Single bed | 90 × 200 |
| Small double | 120–140 × 200 |
| Double / queen | 160 × 200 |
| King | 180 × 200 |
| Nightstand | 40–50 × 35–45 |
| Wardrobe (hinged or sliding) | 100–250 wide × 60 deep |
| Chest of drawers | 80–120 × 45–50 |
| Desk | 100–140 × 60–70, height 72–75 |
| Office chair footprint | 60 × 60 |
| 2-seat sofa | 150–180 × 85–95 |
| 3-seat sofa | 200–230 × 90–100 |
| Corner sofa | 230–280 × 160–200 |
| Armchair | 75–90 × 80–90 |
| Coffee table | 90–120 × 50–60 |
| TV unit | 120–200 × 35–45 |
| Dining table for 4 | 120 × 80, or round Ø 100 |
| Dining table for 6 | 160–180 × 90 |
| Dining chair footprint | 45 × 50 |
| Bookcase | 80 × 30 |
| Kitchen base unit | 60 deep, worktop height 85–92 |
| Fridge | 60 × 65, height 150–200 |
| Washing machine | 60 × 55–60 |

## Clearances

| Space | Min | Good |
|---|---|---|
| Main walkway through a room | 75 | 90+ |
| Space beside a bed (to get in) | 45 | 60–70 |
| Space at the foot of a bed | 60 | 75–90 |
| In front of a wardrobe (hinged doors) | 75 | 90 |
| In front of a wardrobe (sliding doors) | 60 | 70 |
| In front of drawers | 75 | 90 |
| Behind a desk chair | 75 | 90–100 |
| Sofa to coffee table | 35 | 40–45 |
| Behind a dining chair to wall (sitting) | 75 | 90 |
| Walk past a seated diner | 90 | 110 |
| Table width per person | 55 | 60–65 |
| Kitchen aisle (one cook) | 90 | 100–120 |
| Kitchen aisle (two cooks) | 110 | 120–130 |
| Worktop beside hob | 30 | 40+ |
| Worktop between sink and hob | 40 | 60+ |
| Upper cabinets above worktop | 50 | 55–60 |
| In front of toilet | 55 | 70 |
| In front of washbasin | 60 | 75 |
| Door swing zone | keep clear | keep clear |
| Wheelchair turning circle | Ø 150 | Ø 150+ |
| Wheelchair door opening | 80 clear | 90 |

## Kitchen work triangle

The three legs between sink, hob and fridge: each leg about 120–270 cm, the total about 400–790 cm. No tall unit or walkway should cut through the triangle. In one-wall kitchens use the order fridge → worktop → sink → worktop → hob.

## TV distance

A comfortable viewing distance for a 4K TV is about **1.2–1.6 × the screen diagonal**. Diagonal in inches × 2.54 = cm.
- 43" (109 cm) → 1.3–1.75 m
- 55" (140 cm) → 1.7–2.25 m
- 65" (165 cm) → 2.0–2.65 m

The middle of the screen should be close to seated eye level (about 100–110 cm from the floor).

## Shelves and hanging

- Hanging rail: 160–170 cm high for long clothes, two rails at about 100 and 200 cm for short clothes.
- Art: centre at about 145–150 cm from the floor; above a sofa, 20–25 cm above the backrest.
- Curtain rod: 10–15 cm above the window frame (higher makes ceilings look taller), 15–25 cm wider on each side.

## Sample ASCII plan

Bedroom 3.2 × 3.6 m (11.5 m²), window in the top wall, door bottom-left opening inwards.
At 20 cm per character the inside is 320 ÷ 20 = 16 characters wide; at 40 cm per line it is 360 ÷ 40 = 9 lines tall.

```
1 char = 20 cm across, 1 line = 40 cm down
+-----======-----+
|NN        KKKKKK|
|BBBBBBBBBB  CC  |
|BBBBBBBBBB      |
|BBBBBBBBBB   ###|
|BBBBBBBBBB   ###|
|NN ........  ###|
|/  .         ###|
| / .         ###|
|   .            |
+DDDD------------+
```

Legend: `===` window, `DDDD` door (80 cm), `/` door swing, `B` bed 160 × 200 (head on the left wall), `N` nightstands, `K` desk 120 × 40 under the window, `C` chair, `#` sliding wardrobe 200 × 60, `.` main walkway.
Check: bed foot to wardrobe = 3 characters = 60 cm (sliding-door minimum, tight); open floor below the bed = 4 lines = 160 cm.

Tips for drawing:
- Count characters: room width in cm ÷ scale = number of characters inside the walls.
- Draw walls first, then doors and windows, then the biggest piece, then the walkway, then the rest.
- If a label does not fit, use a short code and explain it in the legend.
