# Square knives and spurs (Τετράγωνα ξυράφια και Προχαράξεις)

Two related groups of screwed carbide inserts, taught together from the user's file `Square Knives and Spurs.dwg`.

- **Square knives (τετράγωνα ξυράφια):** square inserts used like the other knives. They are **four-edged (τετράκοπα)**: all 4 sides cut, and the knife is indexed by turning it 90°.
- **Spurs (προχαράξεις):** inserts that cut only **horizontal planes**, i.e. the faces perpendicular to the tool axis (horizontal on a vertical spindle). The spur sits on the side of the tool and its tip scores the fibres of that face ahead of the main knives, so the edge does not tear out. What matters for a spur is **one cutting point (μύτη)**, not an edge. The spur is positioned by that point.

## Which code is what

| Code | Drawing title | Kind | Use |
|---|---|---|---|
| 013259 | 10.5x10.5x1.5-35° | Square knife, no countersink | Knife only. **Never a spur.** |
| 012002 | 12x12x1.5-35° | Square knife, no countersink | Knife only. **Never a spur.** |
| 106682 | 10.5x10.5x1.5-35°(CS) | Square knife with countersink (CS) | Used as a spur |
| 013295 | 14x14x1.2-30° | Square knife with countersink | Used as a spur |
| **013260** | 14x14x2-30° | Square knife with countersink | Used as a spur. **The default spur.** |
| 013258 | 14x28x2-30° | Spur (rhombus, 60° tips) | Spur only |
| 030829 | 16x16x3-32° | Spur (rhombus, 60° tips) | Spur only |
| 045180 | 22.9x19.8x2.5-30° | Spur (equilateral triangle) | Spur only |
| 013271 | 22x19x2-30° | Spur (equilateral triangle) | Spur only |

- **Default spur:** when the user just says "βάλε προχάραξη" without a code, use **013260(14x14x2-30°)**.
- Square knives with a countersink (φρέζα) in the screw hole (CS = countersink) can be used as spurs. The ones without (013259, 012002) cannot.
- These 9 codes are the complete list. Anything else on TIGRA pages 28–31 is out of scope.

## Reference form

Code, then `LxWxT-angle°` in parentheses, as for the edge forming knives. The angle is the clearance angle from the catalog. Decimal point, no trailing zeros.

`013260(14x14x2-30°)` · `045180(22.9x19.8x2.5-30°)` · `106682(10.5x10.5x1.5-35°-CS)`

106682 has the same size as 013259, so `-CS` is added to keep the two apart.

## Catalog and grade

TIGRA Woodworking Catalog 2023. Grade = the column the code is printed in.

| Code | L | W | T | Angle | Catalog page | Grade |
|---|---|---|---|---|---|---|
| 013259 | 10.5 | 10.5 | 1.5 | 35° | 28 ("Square knives", d = 4.0) | T04F-CR |
| 012002 | 12 | 12 | 1.5 | 35° | 28 (d = 4.0) | T04F-CR |
| 106682 | 10.5 | 10.5 | 1.5 | 35° | 28 (countersunk block) and 29 | T04MG-CR |
| 013295 | 14 | 14 | 1.2 | 30° | 28 (countersunk block) | T07MF-CR |
| 013260 | 14 | 14 | 2 | 30° | 28 (countersunk block) and 29 | T04F-CR |
| 013258 | 14 | 28 | 2 | 30° | 31 ("Spurs, grooving knives") | T07MF-CR |
| 030829 | 16 | 16 | 3 | 32° | 31 | T07MF-CR |
| 045180 | 22.9 | 19.8 | 2.5 | 30° | 31 | T07MF-CR |
| 013271 | 22 | 19 | 2 | 30° | 31 | T07MF-CR |

Note: the grades differ per code. For these parts, use the grade above, not the general T04F-CR rule.

## Views and conventions

