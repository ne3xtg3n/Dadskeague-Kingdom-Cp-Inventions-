Dadskeague Kingdom Back yard Build by Chris Perry

### Revised GitHub Repository Structure
```
dads-league-kingdom/
├── README.md
├── LICENSE
├── project.config.json
├── plans/
│   ├── structure.md
│   ├── electrical.md
│   ├── plumbing_hvac.md
│   ├── deck.md
│   ├── portability.md
│   └── figures/
│       ├── fig-01_exterior-deck-elevation.svg
│       ├── fig-02_interior-perspective.svg
│       ├── fig-03_loft-section.svg
│       ├── fig-04_floor-plan_20x20.svg
│       └── fig-05_power-single-line.svg
├── bom/
│   ├── bill_of_materials.csv
│   └── cost_breakdown.md
├── permit/
│   ├── notes_for_ahj.md
│   └── compliance_checklist.md
├── deck/
│   ├── trex_layout_16x20.md
│   └── deck_assembly_guide.md
├── construction/
│   ├── sequence.md
│   └── safety_guidelines.md
├── upgrades/
│   └── future_upgrades.md
├── cad/
│   ├── 3d_model.skp
│   └── 2d_drawings.dwg
└── .github/
    └── workflows/
        └── validate.yml
```

### File Contents

#### README.md
```markdown
# Dad’s League Kingdom — Portable Loft Bar House
**20 × 20 ft Interior · 15 ft Vaulted Ceiling · 10 × 20 ft Queen Loft · Detachable 16 × 20 Trex Deck**  
**Version 3.1  |  Author: Christopher Perry  |  2025-10-07**

A luxury micro-lodge built for dads who want a portable, high-end retreat. Skid-based for easy moves, finished with a black metal roof, board-and-batten siding, and a flip-up bar window. Features a walnut bar, LED-lit loft, and a Trex deck for grilling and chilling. This repo has everything you need to build it: plans, BOM, figures, and permitting notes.

## 🔑 Key Specs
- **Footprint**: 20′ × 20′ (400 ft²) clear interior
- **Height**: 15′ ridge (~7′ to loft floor; ~8′ clear below)
- **Loft**: 10′ × 20′ (200 ft², queen bed + storage)
- **Deck**: 16′ × 20′ Trex (Rocky Harbor), modular, detachable
- **Exterior**: Black Onyx LP SmartSide, faux stone base, bronze door
- **Bar**: 7′ flip-up window (gas struts), walnut counter, bottle opener, kegerator-ready
- **Power**: 30A L14-30 inlet → 8-space subpanel (neutral isolated)
- **HVAC**: 9,000 BTU mini-split (240V)
- **Portability**: 6×6 PT skids, forklift pockets, ≤13′6″ on trailer
- **Dad Features**: Outdoor speaker mounts, cornhole storage, dartboard shelf
- **Cost**: ~$17,500 USD (DIY, 2025 estimate)

## 📁 Repository Layout
```
dads-league-kingdom/
├── README.md
├── LICENSE
├── project.config.json
├── plans/
│   ├── structure.md
│   ├── electrical.md
│   ├── plumbing_hvac.md
│   ├── deck.md
│   ├── portability.md
│   └── figures/
│       ├── fig-01_exterior-deck-elevation.svg
│       ├── fig-02_interior-perspective.svg
│       ├── fig-03_loft-section.svg
│       ├── fig-04_floor-plan_20x20.svg
│       └── fig-05_power-single-line.svg
├── bom/
│   ├── bill_of_materials.csv
│   └── cost_breakdown.md
├── permit/
│   ├── notes_for_ahj.md
│   └── compliance_checklist.md
├── deck/
│   ├── trex_layout_16x20.md
│   └── deck_assembly_guide.md
├── construction/
│   ├── sequence.md
│   └── safety_guidelines.md
├── upgrades/
│   └── future_upgrades.md
├── cad/
└── .github/workflows/
    └── validate.yml
```

## 🚀 How to Use
1. Read `plans/structure.md` and `construction/sequence.md` for build steps.
2. Check `permit/notes_for_ahj.md` for local code requirements.
3. Source materials using `bom/bill_of_materials.csv`.
4. Build per `construction/sequence.md`, using figures for layout.
5. Verify compliance with `permit/compliance_checklist.md`.

**License**: MIT (see `LICENSE`). Credit Christopher Perry for derivative works.
```

