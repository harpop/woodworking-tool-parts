# Edge forming knives (Γωνιοσπάσεις)

Source: TIGRA Woodworking Catalog 2023, **page 36** (PDF page 20, left half), first block of the table. The catalog calls them **"Edge rounding knives"** (DE Kantenrunder); we call them **edge forming knives / γωνιοσπάσεις**. The only grade column is **T10MG**. Geometry learned from the user's file `Edge Forming Knives.dwg`.

## What they are

- A small carbide insert with a **central countersunk hole** and **two wings**, one on each side of the hole.
- Each wing carries the **forming profile** at its outer top corner: a **45° chamfer** or a **concave radius R**. The knife puts this profile on the edge of the workpiece: a 45° bevel (γωνιοσπάση) or a convex rounding of radius R.
- **Reversible:** the two wings are mirror images, so the knife has 2 cutting edges. When one wears out, the knife is turned 180°.
- The plan view (κάτοψη) is **the same for all 7 knives**. Only the side view (the profile) and T change.

## Range (grade T10MG)

| Code | L | W | T | Type | Profile | Reference form |
|---|---|---|---|---|---|---|
| 032292 | 16 | 22 | 5 | TKM 45° | 45° chamfer | 032292(16x22x5-45°) |
| 032294 | 16 | 22 | 5 | TKM R 1.5 | R1.5 | 032294(16x22x5-R1.5) |
| 032295 | 16 | 22 | 5 | TKM R 2.0 | R2 | 032295(16x22x5-R2) |
| 032296 | 16 | 22 | 5 | TKM R 2.5 | R2.5 | 032296(16x22x5-R2.5) |
| 032297 | 16 | 22 | 5 | TKM R 3.0 | R3 | 032297(16x22x5-R3) |
| 032299 | 16 | 22 | 5 | TKM R 4.0 | R4 | 032299(16x22x5-R4) |
| 032301 | 16 | 22 | **6** | TKM R 5.0 | R5 | 032301(16x22x6-R5) |

**Reference form** (confirmed by the user): code, then `LxWxT-Type` in parentheses, e.g. `032295(16x22x5-R2)`. Decimal point, no trailing zeros, as for knives.

- **L = 16** is the height of the plan view (along the cutting edge), **W = 22** the width across the two wings, **T** the thickness (5, but **6 for R5**).
- **Draw W = 22** (outer edges at x = ±11), as the user decided. The source DWG has 22.05 (x = ±11.025); the coordinates below are already corrected to 22. The correction trims the extra 0.025 at the outer face and leaves the rest of the profile unchanged.
- These 7 are the complete list. Anything else on catalog page 36 is out of scope.
- **Selection:** the profile asked for on the workpiece edge decides the knife (45° → 032292, R2 → 032295, …). There is only one size, so there is nothing else to choose.

## Geometry (from the DWG, mm, 1:1)

Coordinates are **centred on the hole**: x across the wings (W), y along L in the plan view and along T in the side view. Only the right half is listed where the shape is symmetric; mirror about x = 0 for the left half (an arc from a1° to a2° becomes 180−a2° to 180−a1°).

### Plan view (κάτοψη), common to all 7

- **Hole:** three concentric circles: **Ø10.206** (countersink outer edge), **Ø6.7115**, **Ø6.456**.
- **Central lug** (top and bottom, mirrored about y = 0):
  - End edge at y = ±8 from x −3.5072 to 3.5072 (so L = 16).
  - Edge-break line at y = ±7.4912 from x −3.6435 to 3.6435.
  - Lug sides at 15°: (±3.5072, ±8) → (±4.5356, ±4.1618).
- **Relief notch** between lug and wing, per quadrant (top right shown):
  - Arc R1.5, centre (5.9845, 4.55), 195°..318.945°.
  - Arc R0.2421, centre (7.2982, 3.4058), 135°..138.945°.
- **Wing:**
  - 45° line (7.127, 3.577) → (11, 7.45).
  - Outer edge (cutting edge) x = ±11, y −7.45..7.45 (14.9 long).
  - Inner line x = ±7.5483, y −3.9983..3.9983 (joins the two 45° lines).

### Side view (πλάγια όψη)

Bottom face y = −T/2 across the full width (x −11..11). Top face y = +T/2 between the two profiles. Outer face x = ±11 from the bottom up to the **land** (where the profile ends).

Lines inside the outline (lug end face and edges seen from the side):