- Each block has three views (visibility states): **Top (κάτοψη)**, **Bottom (κάτω όψη)** and **Section/Side (πλάγια όψη)**. The square knives call the side view `Section`, the spurs call it `Side`. The parts table shows Top and Side.
- **Base point:** the hole centre (0, 0) in all views. The side view's x axis is the plan's x axis. Its y axis is the thickness: top face y = +T/2, bottom face y = −T/2.
- **Top face = the large face.** The flanks run inward to the smaller bottom face at the clearance angle, so the side view is a trapezoid, wider at the top.
- Coordinates are in mm at 1:1. Draw every line **ByLayer**: magenta is knowledge only.

### Cutting point of a spur (μύτη προχάραξης)

The user marked the cutting point in magenta in the **side view**: the top face plus the left flank. The point is where they meet: the **top left corner of the side view**, x = leftmost, y = +T/2. The edges themselves don't matter. Only the point does.

| Code | Cutting point (x, y) in the side view | In plan it is |
|---|---|---|
| 106682 | (−5.25, 0.75) | the left side (only the side view matters) |
| 013295 | (−7, 0.6) | the left side |
| 013260 | (−7, 1) | the left side |
| 013258 | (−14, 1) | the left 60° tip (−14, 0) |
| 030829 | (−16, 1.5) | the left 60° tip (−16, 0) |
| 045180 | (−11.4315, 1.25) | the bottom left corner (−11.4315, −6.6) |
| 013271 | (−11, 1) | the bottom left corner (−11, −6.3509) |

- For the square spurs, the plan corner does not need to be defined: the side view point is enough (confirmed by the user).
- The other corners cut too: when the tip is blunt, the customer turns the insert. That does not matter for the drawing. Always draw the insert with the cutting point as above.
- Where the cutting point goes on the tool is placement, which belongs in the **placement skill**, not here.

### Cutting edges of the square knives

013259 and 012002 are four-edged: the 4 edges of the top face cut. Nothing is marked in magenta in the DWG.

## Square inserts: Top and Bottom views (rule)

For every square insert, with a = L/2 and b = L/2 − T·tan(angle):

| Code | a | b | Hole circles (Top) | Hole circles (Bottom) |
|---|---|---|---|---|
| 013259 | 5.25 | 4.1997 | Ø4.1 | Ø4.1 |
| 106682 | 5.25 | 4.1997 | Ø4.1, Ø6.7 | Ø4.1, Ø6.7 |
| 012002 | 6 | 4.9497 | Ø4.1 | Ø4.1 |
| 013295 | 7 | 6.3072 | Ø8.6, Ø10.2 | Ø8.6 |
| 013260 | 7 | see below | Ø6.5, Ø10 + mark | Ø6.5, Ø10 |

- **Top:** square ±a and the hole circles.
- **Bottom:** square ±a, inner square ±b, 4 corner lines (±a, ±a) → (±b, ±b), and the hole circles.
- **013260, manufacturer's mark:** a circle Ø1 at (−4.95, 4.95), in the **Top view only**. Draw it.
- The catalog gives d = 4.0 for 013259 and 012002. The DWG draws the hole Ø4.1. Draw Ø4.1.

### 013260 Bottom

It does not follow the rule, because the side view has a second, small bevel near the bottom face. Draw it from the side-view values:

- Square ±7; circles Ø6.5, Ø10.
- Square ±6.0429 (where the second bevel starts).
- Square ±5.45 (the bottom face).
- 4 corner lines (±7, ±7) → (±5.45, ±5.45).

The Bottom state in `Square Knives and Spurs.dwg` was drawn with slightly irregular contours (±6.0561/±6.0432 and ±5.424/±5.4494). The user decided to use the side-view values above instead.

## Square inserts: Section (side) views

### 013259 (10.5x10.5x1.5-35°): no hole in the section

- L (−5.25, 0.75) → (5.25, 0.75)
- L (−5.25, 0.75) → (−4.1997, −0.75); L (5.25, 0.75) → (4.1997, −0.75)
- L (−4.1997, −0.75) → (4.1997, −0.75)

