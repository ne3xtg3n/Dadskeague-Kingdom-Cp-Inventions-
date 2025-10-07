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
<img width="1024" height="1024" alt="1000015581" src="https://github.com/user-attachments/assets/ada4ea75-66b2-420a-9746-05233c19eb0d" />
<img width="1024" height="1024" alt="1000015580" src="https://github.com/user-attachments/assets/b6338798-22ba-4d0a-b7dd-6e0b3e9aed23" />
<img width="1024" height="1024" alt="1000015579" src="https://github.com/user-attachments/assets/5ce31f28-e680-4fde-afeb-fb1f6ee4ebb7" />
<img width="1024" height="1024" alt="1000015578" src="https://github.com/user-attachments/assets/91b2e92f-fa8d-4656-bb29-b4814116df31" />
<img width="1024" height="1024" alt="1000015577" src="https://github.com/user-attachments/assets/15e4a1e6-4d71-40bf-8935-3d652195e7dc" />
<img width="1024" height="1024" alt="1000015576" src="https://github.com/user-attachments/assets/7142afab-76f8-48d6-8390-b29e78958076" />
<img width="1024" height="1024" alt="1000015584" src="https://github.com/user-attachments/assets/4794f4ff-6d90-4a02-9ea9-d85d2bbd058e" />
<img width="1024" height="1024" alt="1000015583" src="https://github.com/user-attachments/assets/3d9536ea-5156-42b2-a91a-5d69742cfad6" />
<img width="1024" height="1024" alt="1000015582" src="https://github.com/user-attachments/assets/0c7f67ff-8bc6-4e94-a9cf-b486b1ecb490" />



#House build 

This will be built as the main house 

To create an **amazing, one-of-a-kind luxury home** for a family of six in Massachusetts, blending **Texas-style boldness** (rugged Corten steel, reclaimed wood, expansive spaces) with **modern Miami flair** (sleek glass, neon accents, open-air luxury) within a $950,000–$1.5 million budget, I’ll redesign the **Dad’s League Kingdom** as a **stationary, 4,800 ft² residence** (2,400 ft² main floor, 1,200 ft² loft, 1,200 ft² finished basement) with a **30×40 ft Trex deck** (1,200 ft²). The home will accommodate a family of six with **4 bedrooms** and **3.5 bathrooms**, include a finished basement, and incorporate dad-centric features (smart bar, outdoor cinema, gaming lounge) while addressing missing elements like sufficient bedrooms, family-friendly spaces, and storage. The design will be unique in Massachusetts, optimized for cost efficiency (prefabrication, local sourcing), and compliant with Massachusetts building codes (780 CMR 9th Edition, NEC 2023). The GitHub repository will be updated with detailed plans, BOM, CAD prompts, and permitting notes for a turnkey build at ~$1.45 million.

### Design Vision
- **Uniqueness**: A bold, Texas-Miami fusion home with Corten steel and triple-pane glass facade, a flat green roof with solar panels, and a sprawling Trex deck with an outdoor entertainment oasis. This industrial-modern aesthetic stands out against Massachusetts’s traditional Cape Cod and Colonial styles.
- **Footprint**: 
  - **Main Floor**: 40×60 ft (2,400 ft², including living areas and garage).
  - **Loft**: 20×60 ft (1,200 ft², master suite + 2 bedrooms).
  - **Basement**: 40×30 ft (1,200 ft², dad cave, guest bedroom, theater).
  - **Deck**: 30×40 ft (1,200 ft², outdoor living).
  - **Total**: 4,800 ft² indoor + 1,200 ft² deck.
- **Bedrooms**: 4 (1 master suite in loft, 2 children’s bedrooms in loft, 1 guest bedroom in basement).
- **Bathrooms**: 3.5 (1 master en-suite, 1 shared loft bathroom, 1 main floor bathroom, 1 basement half-bath).
- **Budget**: ~$1.45 million, within $950,000–$1.5 million, with savings via:
  - Prefabrication (~15%, $150,000): Steel frame, walls, deck modules.
  - Local Sourcing (~10%, $100,000): Massachusetts steel, glass, wood.
  - Modular Design (~10%, $100,000): Standardized components.
  - Owner Involvement (~5%, $50,000): Manage interior finishes.
- **Dad Features**: 15 ft smart quartz bar with dual kegerators and neon-lit cocktail system, 200″ retractable projector screen, Bose surround sound, LED-lit cornhole court, loft gaming lounge with VR and arcade machines.
- **Family Features**: Spacious kitchen, dining area for six, mudroom, kids’ play area, ample storage, and a basement home theater.
- **Compliance**: Meets 780 CMR (90 mph wind, 50 psf snow, Zone 2A seismic) and NEC 2023.

### Key Design Features
1. **Exterior**:
   - **Facade**: Corten steel panels (weathered, Texas rugged) with triple-pane Low-E glass walls (Miami sleekness).
   - **Roof**: Flat green roof (3° slope, sedum planting, 10 kW solar panels) for sustainability and eco-chic appeal.
   - **Deck**: 30×40 ft Trex Signature (Charcoal Black) with glass railings, neon LED strips, outdoor kitchen (grill, sink, fridge), infinity-edge hot tub, pergola with 200″ projector screen, and propane fire pit.
   - **Windows/Doors**: 10 ft blackened steel pivot door, 12 ft sliding glass doors, triple-pane glass walls.