#### LICENSE
```text
MIT License

Copyright (c) 2025 Christopher Perry

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

#### project.config.json
```json
{
  "project": "Dad’s League Kingdom — Portable Loft Bar House",
  "version": "3.1",
  "author": "Christopher Perry",
  "date": "2025-10-07",
  "dimensions": {
    "interior": { "width_ft": 20, "length_ft": 20, "area_ft2": 400 },
    "loft": { "width_ft": 10, "length_ft": 20, "area_ft2": 200, "floor_height_ft": 7 },
    "ceiling": { "ridge_ft": 15, "clear_below_loft_ft": 8 },
    "deck": { "width_ft": 16, "length_ft": 20, "area_ft2": 320 }
  },
  "envelope": {
    "siding": "LP SmartSide board-and-batten (Black Onyx)",
    "roof": "Standing-seam metal (Matte Black)",
    "door": "Bronze insulated exterior",
    "windows": "Black vinyl (awning/casement), 7' flip-up bar window"
  },
  "power": {
    "inlet": "L14-30 30A, 120/240V",
    "subpanel_spaces": 8,
    "feeder": "10/4 Cu THWN in PVC",
    "grounding": "Two 8' rods, #6 Cu"
  },
  "hvac": { "type": "Mini-split heat pump", "btus": 9000, "voltage": "240V" },
  "plumbing": { "sink": "Bar sink, 15-20 gal gray tank", "features": "PEX quick-disconnects, exterior hose bib" },
  "portability": { "skids": "6x6 PT (3 rows)", "fork_points": true, "max_trailer_height_in": 162, "weight_lb": 10800 },
  "dad_features": [
    "Wall-mounted bottle opener",
    "Kegerator-ready plumbing",
    "Fold-down dartboard shelf",
    "Outdoor speaker mounts",
    "Cornhole storage nook"
  ]
}
```

#### plans/structure.md
```markdown
# Structural Plan

## Foundation / Base
- (3) 6×6 PT skid beams, 20′ length, spaced at ~0′, ~8′, ~16′
- 4×4 PT cross-blocking @ 48″ OC
- Steel fork/rollback pick points at corners + midspan
- Moisture barrier (6 mil poly) between skids and floor

## Floor
- 2×8 PT joists @ 16″ OC, Simpson hangers to rim
- 3/4″ Advantech T&G subfloor, adhesive + 2″ screws
- Seal edges; roll-on waterproofing at door/bar threshold

## Walls
- 2×6 SPF studs @ 16″ OC, double top plate
- 7/16″ ZIP System sheathing, taped seams
- Bar window header: double 2×10 with jack studs, hurricane straps

## Roof
- 5/12 gable pitch, 2×8 rafters, ridge board
- Hurricane ties at rafters; collar ties every other bay
- Synthetic underlayment + ice shield, 26 ga standing-seam metal (Matte Black)
- Vented ridge, soffit vents for airflow

## Loft
- 2×6 joists spanning 20′, bearing on ledgers + 4×4 posts
- Loft floor at ~7′ A.F.F. (~8′ clear below)
- 3/4″ Advantech deck, steel/wood guardrail with LED strip
- Alternating tread stair (32″ wide, 10″ treads), bolted, removable
```

#### plans/electrical.md
```markdown
# Electrical Plan

**Service**: 30A 120/240V L14-30 inlet → 8-space main-lug subpanel  
**Grounding**: Two 8′ rods, #6 Cu to ground bar, neutral isolated

## Branch Circuits
| Circuit | Breaker | Load |
|---------|---------|------|
| 1       | 15A     | Lighting (8 recessed LEDs + RGB strips, dimmable) |
| 2       | 20A     | Bar/Small Appliance (GFCI: fridge, kegerator, blender) |
| 3       | 20A     | General Receptacles (AFCI/GFCI per location) |
| 4       | 15A     | Exterior/Deck (GFCI, in-use covers) |
| 5       | 15A     | AV/TV (45″ LG TV array, surge protected) |
| 6       | 15-20A  | Mini-split (240V, per nameplate) |
| 7-8     | —       | Spares (solar/inverter tie-in) |