### 012002 (12x12x1.5-35°): no hole in the section

- L (−6, 0.75) → (6, 0.75)
- L (−6, 0.75) → (−4.9497, −0.75); L (6, 0.75) → (4.9497, −0.75)
- L (−4.9497, −0.75) → (4.9497, −0.75)

### 106682 (10.5x10.5x1.5-35°-CS)

- L (−5.25, 0.75) → (5.25, 0.75) · magenta
- L (−5.25, 0.75) → (−4.1997, −0.75) · magenta
- L (5.25, 0.75) → (4.1997, −0.75)
- L (−4.1997, −0.75) → (4.1997, −0.75)
- Countersink: L (±3.35, 0.75) → (±2.05, −0.55); L (−2.05, −0.55) → (2.05, −0.55); L (±2.05, −0.55) → (±2.05, −0.75)

### 013295 (14x14x1.2-30°)

- L (−7, 0.6) → (−5.1, 0.6) · magenta; L (−5.1, 0.6) → (5.1, 0.6); L (5.1, 0.6) → (7, 0.6)
- L (−7, 0.6) → (−6.3072, −0.6) · magenta; L (7, 0.6) → (6.3072, −0.6)
- L (−6.3072, −0.6) → (−4.3, −0.6); L (−4.3, −0.6) → (4.3, −0.6); L (4.3, −0.6) → (6.3072, −0.6)
- Countersink: L (±5.1, 0.6) → (±4.3, −0.2); L (−4.3, −0.2) → (4.3, −0.2); L (±4.3, −0.2) → (±4.3, −0.6)

### 013260 (14x14x2-30°)

- L (−7, 1) → (7, 1) · magenta
- L (−7, 1) → (−6.0429, −0.6577) · magenta; L (7, 1) → (6.0429, −0.6577)
- L (±6.0429, −0.6577) → (±5.45, −1)
- L (−5.45, −1) → (5.45, −1)
- Countersink: L (±5, 1) → (±3.25, −0.75); L (−3.25, −0.75) → (3.25, −0.75); L (±3.25, −0.75) → (±3.25, −1)

## Rhombus spurs (013258, 030829)

A 60° rhombus, point-symmetric about the hole. The cutting tips are the acute (60°) corners on the x axis.

The 030829 outline is the 013258 outline scaled by 16/14. Thickness, angle and bevels differ, so each has its own listing.

**What the catalog L and W mean for the rhombi:** **L is the distance across the parallel sides** (the inscribed circle). For a 60° rhombus, the long diagonal (tip to tip) = 2·L and the side = L / sin 60°.

| Code | Catalog L x W | Across flats | Tip to tip | Short diagonal = side |
|---|---|---|---|---|
| 013258 | 14 x 28 | 14 | 28 | 16.1658 |
| 030829 | 16 x 16 | 16 | **32** | 18.4752 |

For 013258 the catalog W is the tip-to-tip length. For 030829 the catalog prints W = 16, which can't be a tip-to-tip length: a 16 mm rhombus would be only 8 across flats, smaller than its Ø8.9 hole. **Draw 030829 32 tip to tip.** Keep the name `030829(16x16x3-32°)` as in the catalog.

### 013258 (14x28x2-30°)

- **Top:** rhombus (−14, 0) → (0, 8.0829) → (14, 0) → (0, −8.0829) → back; circles Ø6.4, Ø9.6.
- **Bottom:** the same rhombus; inner rhombus through (±12.037, 0) and (0, ±6.9496) (bevel start); inner rhombus through (±10.8906, 0) and (0, ±6.2877) (bottom face); connector lines on the axes: (±14, 0) → (±12.037, 0) → (±10.8906, 0) and (0, ±8.0829) → (0, ±6.9496) → (0, ±6.2877); circle Ø6.4.
- **Side:**
  - L (−14, 1) → (0, 1) · magenta; L (0, 1) → (14, 1)
  - L (−14, 1) → (−12.037, −0.7) · magenta; L (14, 1) → (12.037, −0.7)
  - L (−12.037, −0.7) → (12.037, −0.7)
  - L (±12.037, −0.7) → (±10.8906, −1)
  - L (−10.8906, −1) → (10.8906, −1)
  - L (0, 1) → (0, −1) (the obtuse corners seen edge-on; drawn as (0, 1) → (0, −0.7) → (0, −1))