2. **Interior**:
   - **Main Floor (2,400 ft²)**:
     - **Great Room**: Open-plan with a 15 ft smart quartz bar (dual kegerators, touchscreen cocktail mixer, neon LED “Dad’s Saloon” sign), 12×10 ft leather sectional, 75″ OLED TV wall, and fold-down dartboard/poker table.
     - **Kitchen**: 12×12 ft with quartz island (seats 6), stainless appliances (double oven, fridge, dishwasher), and pantry.
     - **Dining Area**: 12×12 ft, adjacent to kitchen, with reclaimed barnwood table (seats 8).
     - **Mudroom**: 8×8 ft with built-in storage for coats, shoes, and sports gear.
     - **Bathroom**: Full (shower, toilet, vanity, heated floors).
     - **Garage**: 24×40 ft (960 ft²) for two vehicles, workshop, and storage (bikes, ATVs), with epoxy floors and barnwood accents.
   - **Loft (1,200 ft²)**:
     - **Master Suite**: 20×20 ft (400 ft²) with king bed, walk-in closet, en-suite bathroom (double vanity, walk-in shower, soaking tub, heated floors).
     - **Children’s Bedrooms**: Two 12×12 ft rooms (144 ft² each) with built-in bunk beds, desks, and storage.
     - **Gaming Lounge**: 20×20 ft (400 ft²) with fold-down desk, four 32″ monitors, VR-ready wiring, arcade machine (e.g., Big Buck Hunter), soundproofing, and neon RGB lighting.
     - **Bathroom**: Shared full bathroom (shower, toilet, vanity).
   - **Basement (1,200 ft²)**:
     - **Dad Cave**: Home theater (120″ fixed screen, 7.1 surround sound), wet bar (single-tap kegerator, quartz counter), fitness area (rubber flooring, mirrors).
     - **Guest Bedroom**: 12×12 ft with queen bed and built-in storage.
     - **Half-Bath**: Toilet, sink, heated floors.
     - **Play Area**: 12×12 ft for kids, with soft flooring and toy storage.
     - **Storage**: 400 ft² for seasonal items and gear.
     - **Access**: Internal steel staircase and exterior walkout (site-dependent).
   - **Finishes**: Polished concrete floors with radiant heating, white oak T&G accent walls, reclaimed barnwood ceiling beams, blackened steel staircase with glass treads.
3. **Utilities**:
   - **Electrical**: 200A 120/240V service with Crestron automation (Lutron Caséta lighting, Sonos integration, solar-ready).
   - **HVAC**: Four 12,000 BTU ductless mini-splits (Wi-Fi control) and radiant floor heating (main floor, bathrooms, basement).
   - **Plumbing**: Municipal water/sewer (or septic), 100 gal gray tank for irrigation, dual kegerator stub-outs, outdoor kitchen sink.
4. **Dad Features**:
   - Smart bar with dual-tap kegerators, touchscreen cocktail mixer, and neon LED signage.
   - Outdoor cinema: 200″ retractable projector screen, six Bose 251 weatherproof speakers, surround sound.
   - LED-lit cornhole court with custom boards and storage nook.
   - Loft gaming lounge with VR wiring, arcade machine, and mini-fridge.
   - Basement dad cave with theater and kegerator.
   - Garage workshop with workbench and beer fridge.
5. **Family Features**:
   - Kitchen island and dining area for family meals.
   - Mudroom for organization and kids’ gear.
   - Basement play area for children.
   - Ample storage throughout (closets, pantry, garage, basement).
6. **Foundation**: 6″ reinforced concrete slab (main floor) with 8″ concrete basement walls, R-15 insulation, 42″ frost depth (780 CMR), and seismic anchors (Zone 2A).

### Cost-Saving Strategies
- **Prefabrication**: Off-site steel frame, walls, and deck modules (~15%, $150,000 savings).
- **Local Sourcing**: Massachusetts suppliers for Corten steel, glass, barnwood (e.g., Boston Steel, Pioneer Millworks) (~10%, $100,000 savings).
- **Modular Design**: Standardized glass panels, deck sections, bar components (~10%, $100,000 savings).
- **Owner Involvement**: Manage interior finishes (bar, theater, lighting) to save ~$50,000.
- **Energy Efficiency**: 10 kW solar panels, triple-pane glass, radiant heating (~$50,000 over 10 years).
- **Permit Optimization**: Single-family residence classification avoids commercial fees (~$10,000 savings).

