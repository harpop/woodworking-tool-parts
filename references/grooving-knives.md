# Grooving knives (Γκινισιές)

Screwed carbide inserts that cut a **groove (αυλάκι)** in the wood. A typical example is the groove for the sealing rubber (λάστιχο μόνωσης) in a window frame (κούφωμα). They come in several shapes and sizes. The **groove width is the width of the cutting edge**, which is T for all knives here except the seal-seat inserts (3 mm).

Sources:

- **TIGRA** Woodworking Catalog 2023, **page 31** (PDF page 17, right half), block "Spurs, grooving knives". The codes are in the **T07MF-CR** grade column.
- **STARK** catalog (`stark.old.catalog.pdf`), **page 225**: "Grooving inserts" (48 x T x 16) and the seal-seat inserts (30/38 x 14 x 10.5). The STARK catalog gives no grade. Don't record one.

Geometry learned from the user's file `Grooving Knives.dwg`.

## Range

### TIGRA (grade T07MF-CR)

| Code | L | W | T | Cutting edges | Reference form |
|---|---|---|---|---|---|
| 013293 | 18 | 18 | 1.95 | 4 | 013293(18x18x1.95) |
| 013291 | 18 | 18 | 2.45 | 4 | 013291(18x18x2.45) |
| 013305 | 18 | 18 | 2.95 | 4 | 013305(18x18x2.95) |
| 013289 | 18 | 18 | 3.70 | 4 | 013289(18x18x3.7) |
| 053640 | 24.5 | 13 | 4 | 1 | 053640(24.5x13x4) |
| 053641 | 24.5 | 13 | 5 | 1 | 053641(24.5x13x5) |
| 013277 | 34 | 16 | 3 | 2 | 013277(34x16x3) |
| 013278 | 34 | 16 | 4 | 2 | 013278(34x16x4) |
| 013279 | 34 | 16 | 5 | 2 | 013279(34x16x5) |

TIGRA knives use the normal knife rule: code + `LxWxT`, decimal point, no trailing zeros (3.70 → 3.7).

### STARK (no grade)

| Code | Catalog size | T (groove width) | Hand | Cutting edges | Reference form |
|---|---|---|---|---|---|
| 600701 | 48x3x16 | 3 | DX | 2 | 600701(48x3x16-DX) |
| 600702 | 48x3x16 | 3 | SX | 2 | 600702(48x3x16-SX) |
| 600703 | 48x4x16 | 4 | DX | 2 | 600703(48x4x16-DX) |
| 600704 | 48x4x16 | 4 | SX | 2 | 600704(48x4x16-SX) |
| 600705 | 48x5x16 | 5 | DX | 2 | 600705(48x5x16-DX) |
| 600706 | 48x5x16 | 5 | SX | 2 | 600706(48x5x16-SX) |
| 600707 | 48x6x16 | 6 | DX | 2 | 600707(48x6x16-DX) |
| 600708 | 48x6x16 | 6 | SX | 2 | 600708(48x6x16-SX) |
| 600724 | 30x14x10.5, type B | 3 | DX | 1 | 600724(30x14x10.5-DX) |
| 600728 | 30x14x10.5, type B | 3 | SX | 1 | 600728(30x14x10.5-SX) |
| 600723 | 38x14x10.5, type A | 3 | DX | 1 | 600723(38x14x10.5-DX) |
| 600727 | 38x14x10.5, type A | 3 | SX | 1 | 600727(38x14x10.5-SX) |

- **STARK keeps its own dimension order**, as printed in its catalog (confirmed by the user). Don't convert it to LxWxT. In `48x3x16` the middle number is T (the groove width). The hand goes after a dash: `-DX` / `-SX`.
- **DX** = right hand (rh), **SX** = left hand (lh). SX is always the mirror image of DX (mirror about x = 0).
- **48 is the diagonal**, tip to tip: the distance between the outer tip corners (−22.8144, −7.45) and (22.8144, 7.45) is 48.000. The plan view is 45.63 long and **15.9** high. Draw it like that. Don't stretch it to 48 x 16 (confirmed by the user).
- **30/38 x 14 x 10.5** are the inserts for seal seats (έδρα λάστιχου). The drawn view is 30 (or 38) x 10.5. The 14 is the dimension across the view and is not drawn. There is no plan view. They cut a **3 mm** groove.
- **Selection:** the groove width decides the knife (T, or 3 mm for the seal-seat inserts). For the STARK knives the tool's hand also decides between DX and SX.
- These 21 knives are the complete list. Anything else on TIGRA page 31 or STARK page 225 is out of scope.