### 030829 (16x16x3-32°)

- **Top:** rhombus (−16, 0) → (0, 9.2376) → (16, 0) → (0, −9.2376) → back; circles Ø6, Ø8.9.
- **Bottom:** the same rhombus; inner rhombus through (±12.2508, 0) and (0, ±7.073); connector lines (±16, 0) → (±12.2508, 0) and (0, ±9.2376) → (0, ±7.073); circle Ø6.
- **Side:**
  - L (−16, 1.5) → (0, 1.5) · magenta; L (0, 1.5) → (16, 1.5)
  - L (−16, 1.5) → (−12.2508, −1.5) · magenta; L (16, 1.5) → (12.2508, −1.5)
  - L (−12.2508, −1.5) → (12.2508, −1.5)
  - L (0, 1.5) → (0, −1.5)

## Triangle spurs (045180, 013271)

Equilateral triangle, hole at the centroid, one vertex up on the y axis. The cutting point is the bottom left corner.

### 045180 (22.9x19.8x2.5-30°)

- **Top:** triangle (−11.4315, −6.6) → (11.4315, −6.6) → (0, 13.2) → back; circles Ø6.4, Ø10.4.
- **Bottom:** the same triangle; inner triangle (−9.5002, −5.4849), (9.5002, −5.4849), (0, 10.9699) (bevel start); inner triangle (−7.7942, −4.5), (7.7942, −4.5), (0, 9) (bottom face); corner lines from each outer corner to the matching inner corners; circle Ø6.4.
- **Side:**
  - L (−11.4315, 1.25) → (11.4315, 1.25) · magenta
  - L (−11.4315, 1.25) → (−9.5002, −0.6813) · magenta; L (11.4315, 1.25) → (9.5002, −0.6813)
  - L (−9.5002, −0.6813) → (9.5002, −0.6813)
  - L (±9.5002, −0.6813) → (±7.7942, −1.25)
  - L (−7.7942, −1.25) → (7.7942, −1.25)

### 013271 (22x19x2-30°)

- **Top:** triangle (−11, −6.3509) → (11, −6.3509) → (0, 12.7017) → back; circles Ø6.5, Ø10.2.
- **Bottom:** the same triangle; inner triangle (−9, −5.1962), (9, −5.1962), (0, 10.3923); corner lines from each outer corner to the inner corner; circle Ø6.5.
- **Side:**
  - L (−11, 1) → (11, 1) · magenta
  - L (−11, 1) → (−9, −1) · magenta; L (11, 1) → (9, −1)
  - L (−9, −1) → (9, −1)

## How the user draws them (`Square Knives and Spurs.dwg`)

- Each part is a **dynamic block named after its drawing title** (e.g. `14x14x2-30°`), units mm. The block description holds the code. Visibility states: `Top`, `Bottom`, `Section` (square knives) or `Side` (spurs).
- Parts table (BOM) on layer `BOM`, blocks at **scale 0.5**: the Top view in the cell, the side view **15 above it (30 mm at 1:1)**. Below them two MText lines, style `BOM_TXT`, height 2: the drawing title and the code.
- **CADCraft:** exploding these blocks shows all states on top of each other. To read them separately, save as DXF and use the `BLOCKVISIBILITYPARAMETER` state lists. When drawing a new one, draw plain geometry at 1:1 from the coordinates above, not a dynamic block.