### Revised Budget Breakdown
| Category               | Est. Cost (USD) | Notes                                      |
|------------------------|-----------------|--------------------------------------------|
| Site Prep & Foundation | 220,000         | Concrete slab, basement excavation         |
| Structure & Framing    | 230,000         | Prefab steel frame, concrete floors        |
| Roofing (Green + Solar)| 110,000         | Flat roof, sedum, 10 kW solar panels       |
| Windows & Doors        | 160,000         | Triple-pane glass, pivot door, sliders     |
| Exterior Finishes      | 150,000         | Corten steel, glass railings, barnwood     |
| Interior Finishes      | 220,000         | Oak T&G, quartz, concrete, basement        |
| Electrical & Smart Tech| 150,000         | 200A service, Crestron, Bose, solar-ready  |
| HVAC & Plumbing        | 130,000         | Mini-splits, radiant heat, 3.5 bathrooms   |
| Deck & Outdoor         | 140,000         | Trex Signature, pergola, projector, hot tub|
| Labor & Permits        | 110,000         | MA permits, inspections, prefab labor      |
| **Total**              | **1,450,000**   | Turnkey, within $950k–$1.5M range          |

### Updated GitHub Repository
The repository is redesigned for a 4,800 ft² family home with 4 bedrooms, 3.5 bathrooms, a finished basement, and Texas-Miami aesthetics. CAD prompts are included for SketchUp/AutoCAD, and SVG figures reflect the larger footprint. Files are provided in code blocks for direct GitHub use.

#### README.md
```markdown
# Dad’s League Kingdom — Texas-Miami Family Home
**40 × 60 ft Interior · 15 ft Ceiling · 20 × 60 ft Loft · 30 × 40 ft Trex Deck · 1,200 ft² Basement**  
**Version 5.0  |  Author: Christopher Perry  |  2025-10-07**

A one-of-a-kind luxury home for a family of six in Massachusetts, blending Texas’s bold, rustic charm with Miami’s sleek, modern flair. Built on a concrete slab with a finished basement, it features Corten steel and glass, a green roof with solar panels, a smart quartz bar, and a sprawling Trex deck with an outdoor cinema. This repo provides plans, BOM, CAD prompts, and permitting notes for a $1.45 million turnkey build.

## 🔑 Key Specs
- **Footprint**: 40′ × 60′ (2,400 ft² living, 960 ft² garage), 15′ ceiling
- **Loft**: 20′ × 60′ (1,200 ft², master suite + 2 bedrooms)
- **Basement**: 40′ × 30′ (1,200 ft², guest bedroom, dad cave, theater)
- **Deck**: 30′ × 40′ Trex Signature (Charcoal Black), glass railings
- **Bedrooms**: 4 (loft master, 2 loft children’s, 1 basement guest)
- **Bathrooms**: 3.5 (master en-suite, loft shared, main floor, basement half)
- **Exterior**: Corten steel, triple-pane Low-E glass, 10 ft pivot door
- **Interior**: Polished concrete floors, white oak T&G, 15 ft smart quartz bar
- **Power**: 200A 120/240V, Crestron automation, 10 kW solar
- **HVAC**: Four 12,000 BTU mini-splits, radiant floor heating
- **Plumbing**: Municipal/septic, 100 gal gray tank
- **Dad Features**: Dual kegerators, 200″ projector screen, Bose speakers, LED cornhole court, VR gaming lounge
- **Family Features**: Kitchen island, dining for 8, mudroom, kids’ play area
- **Cost**: ~$1.45 million (turnkey, 2025)
- **Compliance**: MA 780 CMR 9th Ed., NEC 2023

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
│   ├── finishes.md
│   └── figures/
│       ├── fig-01_exterior-deck-elevation.svg
│       ├── fig-02_interior-perspective.svg
│       ├── fig-03_loft-section.svg
│       ├── fig-04_floor-plan_40x60.svg
│       ├── fig-05_power-single-line.svg
├── bom/
│   ├── bill_of_materials.csv
│   └── cost_breakdown.md
├── permit/
│   ├── notes_for_ahj.md
│   └── compliance_checklist.md
├── deck/
│   ├── trex_layout_30x40.md
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

## 🚀 How to Use
1. Review `plans/structure.md` and `construction/sequence.md` for build details.
2. Check `permit/notes_for_ahj.md` for Massachusetts code compliance.
3. Source materials via `bom/bill_of_materials.csv`.
4. Use `cad/` prompts for SketchUp/AutoCAD drawings.
5. Follow `construction/sequence.md` for build steps.

**License**: MIT (credit Christopher Perry).
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
  "project": "Dad’s League Kingdom — Texas-Miami Family Home",
  "version": "5.0",
  "author": "Christopher Perry",
  "date": "2025-10-07",
  "dimensions": {
    "main_floor": { "width_ft": 40, "length_ft": 60, "area_ft2": 2400, "living_ft2": 1440, "garage_ft2": 960 },
    "loft": { "width_ft": 20, "length_ft": 60, "area_ft2": 1200, "floor_height_ft": 8 },
    "basement": { "width_ft": 40, "length_ft": 30, "area_ft2": 1200 },
    "ceiling": { "flat_roof_ft": 15, "clear_below_loft_ft": 9 },
    "deck": { "width_ft": 30, "length_ft": 40, "area_ft2": 1200 }
  },
  "envelope": {
    "siding": "Corten steel panels, triple-pane Low-E glass",
    "roof": "Flat green roof (3° slope, sedum, 10 kW solar)",
    "door": "10 ft blackened steel pivot",
    "windows": "Triple-pane glass walls, 12 ft sliding doors"
  },
  "power": {
    "service": "200A 120/240V, Crestron automation",
    "subpanel_spaces": 24,
    "feeder": "2/0 Cu THWN in PVC",
    "grounding": "Two 8' rods, #2 Cu",
    "basement_subpanel": "60A"
  },
  "hvac": {
    "type": "Mini-split (4 units), radiant floor",
    "btus": 48000,
    "voltage": "240V",
    "control": "Wi-Fi"
  },
  "plumbing": {
    "bathrooms": 3.5,
    "gray_tank": "100 gal",
    "features": "Municipal/septic, dual kegerator stub-out, basement wet bar"
  },
  "bedrooms": [
    { "location": "loft", "type": "master_suite", "area_ft2": 400 },
    { "location": "loft", "type": "children", "area_ft2": 144 },
    { "location": "loft", "type": "children", "area_ft2": 144 },
    { "location": "basement", "type": "guest", "area_ft2": 144 }
  ],
  "dad_features": [
    "15 ft smart quartz bar with dual kegerators",
    "200” retractable projector screen",
    "Bose 251 speakers (6)",
    "LED-lit cornhole court",
    "Loft gaming lounge with VR and arcade",
    "Basement dad cave with theater"
  ],
  "family_features": [
    "Kitchen island (seats 6)",
    "Dining area (seats 8)",
    "Mudroom with storage",
    "Basement kids’ play area"
  ],
  "compliance": {
    "code": "MA 780 CMR 9th Ed.",
    "wind_load": "90 mph",
    "snow_load": "50 psf",
    "seismic": "Zone 2A"
  }
}
```