## Views and conventions

- **Plan view (κάτοψη)** and **side view (πλάγια όψη)**. The side view looks at the knife edge-on: its x axis is the same as the plan's x axis, and its y axis is the thickness T.
- **Base point:** the hole centre (0, 0) for all knives, except the seal-seat inserts. Their base point is the bottom corner at the end opposite the cutting tip (bottom right for DX, bottom left for SX).
- Coordinates below are in mm at 1:1, for the **DX** hand where there is one. Arcs run counter-clockwise from the first angle to the second.
- **Cutting edge (κόψη):** the user marked it in magenta, **always in the side view (or the single view)**. It is the end face of the tip, as wide as the groove. Nothing is marked in the plan view. The magenta is knowledge only: draw every line **ByLayer**.

## 18x18 (TIGRA 013293, 013291, 013305, 013289)

A square insert with **4 identical cutting corners**. Each side has an R3 relief notch next to a small tooth. The knife is indexed by turning it 90°.

**Draw 18 x 18 (outer faces at ±9)**, as the user decided. The source DWG has 17.98 (±8.99). The coordinates below are already corrected: every ±8.99 became ±9 and the chamfer line at ±8.79 became ±8.8. Nothing else moves.

### Plan view (same for all 4)

- **Hole:** three concentric circles: **Ø10.25**, **Ø10.65**, **Ø12.1**.
- **One side (the right side, x = +9).** The other three sides are this set rotated by 90°, 180° and 270° counter-clockwise about (0, 0):
  - A centre (9.55, 5.25), R3, 122.449°→230° (relief notch, from (7.9403, 7.7816) to (7.6216, 2.9519))
  - L (7.6216, 2.9519) → (9, 1.8037)
  - L (9, 1.8037) → (9, −5.507) (outer face)
  - L (9, −5.507) → (8.4605, −8.51) (tooth)
  - L (8.4605, −8.51) → (7.7816, −7.9403)
  - L (8.8, 1.9715) → (8.8, −6.6413) (edge of the 0.2 chamfer, seen from above)
- 4 x 6 entities + 3 circles = 27 entities.

### Side view (t = T/2)

- **Outline:** top face y = +t and bottom face y = −t, from x −8.8 to 8.8. End faces x = ±9 from y −(t − 0.2) to +(t − 0.2). Four 0.2 x 45° chamfers join them, e.g. (8.8, t) → (9, t − 0.2).
  - **Exception, 2.45:** the chamfer is 0.215: faces end at x ±8.785 and the end faces span ±1.01.
- **Cutting edge:** at **each** end, the end face plus its two chamfers.
- **Hole in section:** a countersink on both faces with a small step in the middle. With the levels a, b, c from the table:
  - Top countersink: L (±6.05, t) → (±5.325, a).
  - L (±5.325, a) → (±5.325, b); horizontals y = a and y = b from x −5.325 to 5.325.
  - L (±5.125, b) → (±5.125, c); horizontal y = c from x −5.125 to 5.125.
  - Bottom countersink: L (±5.125, c) → (±6.05, −t).

| T | t | a | b | c |
|---|---|---|---|---|
| 1.95 | 0.975 | 0.25 | 0.05 | −0.05 |
| 2.45 | 1.225 | 0.5 | 0.25 | −0.3 |
| 2.95 | 1.475 | 0.75 | 0.55 | −0.55 |
| 3.70 | 1.85 | 1.125 | 0.925 | −0.925 |

(a = t − 0.725, c = −(t − 0.925), b = a − 0.2, except 2.45 where b = a − 0.25.)

## 24.5x13 (TIGRA 053640, 053641)

A rectangular seat with chamfered corners and a hole on the right, and **one cutting tip** on the left reaching x = −18. It has **1 cutting edge** and is not reversible. Overall x −18..6.5 (24.5), y −6.5..6.5 (13).