## Feeder / Conduit
- 10/4 Cu THWN in Schedule-40 PVC, buried 12–24″ (per AHJ)
- Upsize to 8/4 Cu if run >100 ft to limit voltage drop (≤3%)

## Protection
- Whole-panel surge protector (SPD)
- Exterior AC disconnect at mini-split
- Label panel directory and inlet clearly

**Diagram**: See `figures/fig-05_power-single-line.svg`
```

#### plans/plumbing_hvac.md
```markdown
# Plumbing & HVAC

## HVAC
- 9,000 BTU ductless mini-split heat pump (240V)
- Outdoor unit on vibration pads, 12″ above grade for snow/leaf clearance
- Condensate line to exterior or gray tank
- Line-set cover for exterior run

## Plumbing
- Bar sink with 15 gal gray tank (strap-mounted underfloor)
- PEX lines with quick-disconnects, vacuum breaker on fill
- Exterior hose bib (frost-free) for drain/wash-down
- Kegerator-ready: 1/4″ PEX stub-out with shutoff
- Optional propane quick-connect for grill (deck-mounted)

## Dad Features
- Wall-mounted bottle opener at bar
- Magnetic tool strip for bar tools (under counter)
```

#### plans/deck.md
```markdown
# Deck Plan — Trex 16×20 (Rocky Harbor)

## Framing
- Modular 4′ bolt-together sections, 2×8 PT joists @ 16″ OC
- Picture-frame rim joists, adjustable piers/feet
- Deck top flush with cabin threshold

## Surface
- Trex Enhance Naturals (Rocky Harbor), hidden fasteners
- Breaker board at 10′ for 20′ depth, picture-frame border
- Bar counter aligned with 7′ flip-up window

## Dad Features
- Outdoor speaker mounts (2, weatherproof, bolted to pergola)
- Cornhole storage nook (under-deck, lockable)
- Propane quick-connect for grill (deck edge)
- Optional pergola with LED string lights
- Propane fire table zone (right side, quick-connect)
```

#### plans/portability.md
```markdown
# Portability Plan

- **Weight**: ~10,800 lb (structure) + ~2,000 lb (deck)
- **Height**: ≤13′6″ on trailer (secure ridge cap, soffits)
- **Lift**: Forklift pockets or spreader bar at lugs
- **Disconnects**: L14-30 inlet, PEX unions, propane quick-connect
- **Secure for Transport**:
  - Remove bar window glass (store in padded crate)
  - Secure TV, loose items with straps
  - Unbolt deck in ≤2 hr, stack on pallets
- **Permits**: Oversize load (20′ width), check DOT regulations
```

#### plans/figures/fig-01_exterior-deck-elevation.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 500">
  <!-- Exterior elevation with 16x20 Trex deck, Black Onyx siding, faux stone base -->
  <rect x="60" y="360" width="780" height="30" fill="#8a8a8a"/> <!-- Deck -->
  <rect x="220" y="180" width="460" height="160" fill="#111" stroke="#333"/> <!-- Siding -->
  <rect x="220" y="340" width="460" height="20" fill="#5a5a5a"/> <!-- Stone base -->
  <rect x="250" y="210" width="210" height="60" fill="#444"/> <!-- Bar window -->
  <rect x="620" y="250" width="60" height="90" fill="#6e5a41"/> <!-- Bronze door -->
  <polyline points="220,180 450,120 680,180" fill="none" stroke="#000" stroke-width="5"/> <!-- Roofline -->
  <text x="70" y="355" fill="#fff" font-size="12">Trex Deck 16×20</text>
  <text x="252" y="205" fill="#fff" font-size="12">7' Flip-up Bar Window</text>
  <text x="622" y="245" fill="#fff" font-size="12">Bronze Door</text>
</svg>
```