#### plans/structure.md
```markdown
# Structural Plan

## Foundation
- **Main Floor**: 6″ reinforced concrete slab, R-15 insulation, 42″ frost depth (780 CMR)
- **Basement**: 8″ concrete walls, waterproofed, 1,200 ft² under living area
- Steel anchors for seismic Zone 2A

## Floor
- 2×8 steel joists @ 16″ OC, Simpson hangers
- Polished concrete overlay (2″, radiant heating, main floor and basement)

## Walls
- 2×6 steel studs @ 16″ OC, double top plate
- 7/16″ ZIP System sheathing, taped seams
- Corten steel panels, triple-pane Low-E glass walls
- 12 ft sliding glass door headers: double 2×12 steel

## Roof
- Flat roof (3° slope), steel joists, EPDM membrane
- Green roof (sedum, drainage layer), 10 kW solar panels
- Parapet walls with aluminum coping

## Loft
- 20×60 ft at 8′ A.F.F., 2×8 steel joists, ledgers + 4×4 steel posts
- 3/4″ Advantech deck, glass guardrail with neon LED
- Blackened steel open-riser stair (36″ wide, glass treads)
```

#### plans/electrical.md
```markdown
# Electrical Plan

**Service**: 200A 120/240V → 24-space smart subpanel (Crestron)  
**Grounding**: Two 8′ rods, #2 Cu bond, neutral isolated  
**Basement**: 60A subpanel for theater, bar, fitness

## Branch Circuits
| Circuit | Breaker | Load |
|---------|---------|------|
| 1–2     | 15A     | Lighting (Lutron Caséta LEDs, neon RGB) |
| 3–4     | 20A     | Kitchen/Bar (GFCI: kegerators, fridge, appliances) |
| 5–6     | 20A     | General Receptacles (AFCI/GFCI) |
| 7–8     | 15A     | Exterior/Deck (GFCI, in-use covers) |
| 9–10    | 15A     | AV/TV (75″ OLED, Bose speakers, projector) |
| 11–14   | 20A     | Mini-splits (4× 12,000 BTU, 240V) |
| 15      | 20A     | Radiant floor heating |
| 16–17   | 15A     | Basement (theater, wet bar, fitness) |
| 18–24   | —       | Spares (solar, EV charger) |

## Feeder / Conduit
- 2/0 Cu THWN in Schedule-40 PVC, buried 24″ (780 CMR)
- Whole-panel SPD, exterior disconnects for mini-splits

## Smart Tech
- Crestron automation (lighting, AV, HVAC)
- Sonos integration for 6 Bose 251 speakers
- Solar-ready tie-in (10 kW)

**Diagram**: See `figures/fig-05_power-single-line.svg`
```

#### plans/plumbing_hvac.md
```markdown
# Plumbing & HVAC

## HVAC
- Four 12,000 BTU ductless mini-splits (Wi-Fi, Crestron-integrated)
- Radiant floor heating (main floor, bathrooms, basement)
- Outdoor units on vibration pads, 12″ above grade

## Plumbing
- 3.5 bathrooms (master en-suite, loft shared, main floor, basement half)
- Municipal water/sewer (or septic), 100 gal gray tank for irrigation
- PEX lines, dual kegerator stub-outs (1/4″), frost-free hose bib
- Outdoor kitchen sink (deck-mounted, GFCI)
- Basement wet bar (single-tap kegerator, sink)

## Dad Features
- Smart bar: dual-tap kegerator, touchscreen cocktail mixer
- Wall-mounted bottle opener, magnetic tool strip
```