### Plan view (same for both)

- C centre (0, 0), Ø7.6
- C centre (0, 0), Ø11
- A centre (−7, −3.5), R10, 90°→92.4846° (from (−7, 6.5) to (−7.4335, 6.4906); a polyline in the DWG)
- A centre (−7, −3.5), R10, 93.33°→175.494°
- A centre (−9.4185, −4.173), R2, 10°→110°
- L (−12.4079, −3.1327) → (−10.1025, −2.2936)
- L (−12.4079, −3.1327) → (−12.7348, −3.8336)
- L (−12.7348, −3.8336) → (−18, −5.75)
- L (−13.0759, −1.2973) → (−12.4079, −3.1327)
- L (−17.2101, −2.8021) → (−13.0759, −1.2973)
- L (−18, −5.75) → (−17.2101, −2.8021)
- L (−6.0846, −6.1) → (−6.4223, −6.5)
- L (−6.0846, −6.1) → (4.6343, −6.1)
- L (−6.4429, −6.5) → (−7.5809, −0.0457)
- L (−7, 6.5) → (4.8, 6.5)
- L (−7.0475, 6.1) → (−7.1205, −0.0093)
- L (−7.1205, −0.0093) → (−6.0846, −6.1)
- L (−7.1205, −0.0093) → (−7.5809, −0.0457)
- L (−7.4335, 6.4906) → (−7.0475, 6.1)
- L (−7.4488, −3.8257) → (−6.9773, −6.5)
- L (−7.5809, −0.0457) → (−7.5809, 6.4831)
- L (−7.5809, 6.4831) → (−7.4335, 6.4906)
- L (4.6343, −6.1) → (4.8, −6.5)
- L (4.6343, −6.1) → (6.1, −4.6343)
- L (4.6343, 6.1) → (−7.0475, 6.1)
- L (4.6343, 6.1) → (4.8, 6.5)
- L (4.8, −6.5) → (−6.9773, −6.5)
- L (4.8, 6.5) → (6.5, 4.8)
- L (6.1, −4.6343) → (6.1, 4.6343)
- L (6.1, −4.6343) → (6.5, −4.8)
- L (6.1, 4.6343) → (4.6343, 6.1)
- L (6.1, 4.6343) → (6.5, 4.8)
- L (6.5, −4.8) → (4.8, −6.5)
- L (6.5, 4.8) → (6.5, −4.8)

### Side view

Listed for **T = 4**. For T = 5, add (T − 4)/2 = 0.5 to the size of every y ≠ 0 (y > 0 → y + 0.5, y < 0 → y − 0.5), arc centres included. x stays the same.

- A centre (−6.7208, −80.9454), R79.318, 90.526°→92.444°
- A centre (−6.7208, 80.9454), R79.318, 267.556°→269.474°
- L (−10.1025, 1.6996) → (−10.1025, −1.6996)
- L (−12.4079, −1.7852) → (−10.1025, −1.6996)
- L (−12.4079, −2) → (−12.4079, 2)
- L (−12.4079, −2) → (−18, −2)
- L (−12.4079, 1.7852) → (−10.1025, 1.6996)
- L (−12.4079, 2) → (−18, 2)
- L (−12.7348, −2) → (−12.7348, 2)
- L (−18, −2) → (−18, 2) · **cutting edge**
- L (−6.0846, 2.05) → (−6.4223, 1.65)
- L (−6.4223, 1.65) → (−6.4429, 1.6297)
- L (−6.4414, −1.65) → (−6.0747, −2.05)
- L (−6.4414, −1.65) → (6.5, −1.65)
- L (−6.4628, −1.6304) → (−6.4414, −1.65)
- L (−6.9773, −1.6472) → (−6.4628, −1.6304)
- L (−6.9773, 1.6472) → (−6.4429, 1.6297)
- L (−6.9773, 1.6472) → (−6.9773, −1.6472)
- L (−7.1086, −2.05) → (−7.5579, −1.6297)
- L (−7.1205, 2.05) → (−7.5412, 1.6297)
- L (−7.1205, 2.05) → (6.1, 2.05)
- L (−7.4488, −1.6308) → (−6.9773, −1.6472)
- L (−7.4488, 1.6308) → (−6.9773, 1.6472)
- L (−7.4488, 1.6308) → (−7.4488, −1.6308)
- L (4.6343, −2.05) → (4.8, −1.65)
- L (4.6343, 2.05) → (4.8, 1.65)
- L (4.8, −1.65) → (4.8, 1.65)
- L (6.1, −2.05) → (−7.1086, −2.05)
- L (6.1, −2.05) → (6.5, −1.65)
- L (6.1, 2.05) → (6.5, 1.65)
- L (6.5, 1.65) → (−6.4223, 1.65)
- L (6.5, 1.65) → (6.5, −1.65)