#### plans/figures/fig-02_interior-perspective.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 500">
  <!-- Interior perspective: pine T&G walls, walnut bar, sectional, TV array -->
  <rect x="100" y="100" width="700" height="300" fill="#d4a373" stroke="#8b5e3c"/> <!-- Pine walls -->
  <rect x="150" y="320" width="200" height="40" fill="#3c2f2f"/> <!-- Walnut bar -->
  <rect x="500" y="300" width="250" height="80" fill="#4a3728"/> <!-- Leather sectional -->
  <rect x="300" y="150" width="150" height="90" fill="#222"/> <!-- TV array -->
  <line x1="100" y1="250" x2="800" y2="250" stroke="#aaa" stroke-width="3"/> <!-- Loft edge -->
  <text x="152" y="315" fill="#fff" font-size="12">Walnut Bar w/ LED</text>
  <text x="502" y="295" fill="#fff" font-size="12">Leather Sectional</text>
  <text x="302" y="145" fill="#fff" font-size="12">45" LG TV Array</text>
</svg>
```

#### plans/figures/fig-03_loft-section.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 500">
  <!-- Loft cross-section: 7' floor, 8' clear below, 15' ridge -->
  <rect x="140" y="110" width="620" height="320" fill="#1a1a1a" stroke="#444"/> <!-- Structure -->
  <line x1="140" y1="270" x2="760" y2="270" stroke="#aaa" stroke-width="3"/> <!-- Loft floor -->
  <rect x="600" y="270" width="40" height="60" fill="#555"/> <!-- Alternating tread stair -->
  <polyline points="140,110 450,50 760,110" fill="none" stroke="#000" stroke-width="5"/> <!-- Roofline -->
  <text x="150" y="265" fill="#fff" font-size="12">Loft Floor @ ~7' A.F.F.</text>
  <text x="150" y="125" fill="#fff" font-size="12">Ridge @ 15'</text>
  <text x="602" y="265" fill="#fff" font-size="12">Stair</text>
</svg>
```

#### plans/figures/fig-04_floor-plan_20x20.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 500">
  <!-- Floor plan: 20x20 interior, bar, sectional, TV, stair -->
  <rect x="100" y="100" width="700" height="300" fill="#d4a373" stroke="#000" stroke-width="5"/> <!-- Walls -->
  <rect x="150" y="120" width="200" height="40" fill="#3c2f2f"/> <!-- Bar -->
  <rect x="500" y="300" width="250" height="80" fill="#4a3728"/> <!-- Sectional -->
  <rect x="300" y="130" width="150" height="30" fill="#222"/> <!-- TV array -->
  <rect x="650" y="120" width="40" height="60" fill="#555"/> <!-- Stair -->
  <rect x="150" y="360" width="60" height="30" fill="#6e5a41"/> <!-- Door -->
  <text x="152" y="115" fill="#fff" font-size="12">Walnut Bar</text>
  <text x="502" y="295" fill="#fff" font-size="12">Sectional</text>
  <text x="302" y="125" fill="#fff" font-size="12">TV Array</text>
  <text x="652" y="115" fill="#fff" font-size="12">Stair to Loft</text>
</svg>
```

#### plans/figures/fig-05_power-single-line.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 900 500">
  <!-- Single-line diagram: L14-30 inlet, subpanel, circuits -->
  <rect x="100" y="200" width="100" height="60" fill="#ccc" stroke="#000"/> <!-- Inlet -->
  <rect x="300" y="150" width="150" height="200" fill="#ddd" stroke="#000"/> <!-- Subpanel -->
  <line x1="200" y1="230" x2="300" y2="230" stroke="#000" stroke-width="3"/> <!-- Feeder -->
  <line x1="450" y1="160" x2="600" y2="160" stroke="#000" stroke-width="2"/> <!-- Circuit 1 -->
  <line x1="450" y1="190" x2="600" y2="190" stroke="#000" stroke-width="2"/> <!-- Circuit 2 -->
  <line x1="450" y1="220" x2="600" y2="220" stroke="#000" stroke-width="2"/> <!-- Circuit 3 -->
  <text x="102" y="195" fill="#000" font-size="12">L14-30 Inlet</text>
  <text x="302" y="145" fill="#000" font-size="12">8-Space Subpanel</text>
  <text x="602" y="165" fill="#000" font-size="10">C1: Lighting</text>
  <text x="602" y="195" fill="#000" font-size="10">C2: Bar (GFCI)</text>
</svg>
```