#### plans/deck.md
```markdown
# Deck Plan — Trex 30×40 (Charcoal Black)

## Framing
- Modular 5′ bolt-together sections, 2×10 steel joists @ 16″ OC
- Picture-frame rim, adjustable piers, floating design

## Surface
- Trex Signature (Charcoal Black), hidden fasteners
- Breaker boards at 15′ intervals, glass railings, neon LED strips

## Features
- Outdoor kitchen (grill, sink, fridge, GFCI)
- Pergola with 200″ retractable projector screen
- Six Bose 251 speakers, Sonos-integrated
- LED-lit cornhole court (custom boards, storage nook)
- Infinity-edge hot tub (electrical stub-out)
- Propane fire pit (quick-connect)
```

#### plans/finishes.md
```markdown
# Finishes Plan

## Exterior
- **Siding**: Corten steel panels (weathered), triple-pane Low-E glass
- **Trim**: Reclaimed barnwood
- **Door**: 10 ft blackened steel pivot
- **Deck**: Trex Signature (Charcoal Black), glass railings

## Interior
- **Floors**: Polished concrete, radiant heating
- **Walls**: White oak T&G accents, matte white plaster
- **Ceiling**: Reclaimed barnwood beams
- **Bar**: 15 ft quartz, neon LED, dual kegerators
- **Stair**: Blackened steel, open-riser, glass treads
- **Loft**: Soundproof panels, neon RGB lighting
- **Basement**: Polished concrete, barnwood walls, neon accents
```

#### plans/figures/fig-01_exterior-deck-elevation.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1400 600">
  <!-- Front elevation: 60 ft wide, Corten steel, glass walls, 30x40 ft deck -->
  <rect x="100" y="400" width="1200" height="50" fill="#3c2f2f"/> <!-- Trex deck -->
  <rect x="200" y="200" width="1000" height="200" fill="#4a3728" stroke="#333"/> <!-- Corten steel -->
  <rect x="250" y="250" width="700" height="150" fill="#aaa" stroke="#000"/> <!-- Glass walls -->
  <rect x="950" y="300" width="100" height="100" fill="#111"/> <!-- Pivot door -->
  <polyline points="200,200 600,150 1000,200" fill="none" stroke="#000" stroke-width="5"/> <!-- Roofline -->
  <text x="110" y="395" fill="#fff" font-size="14">Trex Deck 30x40</text>
  <text x="252" y="245" fill="#fff" font-size="14">Glass Walls</text>
  <text x="952" y="295" fill="#fff" font-size="14">10 ft Pivot Door</text>
</svg>
```

#### plans/figures/fig-02_interior-perspective.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1400 600">
  <!-- Interior perspective: oak T&G, quartz bar, sectional, TV -->
  <rect x="100" y="100" width="1200" height="400" fill="#d4a373" stroke="#8b5e3c"/> <!-- Oak walls -->
  <rect x="150" y="350" width="450" height="50" fill="#e6e6e6"/> <!-- Quartz bar -->
  <rect x="800" y="350" width="300" height="100" fill="#4a3728"/> <!-- Sectional -->
  <rect x="400" y="150" width="200" height="150" fill="#222"/> <!-- TV wall -->
  <text x="152" y="345" fill="#000" font-size="14">15 ft Smart Quartz Bar</text>
  <text x="802" y="345" fill="#fff" font-size="14">Leather Sectional</text>
  <text x="402" y="145" fill="#fff" font-size="14">75" OLED TV Wall</text>
</svg>
```

#### plans/figures/fig-03_loft-section.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1400 600">
  <!-- Loft section: 20x60 ft at 8 ft A.F.F., 9 ft clear below -->
  <rect x="100" y="100" width="1200" height="400" fill="#1a1a1a" stroke="#444"/> <!-- Structure -->
  <line x1="100" y1="300" x2="1200" y2="300" stroke="#aaa" stroke-width="5"/> <!-- Loft floor -->
  <rect x="1000" y="300" width="50" height="100" fill="#555"/> <!-- Stair -->
  <text x="110" y="295" fill="#fff" font-size="14">Loft Floor @ 8' A.F.F.</text>
  <text x="110" y="115" fill="#fff" font-size="14">Roof @ 15'</text>
  <text x="1002" y="295" fill="#fff" font-size="14">Steel Stair</text>