Note: as drawn, the cutting tip is exactly T thick (±T/2) and the body is 0.1 thicker (±(T/2 + 0.05)).

## 34x16 (TIGRA 013277, 013278, 013279)

A parallelogram insert with **two cutting tips**, at x = −17 and x = +17. It has **2 cutting edges** and is reversible by turning 180°. The plan is point-symmetric about the hole centre. Overall ±17 x ±8.

### Plan view (same for all 3)

- C centre (0, 0), Ø8.6
- C centre (0, 0), Ø10.7
- A centre (−11.0451, −3.4415), R1, 357.498°→4.229°
- A centre (−8.7514, −3.2719), R1.3, 15°→184.229°
- A centre (11.0451, 3.4415), R1, 177.498°→184.229°
- A centre (8.7514, 3.2719), R1.3, 195°→4.229°
- L (−13.7075, 4.7877) → (−8.1436, 8)
- L (−17, −7.5) → (−10.0461, −3.4851)
- L (−17, −7.5) → (−13.7075, 4.7877)
- L (−5.2373, 7.5) → (6.2726, 7.5)
- L (−6.1386, −8) → (8.1436, −8)
- L (−6.2726, −7.5) → (5.2373, −7.5)
- L (−7.4957, −2.9354) → (−6.1386, −8)
- L (−7.8681, −2.3181) → (−5.1033, 8)
- L (−8.1436, 8) → (6.1386, 8)
- L (10.0461, 3.4851) → (17, 7.5)
- L (17, 7.5) → (13.7075, −4.7877)
- L (5.1033, −8) → (7.8681, 2.3181)
- L (7.4957, 2.9354) → (6.1386, 8)
- L (8.1436, −8) → (13.7075, −4.7877)

### Side view

Listed for **T = 3**. For T = 4 and 5, add (T − 3)/2 to the size of every y ≠ 0, as for the 24.5x13. Checked against the DWG for all three.

- A centre (−8.6511, 15.9699), R14.736, 264.568°→272.685°
- A centre (−8.739, −12.3051), R11.0824, 85.974°→96.773°
- A centre (8.6511, 15.9699), R14.736, 267.315°→275.432°
- A centre (8.739, −12.3051), R11.0824, 83.227°→94.026°
- L (−10.0461, −1.3) → (−10.0461, 1.3)
- L (−17, −1.5) → (−10.0461, −1.3)
- L (−17, −1.5) → (−17, 1.5) · **cutting edge**
- L (−17, 1.5) → (−10.0461, 1.3)
- L (−6.1386, −1) → (−6.1386, 1)
- L (−6.1386, −1) → (−6.2324, −1.55)
- L (−6.1386, 1) → (−6.2324, 1.55)
- L (−7.9609, −1.55) → (−7.9609, 1.55)
- L (13.7075, −1.05) → (13.7075, 1.05)
- L (13.7075, −1.05) → (8.1436, −0.9)
- L (13.7075, 1.05) → (8.1436, 0.9)
- L (17, −1.5) → (10.0461, −1.3)
- L (17, −1.5) → (13.7075, −1.05)
- L (17, −1.5) → (17, 1.5) · **cutting edge**
- L (17, 1.5) → (10.0461, 1.3)
- L (17, 1.5) → (13.7075, 1.05)
- L (5.0899, −1.55) → (5.1837, −1)
- L (5.1837, −1) → (−6.1386, −1)
- L (5.1837, −1) → (5.1837, −0.9)
- L (5.1837, 1) → (−6.1386, 1)
- L (5.1837, 1) → (5.0899, 1.55)
- L (5.1837, 1) → (5.1837, 0.9)
- L (7.9609, −1.25) → (5.1837, −0.9)
- L (7.9609, −1.55) → (−7.9609, −1.55)
- L (7.9609, −1.55) → (7.9609, −1.25)
- L (7.9609, 1.25) → (5.1837, 0.9)
- L (7.9609, 1.25) → (7.9609, 1.55)
- L (7.9609, 1.55) → (−7.9609, 1.55)
- L (8.1436, −0.9) → (5.1837, −0.9)
- L (8.1436, −0.9) → (8.1436, 0.9)
- L (8.1436, 0.9) → (5.1837, 0.9)

