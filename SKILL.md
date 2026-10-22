---
name: woodworking-tool-parts
description: Knowledge of the components used to design woodworking cutting tools (κοπτικά εργαλεία ξύλου) — tool bodies, brazed carbide/PCD tips, and screwed-on reversible knives (ξυράφια) with their TIGRA catalog codes and dimensions — and how to draw them in CADCraft (live or headless). Use whenever the user mentions a knife/ξυράφι code (e.g. 012011), asks which knife fits a tool, or asks to design or draw a cutter head, shank tool (κονδύλι) or bore tool.
---

# Woodworking tool parts (Εξαρτήματα κοπτικών εργαλείων)

## Domain overview

We manufacture woodworking cutting tools.

- **Body (στέλεχος):** usually steel (σίδερο), or the harder TIGRAMED.
- **Cutting edges** go on the body in one of three ways:
  - **Brazed carbide (κολλητά καρβίδια):** carbide tips brazed onto the body.
  - **Brazed PCD (κολλητά διαμάντια):** polycrystalline diamond tips brazed onto the body.
  - **Screwed reversible knives (βιδωτά ξυράφια).** There are two kinds:
    - **Standard knives (standard ξυράφια):** mounted on the tool exactly as supplied, with a straight cutting edge and no reshaping. See `references/knives-standard-reversible.md`.
    - **Custom knives (custom ξυράφια)**, catalog name "Blanks for profiling" (TIGRA cat. pp. 44–51): blanks that we grind to the required profile on profile-grinding machines (e.g. WALDER), so the knife cuts that profile into the wood. The required profile decides which blank is used. See `references/knives-custom-blanks.md`.
- **Mounting type:**
  - **Shank tool (κονδύλι):** the tool has a shank.
  - **Bore tool (για άξονα με τρύπα / bore):** the tool has a bore and mounts on an arbor.

## How we refer to knives

Always write the **T04F-CR code followed by L x W x T in parentheses, with a decimal point (never a comma)**:

`012011(25x12x1.5)` · `041075(25x20.4x2)`

Drop trailing zeros (25.0 → 25, 2.0 → 2) and keep real decimals (20.4 → 20.4). This applies to standard and custom knives alike.

## Reference files

| Topic | File |
|---|---|
| Standard reversible knives (Standard ξυράφια), TIGRA cat. p.24 | `references/knives-standard-reversible.md` |
| Custom knives / Blanks for profiling (Custom ξυράφια), TIGRA cat. pp.44–51 | `references/knives-custom-blanks.md` |
| How to draw a knife (views, layers, dimensions) in CADCraft | `references/drawing-knives.md` |

More categories will be added one at a time.

## Supplier catalog

TIGRA Woodworking Catalog 2023 (`_TIGRA´s Woodworking Catalog 2023 with bookmarks.pdf`). **"Page N" always means the page number printed in the catalog**, not the PDF page index. Each PDF page is a two-page spread: catalog page 24 is the left half of PDF page 14. The user's bookmarks in the PDF carry Greek category names (STANDART ΞΥΡΑΦΙΑ, ΕΛΙΚΟΕΙΔΗ SPT030, ΠΡΟΧΑΡΑΞΕΙΣ, ΓΩΝΙΟΣΠΑΣΕΙΣ …).

**Scope rule:** the skill contains only the parts the user actually works with. The catalog holds much more. Never suggest or use a catalog item that isn't listed in `references/`. If nothing listed fits, say so and ask.

## Carbide grade

Use grade **T04F-CR** for both standard and custom knives. It is the only column we order from.

## Drawing

Use CADCraft through the `cadcraft-live` MCP tools (user watching) or the `cadcraft` tools (headless). Both take the same commands. Units are mm. Drawing rules per component will be added as each one is taught.
