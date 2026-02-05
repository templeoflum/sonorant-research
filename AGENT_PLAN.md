# Sonorant Sound — Research Agent Plan & Vision Distillation

---

## PART 1: DISTILLED VISION

### What Sonorant Sound Is

A boutique sound system for intimate communal gatherings (100–200 cap). Not a PA company — a sonic experience entity. The system is a presence with its own life, delivering hyper-real translation with sensual intimacy.

### Core Experiential Goals

- **Transcendence**: Listeners feel transported — ranging from violently ripped into a new dimension to gracefully carried into "aural lovemaking"
- **Hyper-real fidelity**: Psychoacoustically enhanced reproduction that reveals what you didn't know you wanted to hear
- **Visceral sub-weight**: Infrasonic extension felt in chest and bones — clean, minimally distorted, physically present
- **Crystal vocal clarity**: HF detail with snap and transient accuracy, zero sibilance
- **Stereo imaging**: Ultra-wide phantom image with stable center, spatial depth, envelopment
- **Dynamic range over loudness**: Clarity at moderate levels, not volume for its own sake

### Technical Design Priorities (Weighted)

1. HF clarity & transient response (0.23)
2. Directivity control & stereo imaging (0.23)
3. Sub-weight & infrasonic extension (0.23)
4. Psychoacoustic potential (0.20)
5. Small-room viability (0.11)

### System Architecture: OPEN — Determined by Research

**System topology is an open design variable, not a given.**

The research exists to surface all viable architectures so the best one can be selected (or invented) based on evidence. No topology is pre-selected. The experiential goals above are locked; the physical means of achieving them are not.

**Topologies to investigate and compare:**
- **MEH / Synergy horn** — all bands summed through shared horn (Danley, JMOD, ATH). Strong candidate for coherence/imaging goals. Fewer boxes. But complex to build and possibly constraining at scale.
- **Traditional stacks** — separate sub / kick / top / horn. Maximum per-band optimization. More boxes, more alignment complexity, potential comb filtering between enclosures.
- **Coaxial point-source** — coax driver on large waveguide (Fulcrum, KV2 approach). Compact, coherent, but limited LF from a single enclosure.
- **Horn-loaded fullrange + sub** — single large horn covering wide bandwidth with sub below. Funktion-One philosophy territory.
- **Hybrid / novel combinations** — the whole point of first-principles research is that the answer might be something none of these categories describe. Combinations that are "radically simple and different, completely overlooked or unthought of."

**Key insight from JMOD / MEH research:** The traditional assumption of "you need separate bins for everything" is worth questioning. Multi-entry horns demonstrate that dramatically fewer enclosures can achieve superior coherence. This doesn't mean MEH is the answer — it means the bin count and frequency-band-to-enclosure mapping is a design variable, not a given.

**Sub/infra architecture** is also open. Candidates to evaluate:
- Tapped horn (Danley patents, Ricci SKHORN/SKRAM)
- Paraflex / quarter-wave hybrids (HOQS community)
- Horn-loaded (efficiency matching with tops)
- Reflex / passive radiator (simplicity, predictability)
- Cardioid/gradient configurations (small-room rear-rejection)
- Something novel that emerges from the research

### Inspirational References

- **Danley Sound Labs**: Synergy Horn originator — coherence, tapped horn subs, patent lineage
- **Funktion-One**: Visceral presence, bass physicality, acoustic-first philosophy
- **Void Acoustics**: Aesthetic ambition, sculptural forms, enveloping experience
- **JW Sound / JMOD community**: DIY MEH accessibility, CNC/3D-print fabrication, FIR integration
- **Addit Audio**: Large-format 3D-printed MEH (ATH-based), Marcel Batík's Advanced Transition Horn work
- **Scott Hinson**: "The Ultimate Loudspeaker" essay — foundational MEH theory for DIY

### Aesthetic & Identity

- "Glitchy mythopoetic cyber surrealism"
- The system awakens a viscerally more-real-than-real sonic activation
- Ranges from gentle to violent — shows you what you need, not what you expect
- Genre coverage: hyperpop, UKG, jungle, old-school dubstep, intricate noise/soundscapes
- Vinyl-ready, DJ gear, live instruments, open to surround (future)

---

## PART 2: MATERIAL AUDIT

### ✅ Usable As-Is

| Asset | Notes |
|---|---|
| Company master list (166 companies) | Clean input queue for agent |
| UDS v1.0 schema | JSON schemas, tech vocabulary, QA checklist — strong foundation |
| R&D relevance scoring weights | 6-criteria system aligned with Sonorant priorities |
| Tech vocabulary (UDS Section 6) | Controlled tags for cross-brand comparison |
| Ingestion protocol skeleton (UDS Section 12) | 7-step pipeline, needs real implementation |

### ⚠️ Structure Only — Discard Content

| Asset | Action |
|---|---|
| ChatGPT-generated company dossiers | Keep template format. Discard all specific claims. Every fact must be re-sourced. |
| Sonorant "Mark-I" rig spec | Treat as conceptual direction only. The separate kick-bin architecture is superseded by MEH approach. |
| "Sacred Sonic Philology" research | Extract themes and search terms. Verify every specific claim. |

### ❌ Rebuild From Scratch

- Any specific technical specs attributed to products
- Source citations in conversation logs (many hallucinated)
- Case study details (likely mixed real venues with fabricated deployments)

---

## PART 3: RESEARCH AGENT SPECIFICATION

### Agent Name: Transducer Archive

### Mission

Compile verified, source-grounded technical intelligence on loudspeaker companies, designs, patents, and deployments — structured for cross-brand comparison and synthesis into Sonorant Sound's MEH-based system.

### Required Capabilities