Note: as drawn, the cutting tips are exactly T thick (±T/2) and the body is 0.1 thicker (±(T/2 + 0.05)).

## 48 x T x 16 (STARK 600701–600708)

A parallelogram insert with a carbide tip at each end: **2 cutting edges**, reversible by turning 180°. Point-symmetric about the hole centre. Overall 45.63 x 15.9; the catalog's 48 is the tip-to-tip diagonal.

Per thickness (B = body thickness, D = countersink diameter):

| T | t = T/2 | B | b = B/2 | D | h (countersink bottom) |
|---|---|---|---|---|---|
| 3 | 1.5 | 2 | 1 | 9.6 | −0.7 |
| 4 | 2 | 3 | 1.5 | 10.8 | −0.8 |
| 5 | 2.5 | 4 | 2 | 10.8 | −0.3 |
| 6 | 3 | 4 | 2 | 11.2 | −0.5 |

(h = b − (D − 6.2)/2. The countersink is on the top face only.)

### Plan view, DX (same for every T except the ØD circle)

- C centre (0, 0), Ø6.2
- C centre (0, 0), **ØD**
- L (−12.7101, −4.95) → (−20.7167, −4.95)
- L (−12.7101, −7.95) → (−12.7101, −4.95)
- L (−12.7101, −7.95) → (9.3857, −7.95)
- L (−14.7885, −7.45) → (−12.7101, −6.25)
- L (−20.7167, −4.95) → (−22.8144, −7.45)
- L (−22.8144, −7.45) → (−14.7885, −7.45)
- L (−9.3857, 7.95) → (−20.2101, −4.95)
- L (12.7101, 4.95) → (20.7167, 4.95)
- L (12.7101, 7.95) → (−9.3857, 7.95)
- L (12.7101, 7.95) → (12.7101, 4.95)
- L (14.7885, 7.45) → (12.7101, 6.25)
- L (20.7167, 4.95) → (22.8144, 7.45)
- L (22.8144, 7.45) → (14.7885, 7.45)
- L (9.3857, −7.95) → (20.2101, 4.95)

### Side view, DX (t, b, D, h from the table; ± means one line at + and one at −)

- **Left tip (x −22.8144..−12.7101):**
  - L (−22.8144, −t) → (−22.8144, t) · **cutting edge**
  - L (−22.8144, ±t) → (−14.7885, ±t)
  - L (−14.7885, −t) → (−14.7885, t)
  - L (−14.7885, ±t) → (−12.7101, ±(t − 0.0839))
  - L (−12.7101, −(t − 0.0839)) → (−12.7101, t − 0.0839)
- **Body:**
  - L (−12.7101, ±b) → (9.3857, ±b)
  - L (9.3857, −b) → (9.3857, b)
  - L (9.3857, ±b) → (20.2101, ±b)
  - L (20.2101, −b) → (20.2101, b)
- **Right tip (x 12.7101..22.8144):**
  - L (22.8144, −t) → (22.8144, t) · **cutting edge**
  - L (14.7885, ±t) → (22.8144, ±t)
  - L (14.7885, ±b) → (14.7885, ±t)
  - L (14.7885, ±t) → (12.7101, ±(t − 0.0839))
  - L (12.7101, ±b) → (12.7101, ±(t − 0.0839))
  - L (12.7101, ±(t − 0.1748)) → (20.7167, ±(t − 0.1748))
  - L (20.7167, −(t − 0.1748)) → (20.7167, t − 0.1748)
  - L (20.7167, ±(t − 0.1748)) → (22.8144, ±t)
