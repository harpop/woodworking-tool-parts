# woodworking-tool-parts

Skill (Agent Skills, `SKILL.md`) με γνώση για τα εξαρτήματα κοπτικών εργαλείων ξύλου: ξυράφια (standard και custom blanks) και γωνιοσπάσεις με κωδικούς και διαστάσεις, και κανόνες σχεδίασής τους σε CADCraft.

**Έκδοση: 1.1.0**

## Εγκατάσταση

Δώστε το link αυτού του repo στην AI σας (Claude Code ή Codex) και ζητήστε: «Εγκατέστησε αυτό το skill με git clone».

Οδηγίες για την AI: κάνε `git clone` αυτού του repo **απευθείας** ως φάκελο `woodworking-tool-parts` μέσα στον φάκελο skills, ώστε το `SKILL.md` να βρίσκεται στη ρίζα του:

| Εργαλείο | Φάκελος |
|---|---|
| Claude Code | `~/.claude/skills/woodworking-tool-parts` (Windows: `%USERPROFILE%\.claude\skills\woodworking-tool-parts`) |
| Codex | ο φάκελος skills του Codex, π.χ. `~/.codex/skills/woodworking-tool-parts` |

Μετά την εγκατάσταση, ανοίξτε νέα συζήτηση.

## Ενημέρωση

Ζητήστε από την AI: «Ενημέρωσε το skill woodworking-tool-parts από το GitHub». Αυτό σημαίνει `git pull` μέσα στον φάκελο του skill. Μετά ανοίξτε νέα συζήτηση.

## Απαιτήσεις

- Για τη σχεδίαση χρειάζεται το CADCraft με τον MCP server του (`cadcraft-live` ή `cadcraft`).
- Ο κατάλογος TIGRA (PDF) **δεν** περιλαμβάνεται. Οι πίνακες με κωδικούς και διαστάσεις που χρειάζεται το skill βρίσκονται στο `references/`.

## Αλλαγές

- **1.1.0**: Γωνιοσπάσεις / Edge forming knives (TIGRA σελ. 36, 7 κωδικοί T10MG) με γεωμετρία κάτοψης και πλάγιας όψης. Πίνακας «Γνωστά εξαρτήματα» στο `SKILL.md`. Ενότητα «Scope»: το skill καλύπτει μόνο τι εξαρτήματα υπάρχουν και πώς σχεδιάζονται. Η τοποθέτηση σε προφίλ θα γίνει ξεχωριστό skill.
- **1.0.0**: Πρώτη έκδοση. Standard ξυράφια (TIGRA σελ. 24), custom ξυράφια / Blanks for profiling (TIGRA σελ. 44–51), σχεδίαση ξυραφιών σε CADCraft.