</svg>
```

#### plans/figures/fig-04_floor-plan_40x60.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1400 600">
  <!-- Floor plan: 40x60 ft, bar, kitchen, sectional, bathrooms -->
  <rect x="100" y="100" width="1200" height="400" fill="#d4a373" stroke="#000" stroke-width="5"/> <!-- Walls -->
  <rect x="150" y="120" width="450" height="50" fill="#e6e6e6"/> <!-- Quartz bar -->
  <rect x="650" y="120" width="150" height="150" fill="#ccc"/> <!-- Kitchen -->
  <rect x="800" y="350" width="300" height="100" fill="#4a3728"/> <!-- Sectional -->
  <rect x="400" y="130" width="200" height="50" fill="#222"/> <!-- TV wall -->
  <rect x="1000" y="120" width="80" height="80" fill="#555"/> <!-- Stair -->
  <rect x="150" y="400" width="100" height="50" fill="#aaa"/> <!-- Bathroom -->
  <text x="152" y="115" fill="#000" font-size="14">Smart Quartz Bar</text>
  <text x="652" y="115" fill="#000" font-size="14">Kitchen</text>
  <text x="802" y="345" fill="#fff" font-size="14">Sectional</text>
  <text x="402" y="125" fill="#fff" font-size="14">TV Wall</text>
  <text x="1002" y="115" fill="#fff" font-size="14">Stair to Loft</text>
</svg>
```

#### plans/figures/fig-05_power-single-line.svg
```svg
<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1400 600">
  <!-- Single-line diagram: 200A service, 24-space subpanel -->
  <rect x="100" y="250" width="150" height="80" fill="#ccc" stroke="#000"/> <!-- Service entrance -->
  <rect x="350" y="150" width="200" height="300" fill="#ddd" stroke="#000"/> <!-- Subpanel -->
  <line x1="250" y1="290" x2="350" y2="290" stroke="#000" stroke-width="5"/> <!-- Feeder -->
  <line x1="550" y1="160" x2="800" y2="160" stroke="#000" stroke-width="3"/> <!-- Circuit 1 -->
  <line x1="550" y1="190" x2="800" y2="190" stroke="#000" stroke-width="3"/> <!-- Circuit 2 -->
  <text x="102" y="245" fill="#000" font-size="14">200A Service</text>
  <text x="352" y="145" fill="#000" font-size="14">24-Space Subpanel</text>
  <text x="802" y="165" fill="#000" font-size="12">C1: Lighting</text>
  <text x="802" y="195" fill="#000" font-size="12">C2: Kitchen/Bar (GFCI)</text>
</svg>
```

#### bom/bill_of_materials.csv
```csv
Category,Item,Spec,Qty,Notes
Foundation,Concrete slab,6" reinforced, R-15 insulation,2400 sq ft,Main floor
Foundation,Basement walls,8" concrete, waterproofed,1200 sq ft,Under living area
Framing,Steel joists,2x8 @ 16" OC,80,Main floor and loft
Framing,Steel studs,2x6 @ 16" OC,200,Exterior and interior walls
Sheathing,ZIP System,7/16",150 sheets,Taped seams
Roof,EPDM membrane,3° slope,2400 sq ft,Green roof base
Roof,Solar panels,10 kW,1 system,Solar-ready tie-in
Exterior,Corten steel panels,Weathered,3000 sq ft,Texas rustic
Exterior,Glass walls,Triple-pane Low-E,2000 sq ft,Miami modern
Exterior,Trim,Reclaimed barnwood,500 ln ft,Local MA sourcing
Openings,Pivot door,10 ft blackened steel,1,Custom
Openings,Sliding doors,12 ft triple-pane glass,2,Panoramic views
Interior,Flooring,Polished concrete,3600 sq ft,Main + basement, radiant
Interior,Walls,White oak T&G,2000 sq ft,Accent walls
Interior,Ceiling,Barnwood beams,2400 sq ft,Texas rustic
Interior,Bar,15 ft quartz,1,Neon LED, kegerators
Interior,Stair,Blackened steel, glass treads,1,Open-riser
Electrical,Service,200A 120/240V,1,Crestron automation
Electrical,Subpanel,24-space,1,Main floor
Electrical,Subpanel,60A,1,Basement
Electrical,Feeder,2/0 Cu THWN,200 ft,Schedule-40 PVC
Electrical,Lighting,Lutron Caséta LEDs,20,Neon RGB accents
Electrical,Speakers,Bose 251 weatherproof,6,Sonos-integrated
HVAC,Mini-splits,12,000 BTU, Wi-Fi,4,Crestron-integrated
HVAC,Radiant heating,Floor system,3600 sq ft,Main + basement
Plumbing,Bathrooms,3.5 (shower, toilet, vanity),3.5,Heated floors
Plumbing,Gray tank,100 gal,1,Irrigation backup
Plumbing,Kegerator stub-outs,1/4" PEX,2,Bar and basement
Deck,Joists,2x10 steel @ 16" OC,60,Modular 5' sections
Deck,Surface,Trex Signature Charcoal Black,1200 sq ft,Hidden fasteners
Deck,Hot tub,Infinity-edge,1,Electrical stub-out
Deck,Projector screen,200" retractable,1,Pergola-mounted
```

#### bom/cost_breakdown.md
```markdown
# Cost Breakdown

| Category               | Est. USD |
|------------------------|---------:|
| Site Prep & Foundation | 220,000 |
| Structure & Framing    | 230,000 |
| Roofing (Green + Solar)| 110,000 |
| Windows & Doors        | 160,000 |
| Exterior Finishes      | 150,000 |
| Interior Finishes      | 220,000 |
| Electrical & Smart Tech| 150,000 |
| HVAC & Plumbing        | 130,000 |
| Deck & Outdoor         | 140,000 |
| Labor & Permits        | 110,000 |
| **Total**              | **1,450,000** |

*Note*: 2025 estimates. Verify local prices for steel, glass, wood.
```