- Lug end face: rectangle x ±3.5, y ±(T/2 − 0.5), with 15° lines from (±3.5, ±(T/2 − 0.5)) to (±3.634, ±T/2). The 45° knife uses ±3.5072 / ±3.6435 / ±1.9912.
- Full-height vertical lines at x = ±4.534 (±4.5418 on R2 and R3, ±4.5356 on 45°).
- Full-height vertical lines at x = ±7.0436 (±7.0563 on R2 and R3, **±5.5356 on 45°**).

Profile, right side (mirror for the left):

| Type | T | Top face ends at | Upper line | Arc (centre, R, angles) | Lower line | Land (outer face) |
|---|---|---|---|---|---|---|
| 45° | 5 | x 6.575 | chamfer (6.575, 2.5) → (11, −1.925), 45° | – | – | y −2.5..−1.925 (0.575) |
| R1.5 | 5 | x 8 | (8, 2.5) → (8.3848, 0.3177) | (9.8620, 0.5782), R1.5, 190°..260° | (9.6015, −0.8990) → (11, −1.1456) | y −2.5..−1.1456 |
| R2 | 5 | x 8 | (8, 2.5) → (8.3240, 0.6625) | (10.2936, 1.0098), R2, 190°..260° | (9.9463, −0.9598) → (11, −1.1456) | y −2.5..−1.1456 |
| R2.5 | 5 | x 8 | (8, 2.5) → (8.4461, 0.8351) | (10.8609, 1.4822), R2.5, 195°..255° | (10.2139, −0.9327) → (11, −1.1433) | y −2.5..−1.1433 |
| R3 | 5 | x 8 | (8, 2.5) → (8.2024, 1.3521) | (11.1568, 1.8730), R3, 190°..260° | (10.6359, −1.0814) → (11, −1.1456) | y −2.5..−1.1456 |
| R4 | 5 | x 8 | (8, 2.5) → (8.1756, 1.5041) | (12.1148, 2.1987), R4, 190°..253.82° | none: the arc ends on the outer face at (11, −1.6429) | y −2.5..−1.6429 |
| R5 | 6 | x 8 | (8, 3) → (8.0440, 2.4968) | (13.0250, 2.9326), R5, 185°..246.11° | none: the arc ends on the outer face at (11, −1.6390) | y −3..−1.6390 |

### Cutting edge (κόψη: the part that forms the wood)

The user marked the cutting edges in magenta in `Edge Forming Knives.dwg`, in the side view:

- **The cutting edge is the whole profile** of each wing, from the point where it leaves the top face to the point where it meets the land on the outer face:
  - **45°:** the chamfer line.
  - **R knives:** upper tangent line + arc + lower tangent line, where the knife has them.
- **Both wings** carry the same cutting edge (mirror images). The knife is reversible, and one wing cuts at a time.
- **Not cutting:** the top face, the bottom face, the land (outer face below the profile) and all inner lines.
- **Plan view:** nothing is marked.
- **Drawing:** the magenta is knowledge only. When drawing, keep every line **ByLayer** like the rest of the knife.

How the R profiles are built:

- The arc is **concave** (its centre lies outside the knife), so the knife cuts a convex rounding on the workpiece.
- The arc joins the top face and the outer face through **short straight lines tangent to the arc**, inclined 10° (15° on R2.5, 5° on R5; R4 and R5 have no lower line). The profile zone always runs from x = 8 on the top face to x = 11 on the outer face.
- These tangent angles differ from knife to knife, so **draw from the table above, don't derive the profile from a rule**.

## How the user draws them (`Edge Forming Knives.dwg`)

- Each knife is a **block named after its drawing title** (e.g. `16x22x5-R1.5`), units mm, base point at the hole centre. It is a dynamic block with two visibility states, plan view and side view, and is inserted twice: the **side view above the plan view**, centres **30 mm apart** at 1:1.
- The file is a parts table (BOM) on layer `BOM`, with the blocks inserted at **scale 0.5**. One cell per knife, 25.89 wide and 42.6 high. The insert points are at the cell centre in x, plan at y = 16.6 and side view at y = 31.6.
- Under the views, two MText lines on layer `BOM`, style `BOM_TXT` (simplex.shx), height 2, top-left attach, at x = cell left + 2:
  - y = 10.6: the drawing title, e.g. `16x22x5-45°`;
  - y = 7.7: the code, e.g. `032292`.
- No dimensions in the example.
- **CADCraft:** exploding these blocks shows **both** visibility states on top of each other. When reading the geometry, take entities 0–26 as the plan view and the rest as the side view. When drawing a new one, draw plain geometry at 1:1 from the coordinates above (plan view, side view 30 mm above), not a dynamic block.
