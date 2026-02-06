# Directive 009 — DIY Designer Profiles: HOQS & JW Sound

**From:** Planning instance (claude.ai)
**To:** Transducer Archive (CLI agent)
**Date:** 2025-02-06

## Context

The project is pivoting to a near-term buildable system (Mark I) alongside the ongoing long-term research program. Mark I will be built by an authorized HOQS dealer/builder using DIY plans, targeting the same 100–200 person venue scale as the full Sonorant vision but using immediately available, community-proven designs.

Two designers are under active consideration:

1. **HOQS (Australia, designed by Kaironex)** — Creator of the Paraflex cabinet loading technology and a full catalog of subwoofer and mid-top designs. Also manufactures their own drivers. The builder is an authorized HOQS dealer recommending Type O subs (1x18 and 2x18 variants) for Mark I.

2. **JW Sound (John White)** — Creator of the JMOD, a Multiple Entry Horn (MEH) in the Danley lineage. Free DIY plans available. JMOD v2 is expected soon and is being considered for Mark I tops. JW Sound also offers other designs (JMOD-M, SAWMOD, Solana).

These are not commercial loudspeaker manufacturers like the Batch 1 companies. They are open-source/open-plan designers serving the DIY sound system community. The existing UDS scoring system does not apply. These profiles need a different format focused on buildability, specifications, driver options, and community track record.

## Objective

Create two designer profile reports in a new `reports/diy/` directory. Each profile should comprehensively document the designer's background, design philosophy, full relevant catalog with specifications, driver requirements, build considerations, and community reception. No composite scoring — instead, include a Mark I suitability assessment.

## Part A: Directory Setup

### A1: Create `reports/diy/` directory

Create the directory with a `_README.md` template file that defines the DIY designer profile format:

```
reports/diy/_README.md
```

The template should specify these sections for each profile:

1. **Designer Overview** — Who they are, where they're based, what they do, how long they've been active
2. **Design Philosophy** — Core approach, what distinguishes their work, key innovations
3. **Technology Summary** — The underlying loading/acoustic principles (e.g., Paraflex loading, MEH principle)
4. **Product Catalog** — Every relevant design with:
   - Model name and version
   - Configuration (driver count × driver size)
   - Cabinet dimensions (LxWxH in mm)
   - Cabinet weight (unloaded, kg)
   - Cabinet volume (litres)
   - Tuning frequency (Fb, Hz)
   - Operating range (Hz)
   - Sensitivity (dB avg 1w@1m over operating range)
   - Maximum SPL (continuous and peak, dB)
   - Recommended drivers (full list with manufacturer and model number)
   - Plan availability (free/paid, PDF/DXF/STEP)
   - Version history (V1, V2, changes between versions)
5. **Driver Lineup** (if designer manufactures drivers) — Model numbers, sizes, key specs (Xmax, power handling, impedance, sensitivity), pricing if available
6. **Build Requirements** — Materials (plywood thickness, type), tools needed, CNC vs hand-build feasibility, 3D printed components, assembly complexity
7. **DSP/Processing Requirements** — Active crossover needs, FIR filter availability, recommended amplification, processing platforms used by community
8. **Community Track Record** — Build threads (diyAudio, AVS Forum, etc.), number of known builds, reported issues, user impressions, notable deployments
9. **Mark I Suitability Assessment** — How well the designs fit Sonorant's constraints:
   - 100–200 person venue scale
   - Sub-bass weight and infrasonic extension
   - Hyper-real clarity
   - Fast transients
   - Small-room optimization
   - Transportability (preference, not constraint)
   - Builder availability and support ecosystem
10. **Sources** — All citations with provenance tags (designer-published | community-measured | peer-reviewed | industry)
11. **Open Questions** — Unknowns that need user input or further research

Source provenance tags for DIY profiles use a modified set:
- **designer-published**: specs, plans, and measurements from the designer themselves
- **community-measured**: independent measurements by builders (diyAudio, etc.)
- **peer-reviewed**: academic sources on underlying principles
- **industry**: component manufacturer datasheets, industry publications

## Part B: HOQS Profile

### B1: Create `reports/diy/hoqs.md`