- **Hole (Ø6.2, countersunk from the top face):**
  - L (±3.1, −b) → (±3.1, h)
  - L (−3.1, h) → (3.1, h)
  - L (±3.1, h) → (±D/2, b)

**SX:** mirror every DX entity about x = 0, in both views.

## Seal-seat inserts 30/38 x 14 x 10.5 (STARK 600724, 600728, 600723, 600727)

A block 10.5 high with a **3 mm wide tongue** at one end that cuts the seal groove. **1 cutting edge:** the end face of the tongue. Only this one view exists. The hole lines (Ø6.2 with a 45° countersink to Ø11.5, centre 9 from the base-point end) are drawn in linetype **CENTER**, as in the DWG.

Base point (0, 0) = bottom corner opposite the tongue. DX listed; **SX = mirror about x = 0**.

### 30x14x10.5-DX (600724)

- A centre (−23.3453, 9.5), R1, 270°→330°
- A centre (−26.0392, 4.9), R0.6, 330°→90°
- A centre (−29.1261, 6.025), R10.5128, 0°→25.193°
- L (0, 0) → (0, 10.5)
- L (0, 10.5) → (−21.6132, 10.5)
- L (−22.4793, 9) → (−21.6132, 10.5)
- L (−23.3453, 8.5) → (−30, 8.5)
- L (−30, 8.5) → (−30, 5.5) · **cutting edge**
- L (−26.0392, 5.5) → (−30, 5.5)
- L (−28.1754, 0) → (−25.5196, 4.6)
- L (−28.1754, 0) → (0, 0)
- L (−18.6132, 0) → (−18.6132, 6.025) (inner line; continues as the R10.5128 arc to the top face)
- Hole, linetype CENTER:
  - L (−12.1, 0) → (−12.1, 7.85)
  - L (−5.9, 0) → (−5.9, 7.85)
  - L (−12.1, 7.85) → (−5.9, 7.85)
  - L (−14.75, 10.5) → (−12.1, 7.85)
  - L (−3.25, 10.5) → (−5.9, 7.85)

### 38x14x10.5-DX (600723)

- A centre (−22, 9.8412), R1, 0°→41.212°
- A centre (−23.6144, 9.1), R0.6, 270°→330°
- A centre (−33.5, 5), R0.5, 0°→90°
- L (0, 0) → (0, 10.5)
- L (0, 10.5) → (−22.1132, 10.5)
- L (−23.0947, 8.8) → (−22.1132, 10.5)
- L (−23.6144, 8.5) → (−38, 8.5)
- L (−38, 8.5) → (−38, 5.5) · **cutting edge**
- L (−33.5, 5.5) → (−38, 5.5)
- L (−33, 0) → (−33, 5)
- L (−33, 0) → (0, 0)
- L (−21, 0) → (−21, 9.8412) (inner line; continues as the R1 arc to the top face)
- Hole, linetype CENTER: the same 5 lines as the 30x14x10.5.

## How the user draws them (`Grooving Knives.dwg`)

Same layout as the edge forming knives:

- Each knife is a **block named after its drawing title** (e.g. `18x18x1.95`, `48x3x16(DX)`), units mm. The block description holds the code.
- All except the seal-seat inserts are **dynamic blocks** with two visibility states, `Top` (plan view) and `Side` (side view). Each is inserted twice: the side view **40 mm above** the plan view at 1:1.
- The seal-seat inserts are plain blocks with one view.
- The file is a parts table (BOM) on layer `BOM`, blocks inserted at **scale 0.5**. Cells are 26.81 wide. Under the views, two MText lines, style `BOM_TXT`, height 2, at x = cell left + 2: the drawing title (e.g. `48x3x16(DX)`), and below it the code.
- **CADCraft:** exploding these blocks shows **both** visibility states on top of each other. To read them separately, save the drawing as DXF and use the `BLOCKVISIBILITYPARAMETER` state lists. When drawing a new one, draw plain geometry at 1:1 from the coordinates above (plan view, side view 40 mm above it), not a dynamic block.
