# DIY Designer Profiles — Template & Standards

This directory contains profiles for open-source/open-plan loudspeaker designers serving the DIY sound system community. These are distinct from the commercial manufacturer dossiers in `reports/boutique/`.

**Key difference:** DIY profiles do not use the UDS composite scoring system. Instead, they assess buildability, specifications, driver options, community track record, and Mark I suitability for the Sonorant Sound project.

---

## Profile Template

Each DIY designer profile should include the following sections:

### 1. Designer Overview
- Who they are, where they're based, what they do
- How long they've been active
- Business model (open-source plans, paid plans, kit sales, driver manufacturing)

### 2. Design Philosophy
- Core approach and what distinguishes their work
- Key innovations or proprietary loading techniques
- Target use cases (PA, home audio, festival, etc.)

### 3. Technology Summary
- The underlying loading/acoustic principles
- How the technology works (e.g., Paraflex loading, MEH principle)
- Comparison to conventional approaches

### 4. Product Catalog
Every relevant design with:

| Field | Description |
|-------|-------------|
| Model name | Including version (V1, V2, etc.) |
| Configuration | Driver count × driver size |
| Dimensions | LxWxH in mm |
| Weight | Unloaded, kg (BB ply or specified material) |
| Volume | Internal volume in litres |
| Tuning frequency | Fb in Hz |
| Operating range | Hz |
| Sensitivity | dB avg 1w@1m over operating range |
| Maximum SPL | Continuous and peak, dB |
| Recommended drivers | Full list with manufacturer and model |
| Plan availability | Free/paid, PDF/DXF/STEP |
| Version history | Changes between versions |

### 5. Driver Lineup (if designer manufactures drivers)
- Model numbers and sizes
- Key specs: Xmax, power handling, impedance, sensitivity, BL, Vas
- Pricing if available
- Cone/voice coil materials

### 6. Build Requirements
- Materials (plywood thickness, type)
- Tools needed
- CNC vs hand-build feasibility
- 3D printed components
- Assembly complexity (beginner/intermediate/advanced)

### 7. DSP/Processing Requirements
- Active crossover needs
- FIR filter availability and design tools
- Recommended amplification
- Processing platforms used by community

### 8. Community Track Record
- Build threads (diyAudio, AVS Forum, etc.)
- Number of known builds (estimate)
- Reported issues and solutions
- User impressions of sound quality
- Notable deployments

### 9. Mark I Suitability Assessment
How well the designs fit Sonorant's constraints:

| Criterion | Assessment |
|-----------|------------|
| 100–200 person venue scale | How appropriate for this scale |
| Sub-bass weight and infrasonic extension | Low frequency capability |
| Hyper-real clarity | Mid/high frequency performance |
| Fast transients | Transient response characteristics |
| Small-room optimization | Directivity, room interaction |
| Transportability | Weight, size, handling |
| Builder availability | Support ecosystem, parts sourcing |

### 10. Sources
All citations with provenance tags:

| Tag | Meaning |
|-----|---------|
| designer-published | Specs, plans, and measurements from the designer |
| community-measured | Independent measurements by builders |
| peer-reviewed | Academic sources on underlying principles |
| industry | Component manufacturer datasheets, publications |

### 11. Open Questions
- Unknowns that need user input or further research
- Specs not established or conflicting

---

## JSON Schema (Adapted for DIY)

The companion `.json` file uses an adapted UDS schema:

- Replace `composite_score` with `mark_i_suitability` (qualitative, not numeric)
- Replace `scoring_rationale` with `design_fit_notes`
- Keep `models[]` array with specs per design
- Keep `sources[]` array with provenance tags
- Add `drivers[]` array if designer manufactures drivers

---

## Current Profiles

| Designer | Profile | Focus |
|----------|---------|-------|
| HOQS (Kaironex) | `hoqs.md` | Paraflex loading, subwoofers, mid-tops, drivers |
| JW Sound (John White) | `jw_sound.md` | MEH / Multiple Entry Horn, JMOD series |