Research HOQS comprehensively via web. Key sources:
- https://www.hoqs.com.au/projects (full project catalog)
- https://www.hoqs.com.au (main site)
- diyAudio threads on Paraflex builds
- Speaker Hardware (https://www.speakerhardware.com) — HOQS kits distributor
- Calum Audio (https://calumaudio.co.uk/pages/paraflex) — authorized builder with build notes

Cover at minimum:
- The Paraflex loading principle — what it is, how it works, how it differs from conventional reflex/horn loading
- **Sub catalog (all models):**
  - Type O variants (1x18, 2x18, 2x12 CRAM/OCRAM)
  - Type C variants (Classic 1x18/1x21/2x15, V1 and V2)
  - Type R (1x21)
  - ELF / C2E variants
  - Any other sub designs listed on the projects page
- **Mid-top catalog:**
  - 2x8" Mid-Top
  - C3DKT 1x12" Kick-Top
  - G1V2 1x12" Kick-Top
  - WS V2 configurations
  - Any other mid-top/kick-top designs
- **HOQS driver lineup** (N185C, N216C, N124C, F-series, etc.)
- Builder/dealer network and support model
- Mark I suitability assessment focused on the Type O 2x18 (builder's primary recommendation) with comparison to other viable options

### B2: Create `reports/diy/hoqs.json`

Structured data companion. Adapt the UDS JSON schema for DIY context:
- Replace `composite_score` with `mark_i_suitability` (qualitative assessment, not numeric)
- Replace `scoring_rationale` with `design_fit_notes`
- Keep `models[]` array with specs per design
- Keep `sources[]` array with provenance tags
- Add `drivers[]` array for HOQS-manufactured drivers

## Part C: JW Sound / JMOD Profile

### C1: Create `reports/diy/jw_sound.md`

Research JW Sound comprehensively via web. Key sources:
- https://www.jwsound.live/designs (full design catalog)
- https://www.jwsound.live/store (available parts/flatpacks)
- diyAudio JMOD build threads (https://www.diyaudio.com/community/threads/jmod-v2-build-thread.429672/)
- AVS Forum MEH threads
- Audio Abattoir MEH build discussions

Cover at minimum:
- The Multiple Entry Horn (MEH) principle — what it is, lineage from Danley/Hinson, how it achieves point-source behavior
- **JMOD** — full specs for v1 and v2 (if v2 info is available), driver options (B&C 12NDL76, 12NDL88, 18 Sound 12NTLW3500, compression driver options), horn geometry, crossover points
- **JMOD-M** — medium format array variant, specs, intended use case
- **SAWMOD** — what it is, how it differs from JMOD
- **Solana** — what it is, specs
- **Ricci designs hosted on JW Sound** (SKRAM, SKHORN) — note these but focus detail on JMOD
- DSP/processing requirements — FIR filter design, recommended amps (Hypex FA253, Linea Research, QSC Q-Sys mentioned in community), crossover topology (3-way active)
- Build complexity assessment — CNC requirement, 3D printed components (mouth adaptor), assembly difficulty relative to typical DIY speaker builds
- Community track record — how many people have built JMODs, reported sound quality impressions, common issues
- Mark I suitability assessment — how JMOD fits as tops paired with HOQS Type O subs

### C2: Create `reports/diy/jw_sound.json`

Structured data companion, same adapted schema as HOQS.

## Part D: DEVLOG Entry

Append Entry 11 to DEVLOG.md:

```markdown
## Entry 11 — DIY Designer Profiles: HOQS & JW Sound (Directive 009)

**Date:** 2025-02-06
**Phase:** Directive 009

### What Happened

Created DIY designer profile format and produced two comprehensive profiles for Mark I planning: HOQS (Paraflex sub and mid-top catalog) and JW Sound (JMOD MEH tops).

### Key Decisions and Rationale

**New report category:** DIY designer profiles live in `reports/diy/` with a format distinct from the commercial company dossiers in `reports/boutique/`. No composite scoring — these profiles assess buildability and Mark I suitability rather than R&D relevance.

**Mark I context:** The project is adding a near-term build track alongside long-term research. Mark I uses community-proven DIY designs built by an authorized HOQS dealer. This does not replace the research program — it runs in parallel as a learning platform.

### Files Changed

- reports/diy/_README.md — Created (DIY profile template)
- reports/diy/hoqs.md — Created
- reports/diy/hoqs.json — Created
- reports/diy/jw_sound.md — Created
- reports/diy/jw_sound.json — Created
- DEVLOG.md — This entry

### Surprises or Pattern Shifts

[Agent fills in based on research findings]

### Open Questions

[Agent fills in based on research findings]
```

---

## Scope Boundaries

**DO:**
- Create `reports/diy/` directory with template and two complete designer profiles
- Conduct web research to populate all sections of both profiles
- Document all specs with source citations and provenance tags
- Include Mark I suitability assessments
- Add DEVLOG Entry 11
- Commit and push all changes

**DO NOT:**
- Modify PLANNING_LOG.md (updated version committed alongside this directive)
- Modify any existing files in `reports/boutique/`
- Modify any knowledge base entries
- Modify VISION.md, STANDARDS.md, or AGENT_PLAN.md
- Modify any historical handoff files
- Apply UDS composite scoring to DIY profiles
- Import unverified specs — if a spec is not published by the designer or measured by community, mark as "not established"

---

## Deliverables

| File | Action |
|------|--------|
| `reports/diy/_README.md` | Created (DIY profile template) |
| `reports/diy/hoqs.md` | Created |
| `reports/diy/hoqs.json` | Created |
| `reports/diy/jw_sound.md` | Created |
| `reports/diy/jw_sound.json` | Created |
| `DEVLOG.md` | Updated (Entry 11) |
| `handoff/009_directive.md` | This file |
| `handoff/009_response.md` | Agent's completion report |

---

## Verification Checklist

- [ ] `reports/diy/_README.md` exists with complete template
- [ ] `reports/diy/hoqs.md` exists with all template sections populated
- [ ] HOQS profile covers Paraflex loading principle
- [ ] HOQS profile includes complete sub catalog (Type O, Type C, Type R, ELF at minimum)
- [ ] HOQS profile includes mid-top catalog
- [ ] HOQS profile includes driver lineup with specs
- [ ] HOQS profile includes Mark I suitability assessment
- [ ] `reports/diy/hoqs.json` exists with adapted schema
- [ ] `reports/diy/jw_sound.md` exists with all template sections populated
- [ ] JW Sound profile covers MEH operating principle
- [ ] JW Sound profile includes JMOD specs (v1, v2 if available)
- [ ] JW Sound profile includes DSP/processing requirements
- [ ] JW Sound profile includes other designs (JMOD-M, SAWMOD, Solana)
- [ ] JW Sound profile includes Mark I suitability assessment
- [ ] `reports/diy/jw_sound.json` exists with adapted schema
- [ ] All specs have source citations with provenance tags
- [ ] No specs imported without source — unknowns marked "not established"
- [ ] DEVLOG.md has Entry 11
- [ ] No files modified outside scope (boutique reports, knowledge base, VISION.md, STANDARDS.md, AGENT_PLAN.md, PLANNING_LOG.md)
- [ ] No historical handoff files edited
- [ ] Git commit and push completed
