# Drawing knives (Σχεδίαση ξυραφιών)

Learned from the user's example file `Knives Examples.dwg`. It holds four custom blanks, all 30x20.4x2:

| Example | Catalog family | Seat |
|---|---|---|
| 014917(30x20.4x2) | p44 | 35° bevel |
| 014918(30x20.4x2) | p45 | flat |
| 034998(30x20.4x2) | p46 bottom, Italian Style | 2 chamfers |
| 034981(30x20.4x2) | p46 top, Italian Style | 35° bevel |

The layout follows the catalog sketch: a front view plus a side view to its right.

## Layers and styles

| What | Layer | Style |
|---|---|---|
| Knife geometry (outline, hole, seat line) | `0` | colour ByLayer, Continuous |
| Dimensions | `Dimensions` (red) | dimstyle `Height.Dims`, text height override 1.0 |
| Title (the knife reference) | `0` | MText, style `Standard`, height 3, top-left attach |

- Units are mm, drawn at 1:1.
- Dimension precision: the style has 0 decimals. Add the override `decimals 1` only to dimensions whose value has a decimal (20.4, 6.3, Ø4.1), so whole values show as 40, not 40.0.
- **`Height.Dims` in a new drawing:** if the style is missing, create it with these settings, copied from the example file:
  - `DIMASZ 1.5`, `DIMBLK _Oblique`, `DIMDEC 0`, `DIMADEC 1`
  - `DIMEXE 0.5`, `DIMEXO 1`, `DIMGAP 1`, `DIMTAD 1`
  - `DIMTIX on`, `DIMTIH off`, `DIMTOH off`, `DIMATFIT 2`
  - `DIMDLI 1`, `DIMTXT 1.5`, `DIMTMOVE 1`, `DIMLUNIT 2`
  - `DIMDSEP "."`, `DIMZIN 0`, `DIMSCALE 1`
- **Layer `Dimensions` in a new drawing:** create it with colour red.

## Front view (Όψη)

Origin is the **bottom-left corner of the knife**. The **seat edge (έδρα) is at the bottom**, along y = 0, and the profile edge is at the top, y = W.

1. **Outline:** a closed polyline rectangle, L wide and W high: (0,0) → (L,0) → (L,W) → (0,W).
2. **Hole(s):** circles of diameter d with their centres at y = e.
   - 1 hole: centre at x = L/2.
   - 2 holes: centres at x = L/2 − a/2 and x = L/2 + a/2.
3. **Seat line:** a horizontal line across the full length, x 0 → L, at the height where the seat form ends:
   - 35° bevel: at y = T·tan35° (1.4004 for T = 2, 1.7505 for T = 2.5).
   - 2 chamfers (Italian Style): at y = 0.5.
   - Flat seat: **no seat line**.
   - The front-view seat line and the side view must always show the same seat form.
4. **Title:** MText with the knife reference, e.g. `014917(30x20.4x2)`. Insert at (0, W + 8.8), top-left attach, height 3.

## Side view (Πλάγια όψη)

Placed to the right of the front view. Its left edge is at x = L + 9.9 (gap ≈ 10 mm). It spans x 0 → T in local coordinates and has the same height as the front view, y 0 → W.

- **Flat seat:** a plain rectangle T x W.
- **35° bevel:** the left face runs the full height. The right face stops at y = T·tan35°, and a line runs from (T, T·tan35°) down to the sharp corner (0, 0). The bevel makes 35° with the seat plane, so the angular dimension between the vertical face and the bevel reads **55°**.
- **35° on both long edges (p48 family):**
  - The left face runs the full height. The right face is shortened at both ends.
  - Shape: closed polyline (0,0) → (0,W) → (T,W−h) → (T,h), with h = T·tan35°.
  - The front view then gets two lines, at y = h and at y = W − h.
  - Each bevel gets its own 55° dimension: one below-left as above, and one mirrored above-left.
  - Confirmed by the user on 019030(50x40x2).
- **2 chamfers (Italian Style):** a rectangle with 0.5 x 0.5 chamfers on both bottom corners: (0,0.5) → (0,W) → (T,W) → (T,0.5) → (T−0.5,0) → (0.5,0) → close.

## Dimensions (all on layer `Dimensions`)

| Dimension | Type | Between | Placement |
|---|---|---|---|
| L | linear horizontal | bottom-right → bottom-left corner | 3.86 below the knife |
| W | linear vertical | top-left → bottom-left corner | 6.14 left of the knife |
| e | linear vertical | (left) hole centre → bottom-left corner | 2.28 left of the knife |
| a (2-hole knives only) | linear horizontal | hole centre → hole centre | 3.86 below the knife. L then moves out to 7.72 below. Confirmed by the user. |
| Ø d | diameter | the hole | leader up and to the right |
| T | linear horizontal | side view bottom corners | same line as L (3.86 below) |
| 55° | angular | side-view vertical face ↔ bevel line | below-left of the side view (35° bevel only) |

## Grid of several knives

The example spaces knives 65.45 apart in x and 50.66 apart in y, so each knife fits a cell of about 65 x 50.

Knives are drawn as plain geometry, not blocks. The unused blocks in the example file are leftovers.

## CADCraft procedure notes

- Draw the geometry on layer `0`. Before dimensioning:
  - run `layer.current {name:"Dimensions"}` and `dimstyle.current {name:"Height.Dims"}`;
  - after creating the dimensions, run `dimoverride {handles, textHeight: 1}`;
  - finally switch back to layer `0`.
- **55° angular dimension:** use `dimangular {vertex, p1, p2, at}` with the vertex at the sharp seat corner (0,0) of the side view.
  - Take p1 straight **down** from the vertex, (0, −k).
  - Take p2 on the bevel's extension **down-left**, (−T, −T·tan35°).
  - Put `at` below-left of the side view.
  - Points on the knife itself (up / up-right) with `at` below-left give a 305° dimension.
- Don't copy dimensions between knives with `copy`. The copies keep their association to the original geometry and can render wrongly. Create fresh dimensions instead.
- Saving to `.dwg` writes DWG 2018 (AC1032).