#### bom/bill_of_materials.csv
```csv
Category,Item,Spec,Qty,Notes
Foundation,Skid beams,6x6 PT x 20',3,Primary runners
Foundation,Cross blocking,4x4 PT,12,@ 48" OC
Floor,Joists,2x8 PT 16" OC,30,Verify span count
Floor,Subfloor,3/4" Advantech T&G,20 sheets,Adhesive + screws
Walls,Studs,2x6 SPF 16" OC,110,Includes openings
Sheathing,ZIP System,7/16",70 sheets,Tape seams
Roof,Rafters,2x8 SPF,22,5/12 pitch
Roof,Underlayment,Synthetic + ice shield,400 sq ft,Eaves/valleys
Roof,Metal panels,Standing-seam 26ga,400 sq ft,Matte Black
Openings,Bar window,7' flip-up awning,1,Gas struts + gasket
Openings,Door,Bronze insulated exterior,1,Weatherstripped
Openings,Windows,Vinyl awning/casement,2,Low-E
Exterior,Siding,LP SmartSide BnB,700 sq ft,Black Onyx
Exterior,Stone veneer,Faux stone panels,120 sq ft,Removable skirt
Interior,Wall/Ceiling,Pine T&G,1000 sq ft,Satin clear
Interior,Floor,LVP,Dark walnut 400 sq ft,Waterproof
Interior,Bar counter,Walnut slab,1,LED underglow
Interior,Dartboard shelf,Fold-down wood,1,Bar-adjacent
Electrical,Inlet,L14-30 30A,1,Weatherproof
Electrical,Subpanel,8-space,1,Neutral isolated
Electrical,Feeder,10/4 Cu THWN,100 ft,Upsize if >100 ft
Electrical,Devices,Recessed LEDs + strips,10,Dimmers, drivers
Electrical,Bottle opener,Wall-mounted,1,Stainless steel
HVAC,Mini-split,9000 BTU 240V,1,Exterior disconnect
Plumbing,Sink,Bar sink + 15 gal gray tank,1,PEX quick-disconnect
Deck,Joists,2x8 PT 16" OC,28,Modular 4' sections
Deck,Surface,Trex Enhance Rocky Harbor,320 sq ft,Hidden fasteners
Deck,Speaker mounts,Weatherproof,2,Bolted to pergola
Deck,Cornhole storage,Lockable nook,1,Under-deck
```

#### bom/cost_breakdown.md
```markdown
# Cost Breakdown (DIY Estimate)

| Category          | Est. USD |
|-------------------|---------:|
| Structure & Framing | 4,800 |
| Roofing           | 1,600 |
| Windows / Doors   | 1,400 |
| Siding / Exterior Trim | 2,000 |
| Interior Finish   | 2,400 |
| Electrical / Lighting | 1,400 |
| HVAC              | 900   |
| Plumbing          | 300   |
| Deck & Pergola    | 3,000 |
| **Total DIY**     | **≈17,500** |

*Note*: Based on 2025 estimates. Verify local prices due to potential fluctuations (e.g., lumber +10% since 2024).
```