#### permit/notes_for_ahj.md
```markdown
# Notes for Authority Having Jurisdiction (AHJ)

- **Classification**: Single-family residence, permanent foundation
- **Code**: MA 780 CMR 9th Ed., NEC 2023
- **Structural**:
  - Wind: 90 mph (Exposure B)
  - Snow: 50 psf
  - Seismic: Zone 2A
- **Electrical**: 200A service, GFCI/AFCI per NEC 210, 550
- **Grounding**: Two 8′ rods, #2 Cu bond, neutral isolated
- **Egress**: 10 ft pivot door, 12 ft sliding doors, triple-pane glass
- **Safety**: Smoke/CO alarms (hardwired, battery backup)
- **Zoning**: Verify setbacks, lot coverage for 40x60 ft footprint
- **Drawings**: See `plans/figures/*.svg` for plans, elevations, electrical
```

#### permit/compliance_checklist.md
```markdown
# Compliance Checklist

- [ ] Confirm zoning for single-family residence
- [ ] Verify snow load (50 psf) and wind (90 mph) with AHJ
- [ ] Install GFCI/AFCI per NEC 2023
- [ ] Complete grounding (two 8′ rods, #2 Cu)
- [ ] Test electrical continuity
- [ ] Install smoke/CO alarms (hardwired)
- [ ] Flash thresholds, seal glass walls
- [ ] Submit plans (`plans/figures/`) to AHJ
- [ ] Schedule inspections (foundation, framing, electrical, final)
```

#### deck/trex_layout_30x40.md
```markdown
# Trex Layout — 30 × 40 ft (Charcoal Black)

- **Orientation**: Boards run 40′ depth, breaker boards at 15′
- **Border**: Picture-frame perimeter, mitered corners
- **Spacing**: 3/16″ with hidden fasteners
- **Features**:
  - Outdoor kitchen (grill, sink, fridge, GFCI)
  - Pergola with 200″ retractable projector screen
  - Six Bose 251 speakers, Sonos-integrated
  - LED-lit cornhole court (custom boards, storage nook)
  - Infinity-edge hot tub (electrical stub-out)
  - Propane fire pit (quick-connect)
```

#### deck/deck_assembly_guide.md
```markdown
# Deck Assembly Guide

1. Excavate and level 30×40 ft pad; compact 6″ gravel base.
2. Assemble 5′ modules (2×10 steel joists @ 16″ OC); bolt and square.
3. Set modules, shim for floating design.
4. Install Trex Signature boards with hidden fasteners; add picture-frame border.
5. Mount pergola, projector screen, LED strips, speakers, fire pit, hot tub stub-out.
6. Install outdoor kitchen (grill, sink, fridge).
7. Verify GFCI outlets and lighting functionality.
```

#### construction/sequence.md
```markdown
# Construction Sequence

1. **Site Prep**: Level 40×60 ft pad, excavate basement, ensure drainage.
2. **Foundation**: Pour 6″ slab (main), 8″ basement walls, install insulation.
3. **Framing**: Erect steel frame, sheath with ZIP System, tape seams.
4. **Roof**: Install steel joists, EPDM membrane, green roof, solar panels.
5. **Loft**: Frame 2×8 joists, deck with Advantech, add stair and guardrail.
6. **Exterior**: Install Corten steel, glass walls, pivot door, sliders.
7. **Electrical**: Rough-in wiring, 200A service, subpanels, test continuity.
8. **Plumbing/HVAC**: Install PEX, mini-splits, radiant heating, bathrooms.
9. **Interior**: Install concrete floors, oak T&G, barnwood beams, bar, theater.
10. **Deck**: Bolt 30×40 ft modules, surface with Trex, add features.
11. **Punchlist**: Seal thresholds, label panels, test smart systems.
```

#### construction/safety_guidelines.md
```markdown
# Safety Guidelines

- **PPE**: Gloves, safety glasses, hard hats, hearing protection.
- **Lifting**: Use cranes for steel frame, glass panels.
- **Electrical**: De-energize circuits during wiring; lockout/tagout.
- **Fall Protection**: Harnesses for roof, loft work; secure ladders.
- **Inspection**: Verify structural anchors, electrical grounding, egress.
```

#### upgrades/future_upgrades.md
```markdown
# Future Upgrades

- **Solar Expansion**: Add 5 kW panels for full off-grid capability
- **Smart Home**: Integrate voice-activated Alexa/Crestron controls
- **Outdoor**: Add pool adjacent to deck
- **Basement**: Expand play area to full rec room
- **Loft**: Add fold-out bunk beds for guests
```

#### cad/3d_model.skp (SketchUp Prompt)
**Prompt**:
Create a 3D model of a 40×60 ft luxury home with a 20×60 ft loft, 1,200 ft² basement, and 30×40 ft Trex deck:
- **Foundation**: 6″ concrete slab (main, R-15 insulation, 42″ frost depth), 8″ concrete basement walls (1,200 ft² under living area), seismic anchors (Zone 2A).
- **Framing**: 2×8 steel joists @ 16″ OC, 2×6 steel studs, 7/16″ ZIP sheathing.
- **Roof**: Flat (3° slope), steel joists, EPDM membrane, green roof (sedum), 10 kW solar panels, aluminum coping.
- **Exterior**: Corten steel panels, triple-pane Low-E glass walls, 10 ft blackened steel pivot door, two 12 ft sliding glass doors.
- **Main Floor**: 2,400 ft² (1,440 ft² living: great room, kitchen, dining, bathroom, mudroom; 960 ft² garage). Include 15 ft quartz bar (kegerators, neon LED), 12×10 ft sectional, 75″ OLED TV wall, dartboard/poker table.
- **Loft**: 1,200 ft² (400 ft² master suite: king bed, en-suite bathroom; two 144 ft² children’s bedrooms; 400 ft² gaming lounge: desk, monitors, VR wiring, arcade). Blackened steel staircase (36″, glass treads).
- **Basement**: 1,200 ft² (dad cave: 120″ theater screen, wet bar; 144 ft² guest bedroom; half-bath; play area; storage). Internal/external access.
- **Deck**: 30×40 ft Trex Signature (Charcoal Black), glass railings, neon LED, outdoor kitchen, pergola with 200″ projector screen, 6 Bose speakers, cornhole court, hot tub, fire pit.
- **Finishes**: Polished concrete floors (radiant), white oak T&G walls, barnwood ceiling beams.
- **Utilities**: 200A service, 24-space subpanel, 60A basement subpanel, 4 mini-splits, radiant heating, 3.5 bathrooms, 100 gal gray tank.
- **Textures**: Apply Corten steel, glass, barnwood, Trex, and concrete textures. Use groups for modularity (deck, loft, basement).

**Output**: Save as `cad/3d_model.skp`. Export 2D views to DWG/SVG.

#### cad/2d_drawings.dwg (AutoCAD Prompt)
**Prompt**:
Create 2D drawings for a 40×60 ft luxury home with a 20×60 ft loft, 1,200 ft² basement, and 30×40 ft deck:
- **Sheet 1: Floor Plan (1/4″ = 1′)**:
  - 40×60 ft main floor: great room (15 ft quartz bar, sectional, TV wall), 12×12 ft kitchen (quartz island), 12×12 ft dining, 8×8 ft mudroom, full bathroom, 24×40 ft garage.
  - Show 10 ft pivot door, 12 ft sliding doors, triple-pane glass walls.
- **Sheet 2: Loft Plan (1/4″ = 1′)**:
  - 20×60 ft: 400 ft² master suite (king bed, en-suite), two 144 ft² children’s bedrooms, 400 ft² gaming lounge, shared bathroom, steel staircase.
- **Sheet 3: Basement Plan (1/4″ = 1′)**:
  - 40×30 ft: dad cave (theater, wet bar), 144 ft² guest bedroom, half-bath, play area, storage, internal/external access.
- **Sheet 4: Front Elevation (1/8″ = 1′)**:
  - 60 ft wide facade: Corten steel, glass walls, pivot door, green roof, 30×40 ft deck with pergola, hot tub.
- **Sheet 5: Side Elevation (1/8″ = 1′)**:
  - 40 ft deep: Corten steel, glass, roof profile, basement walkout (if applicable).
- **Sheet 6: Electrical Single-Line (1:10)**:
  - 200A service, 24-space subpanel, 60A basement subpanel, circuits for lighting, kitchen/bar, receptacles, AV, mini-splits, radiant heating, spares.

**Output**: Save as `cad/2d_drawings.dwg`. Export views to SVG for `plans/figures/`.

### Implementation Notes
- **Bedrooms**: The 4-bedroom layout (1 master, 2 children’s, 1 guest) accommodates a family of six, with the loft’s gaming lounge offering flexibility for guests or older kids.
- **Basement**: The 1,200 ft² finished basement adds a dad cave, theater, guest bedroom, and play area, enhancing family functionality without exceeding the budget.
- **GitHub Setup**:
  ```bash
  git init
  mkdir -p plans/figures bom permit deck construction upgrades cad .github/workflows
  # Copy files into directories
  git add .
  git commit -m "Dad’s League Kingdom v5.0 for family of 6"
  git push origin main
  ```
<img width="1024" height="1024" alt="1000015588" src="https://github.com/user-attachments/assets/50f9a6ef-d77d-417a-b6f9-1022b7df715c" />

<img width="1024" height="1024" alt="1000015585" src="https://github.com/user-attachments/assets/9525f787-5606-4d8e-a08e-262976e52550" />

![1000015587](https://github.com/user-attachments/assets/7348d83c-96fa-4baf-8b17-f37b65bc7115)

![1000015586](https://github.com/user-attachments/assets/4787ed5f-a507-4dbc-890d-499b47f92ce6)