1. **Web research** — manufacturer sites, patent databases, trade press, AES papers, integrator case studies
2. **PDF/datasheet parsing** — extract specs from manufacturer documents
3. **Patent search** — Google Patents per company
4. **Structured output** — validated JSON (UDS schema) + markdown dossiers
5. **Source verification** — every claim needs a resolvable URL + date
6. **Conflict detection** — flag when manufacturer vs. independent data diverge

### Company Queue (Prioritized Batches)

| Batch | Category | Priority | Rationale |
|---|---|---|---|
| 1 | Boutique / underground | **Highest** | Funktion-One, Void, Danley, PK Sound, Holoplot, Hennessey, Fulcrum, KV2 |
| 2 | Touring / club majors | **High** | d&b, L-Acoustics, Meyer, Adamson, CODA, Martin, EAW, etc. |
| 3 | Esoteric / specialty | **High** | Omni (MBL, German Physiks), underwater, BMR/DML, directional audio |
| 4 | Home audiophile / cinema | Medium | |
| 5 | Car audio / SPL | Medium | Driver engineering, extreme LF |
| 6 | Studio monitors | Medium | |
| 7 | Industrial / mass notification | Lower | Patents on directional/long-throw tech |
| 8 | DIY / kit vendors | Medium | Enclosure designs, community knowledge |

### Per-Company Pipeline

```
1. RESOLVE ENTITY
   - Confirm IDs, aliases, parent, founding, HQ, key people, status

2. PRIMARY SOURCE SWEEP (priority order)
   a) Manufacturer site → products, datasheets, whitepapers
   b) Google Patents → [company] + loudspeaker|horn|waveguide|array|port|cardioid
   c) AES E-Library → papers by company engineers
   d) Trade press → ProSoundWeb, SOS, audioXpress, Resolution, FOH, ISE
   e) Independent measurements → SynAudCon, Audioholics, ASR, data-bass.com

3. EXTRACT STRUCTURED DATA (per UDS schema)
   - Company, model, case study, patent, source records

4. VERIFY & CROSS-REFERENCE
   - Provenance: manufacturer|independent|derived
   - Confidence: high|med|low
   - Conflicts: record both sides

5. SCORE R&D RELEVANCE (5 criteria, weighted)
   - hf_clarity_transient (0.23)
   - directivity_control_imaging (0.23)
   - sub_weight_infrasonic (0.23)
   - psychoacoustic_potential (0.20)
   - small_room_viability (0.11)

6. TAG WITH TECH VOCABULARY (UDS Section 6)

7. WRITE OUTPUTS
   - reports/<category>/<company>.md + .json
   - Append to index CSVs

8. QA VALIDATION
   - All fields present, units normalized
   - ≥5 sources or audit note
   - Measured vs. claimed separated
   - Derived metrics flagged
   - last_audited date set
```

### Parallel Knowledge Tracks

#### Track A: Acoustics & Psychoacoustics
Small-room acoustics, precedence effect, HRTF, bass perception, infrasonic physiology, directivity in near-field contexts, cardioid/gradient sub theory.
**Sources**: AES papers, Beranek, Toole, Linkwitz

#### Track B: Enclosure Design
MEH/synergy horn theory (Danley patents, Scott Hinson essay, ATH work), tapped horn, Paraflex, horn loading theory, port turbulence, thermal/power compression, materials.
**Sources**: Patents, HOQS/SpeakerPlans community, manufacturer whitepapers, Klippel

#### Track C: Transducer Technology
Compression drivers (throat geometry, diaphragm materials), coaxial designs, large-format LF (21"+), AMT/BMR/planar/ribbon alternatives, T/S parameter interpretation.
**Sources**: B&C, BMS, Faital, Eminence, Celestion engineering docs, patents

#### Track D: Esoteric & Fringe
Ancient resonant architecture, cymatics, parametric/ultrasonic audio, omnidirectional radiation, open-baffle/dipole hybrids, acoustic levitation.
**Sources**: Academic papers, verified archaeological studies, patents, documented experiments

### Quality Gates

1. Every cited URL visited and confirmed
2. Every spec has provenance tag (manufacturer|independent|derived)
3. Conflicts documented with both values
4. Unknown = `null`, never estimated without flag
5. Product status verified (current/discontinued/prototype)

---

## PART 4: NEXT STEPS

### Step 1: Validate UDS Schema
Finalize JSON schema. Add product_line record, patent record, knowledge_article type.

### Step 2: Pilot Batch — Boutique Systems
8 companies, highest priority:
Funktion-One, Void Acoustics, Danley Sound Labs, Fulcrum Acoustic, KV2 Audio, PK Sound, HOLOPLOT, Hennessey Sound Systems

### Step 3: MEH-Specific Research Track
Dedicated deep dive on multi-entry horn lineage:
- Danley Synergy Horn patents and theory
- Scott Hinson's "The Ultimate Loudspeaker"
- JW Sound JMOD (v1, v2, Solana, JMOD-M)
- Marcel Batík's ATH (Advanced Transition Horn)
- Addit Audio large-format 3D-printed MEH
- Bill Waslo's SynCalc modeling tool
- Commercial MEH implementations (Danley SH50, SH96, SM60F, etc.)

### Step 4: Sub Architecture Research
Evaluate sub topologies against Sonorant's infrasonic goals:
- Ricci's SKHORN / SKRAM (tapped horn, data-bass.com measured)
- Paraflex variants (HOQS community)
- Horn-loaded options for sensitivity matching with MEH tops
- Cardioid configurations for small-room deployment

### Step 5: Synthesis (After Sufficient Data)
Cross-reference verified company data + knowledge tracks → Sonorant system design grounded in real evidence, not assumptions.

---

*This document supersedes all prior conversation-log-based specifications.*