#### permit/notes_for_ahj.md
```markdown
# Notes for Authority Having Jurisdiction (AHJ)

- **Classification**: Portable/temporary structure, non-permanent skid foundation
- **Electrical**: NEC 2023 compliant (GFCI/AFCI per Articles 210, 551)
- **Grounding**: Two 8′ rods, #6 Cu bond, neutral isolated in subpanel
- **Egress**: 36″ bronze insulated door, weatherstripped; windows per manufacturer
- **Structural**:
  - Wind load: 90 mph Exposure B
  - Snow load: ≥30 psf (verify local requirements)
- **Safety**: Smoke/CO alarms recommended (battery-powered)
- **Zoning**: Confirm portable structure allowances and setbacks
- **Drawings**: See `plans/figures/*.svg` for elevations, plans, and electrical
```

#### permit/compliance_checklist.md
```markdown
# Compliance Checklist

- [ ] Confirm zoning for portable/temporary structures
- [ ] Verify snow load (≥30 psf) with AHJ
- [ ] Ensure wind load (90 mph) meets local Exposure B/C
- [ ] Install GFCI/AFCI per NEC 2023
- [ ] Complete grounding (two 8′ rods, #6 Cu)
- [ ] Test electrical continuity
- [ ] Install smoke/CO alarms
- [ ] Flash thresholds, seal bar window
- [ ] Submit plans (`plans/figures/`) to AHJ
- [ ] Schedule final inspection (if required)
```

#### deck/trex_layout_16x20.md
```markdown
# Trex Layout — 16 × 20 ft (Rocky Harbor)

- **Orientation**: Boards run 20′ depth, center breaker board at 10′
- **Border**: Picture-frame perimeter, mitered corners
- **Spacing**: 3/16″ with hidden fasteners
- **Bar Zone**: Stools aligned with 7′ flip-up window; blocking under counter
- **Dad Features**:
  - Weatherproof speaker mounts (2, pergola-bolted)
  - Cornhole storage nook (lockable, under-deck)
  - Propane quick-connect for grill (deck edge)
- **Options**: Detachable pergola with LED string lights, propane fire table
```

#### deck/deck_assembly_guide.md
```markdown
# Deck Assembly Guide

1. Excavate and level 16×20 ft pad; compact 4″ gravel base.
2. Assemble 4′ modules (2×8 PT joists @ 16″ OC); bolt and square.
3. Set modules, shim to align deck top with cabin threshold.
4. Install Trex boards with hidden fasteners; add picture-frame border.
5. Mount pergola (optional), string LED lights, install fire table quick-connect.
6. Add speaker mounts, cornhole nook, grill quick-connect.
7. For transport: unbolt modules, stack on pallets (≤2 hr).
```

#### construction/sequence.md
```markdown
# Construction Sequence

1. **Site Prep**: Level 16×24 ft gravel pad, ensure drainage.
2. **Skids**: Set 6×6 PT beams, shim level, install moisture barrier.
3. **Floor**: Frame 2×8 joists, lay 3/4″ Advantech, seal edges.
4. **Walls**: Frame 2×6 studs, sheath with ZIP System, tape seams, stand/plumb.
5. **Roof**: Install 2×8 rafters, ridge board, underlayment, metal panels, vents.
6. **Loft**: Frame 2×6 joists, deck with Advantech, add stair and guardrail.
7. **Openings**: Install bar window, door, casements; flash and trim.
8. **Electrical**: Rough-in wiring, mount L14-30 inlet, subpanel, test continuity.
9. **Interior**: Install pine T&G, LVP flooring, walnut bar, dartboard shelf, TV.
10. **HVAC/Plumbing**: Mount mini-split, bar sink, gray tank, kegerator stub-out.
11. **Deck**: Bolt 16×20 ft modules, surface with Trex, align with bar window.
12. **Punchlist**: Seal thresholds, label panel, secure for transport.
```

#### construction/safety_guidelines.md
```markdown
# Safety Guidelines

- **PPE**: Wear gloves, safety glasses, hearing protection, hard hats.
- **Lifting**: Use forklifts/cranes for skids, walls, roof panels.
- **Electrical**: De-energize circuits during wiring; lockout/tagout.
- **Fall Protection**: Secure ladders for loft/rafter work; use harnesses on roof.
- **Transport**: Secure loose items (TV, bar glass), use lashing points.
- **Inspection**: Verify structural fasteners, electrical grounding before occupancy.
```

#### upgrades/future_upgrades.md
```markdown
# Future Upgrades

- **Solar Power**: 400W roof kit + 200 Ah LiFePO₄ battery, inverter tie-in
- **Smart Controls**: Wi-Fi app for RGB lighting, mini-split
- **Entertainment**: Exterior projector screen on pergola
- **Loft**: Fold-down bunk or desk for multi-use
- **Plumbing**: Upgrade to 30 gal gray tank
- **Dad Features**: Ruggedized tablet mount for sports streaming, bar tool organizer
```

#### .github/workflows/validate.yml
```yaml
name: Validate Repository
on: [push, pull_request]
jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Install Dependencies
        run: sudo apt-get install -y jq
      - name: Validate JSON
        run: jq . project.config.json
      - name: Check Markdown
        run: |
          npm install -g markdownlint-cli
          markdownlint "**/*.md"
      - name: Check CSV
        run: |
          npm install -g csvlint
          csvlint bom/bill_of_materials.csv
      - name: Check SVG Files
        run: |
          for f in plans/figures/*.svg; do xmllint --noout "$f"; done
      - name: Check Required Files
        run: |
          test -f README.md
          test -f LICENSE
          test -f bom/bill_of_materials.csv
          test -f plans/structure.md
```

